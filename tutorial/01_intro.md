<!-- markdownlint-disable MD002 MD041 -->

<span data-ttu-id="9d01b-101">このチュートリアルでは、Azure Active Directory (Azure AD) でユーザーアカウントが変更されたときに通知 (webhooks) を使用してクエリを実行し、ユーザーにすべての変更を反映するためにデルタクエリ API を使用してクエリを実行する .NET コアアプリを構築する方法について説明します。最後のクエリが実行されてからのアカウント。</span><span class="sxs-lookup"><span data-stu-id="9d01b-101">This tutorial teaches you how to build a .NET Core app that uses the Microsoft Graph API to receive notifications (webhooks) when a user account changes in Azure Active Directory (Azure AD) and perform queries using the delta query API to receive all changes to user accounts since the last query was made.</span></span>

> [!TIP]
> <span data-ttu-id="9d01b-102">完成したチュートリアルをダウンロードするだけで済む場合は、 [GitHub リポジトリ](https://github.com/microsoftgraph/msgraph-training-changenotifications)をダウンロードするか、クローンを作成できます。</span><span class="sxs-lookup"><span data-stu-id="9d01b-102">If you prefer to just download the completed tutorial, you can download or clone the [GitHub repository](https://github.com/microsoftgraph/msgraph-training-changenotifications).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9d01b-103">前提条件</span><span class="sxs-lookup"><span data-stu-id="9d01b-103">Prerequisites</span></span>

<span data-ttu-id="9d01b-104">このチュートリアルを開始する前に、開発用コンピューターに[.Net Core 2.2 SDK](https://dotnet.microsoft.com/download)と[Visual Studio コード](https://code.visualstudio.com/)をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d01b-104">Before you start this tutorial, you should have [.NET Core 2.2 SDK](https://dotnet.microsoft.com/download) and [Visual Studio Code](https://code.visualstudio.com/) installed on your development machine.</span></span>

> [!NOTE]
> <span data-ttu-id="9d01b-105">このチュートリアルは、.NET コアバージョン2.2 で記述されています。</span><span class="sxs-lookup"><span data-stu-id="9d01b-105">This tutorial was written with .NET Core version 2.2.</span></span> <span data-ttu-id="9d01b-106">このガイドの手順は、他のバージョンでは動作しますが、テストされていません。</span><span class="sxs-lookup"><span data-stu-id="9d01b-106">The steps in this guide may work with other versions, but that has not been tested.</span></span>

## <a name="watch-the-tutorial"></a><span data-ttu-id="9d01b-107">チュートリアルを見る</span><span class="sxs-lookup"><span data-stu-id="9d01b-107">Watch the tutorial</span></span>

<span data-ttu-id="9d01b-108">このモジュールは、Office 開発 YouTube チャネルで記録されており、利用できます。</span><span class="sxs-lookup"><span data-stu-id="9d01b-108">This module has been recorded and is available in the Office Development YouTube channel.</span></span>

<!-- markdownlint-disable MD033 MD034 -->
<br/>

> [!VIDEO https://www.youtube-nocookie.com/embed/fThiCZmIcMQ]
<!-- markdownlint-enable MD033 MD034 -->

## <a name="feedback"></a><span data-ttu-id="9d01b-109">フィードバック</span><span class="sxs-lookup"><span data-stu-id="9d01b-109">Feedback</span></span>

<span data-ttu-id="9d01b-110">このチュートリアルに関するフィードバックは、 [GitHub リポジトリ](https://github.com/microsoftgraph/msgraph-training-changenotifications)に記入してください。</span><span class="sxs-lookup"><span data-stu-id="9d01b-110">Please provide any feedback on this tutorial in the [GitHub repository](https://github.com/microsoftgraph/msgraph-training-changenotifications).</span></span>
