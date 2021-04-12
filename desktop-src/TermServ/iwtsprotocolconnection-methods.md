---
title: Métodos IWTSProtocolConnection
description: La interfaz IWTSProtocolConnection expone los métodos siguientes.
ms.assetid: DBB96D6B-F5A5-4CAF-974F-44D76B9CBFB6
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb89f63aea6b1904eb4319dcce541aeb4d15d34f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419192"
---
# <a name="iwtsprotocolconnection-methods"></a><span data-ttu-id="67f21-103">Métodos IWTSProtocolConnection</span><span class="sxs-lookup"><span data-stu-id="67f21-103">IWTSProtocolConnection Methods</span></span>

<span data-ttu-id="67f21-104">\[IWTSProtocolConnection ya no está disponible para su uso a partir de Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="67f21-104">\[IWTSProtocolConnection is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="67f21-105">La interfaz [**IWTSProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection) expone los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="67f21-105">The [**IWTSProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="67f21-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="67f21-106">In this section</span></span>

-   [<span data-ttu-id="67f21-107">**Método AcceptConnection**</span><span class="sxs-lookup"><span data-stu-id="67f21-107">**AcceptConnection method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-acceptconnection)
-   [<span data-ttu-id="67f21-108">**Método AuthenticateClientToSession**</span><span class="sxs-lookup"><span data-stu-id="67f21-108">**AuthenticateClientToSession method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-authenticateclienttosession)
-   [<span data-ttu-id="67f21-109">**Close (método)**</span><span class="sxs-lookup"><span data-stu-id="67f21-109">**Close method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-close)
-   [<span data-ttu-id="67f21-110">**Método ConnectNotify**</span><span class="sxs-lookup"><span data-stu-id="67f21-110">**ConnectNotify method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-connectnotify)
-   [<span data-ttu-id="67f21-111">**Método CreateVirtualChannel**</span><span class="sxs-lookup"><span data-stu-id="67f21-111">**CreateVirtualChannel method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-createvirtualchannel)
-   [<span data-ttu-id="67f21-112">**Método DisconnectNotify**</span><span class="sxs-lookup"><span data-stu-id="67f21-112">**DisconnectNotify method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-disconnectnotify)
-   [<span data-ttu-id="67f21-113">**Método GetClientData**</span><span class="sxs-lookup"><span data-stu-id="67f21-113">**GetClientData method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getclientdata)
-   [<span data-ttu-id="67f21-114">**Método GetLastInputTime**</span><span class="sxs-lookup"><span data-stu-id="67f21-114">**GetLastInputTime method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlastinputtime)
-   [<span data-ttu-id="67f21-115">**Método GetLicenseConnection**</span><span class="sxs-lookup"><span data-stu-id="67f21-115">**GetLicenseConnection method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlicenseconnection)
-   [<span data-ttu-id="67f21-116">**Método GetLogonErrorRedirector**</span><span class="sxs-lookup"><span data-stu-id="67f21-116">**GetLogonErrorRedirector method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlogonerrorredirector)
-   [<span data-ttu-id="67f21-117">**Método GetProtocolHandles**</span><span class="sxs-lookup"><span data-stu-id="67f21-117">**GetProtocolHandles method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getprotocolhandles)
-   [<span data-ttu-id="67f21-118">**Método GetProtocolStatus**</span><span class="sxs-lookup"><span data-stu-id="67f21-118">**GetProtocolStatus method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getprotocolstatus)
-   [<span data-ttu-id="67f21-119">**Método GetShadowConnection**</span><span class="sxs-lookup"><span data-stu-id="67f21-119">**GetShadowConnection method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getshadowconnection)
-   [<span data-ttu-id="67f21-120">**Método GetUserCredentials**</span><span class="sxs-lookup"><span data-stu-id="67f21-120">**GetUserCredentials method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getusercredentials)
-   [<span data-ttu-id="67f21-121">**Método GetUserData**</span><span class="sxs-lookup"><span data-stu-id="67f21-121">**GetUserData method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getuserdata)
-   [<span data-ttu-id="67f21-122">**Método IsUserAllowedToLogon**</span><span class="sxs-lookup"><span data-stu-id="67f21-122">**IsUserAllowedToLogon method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-isuserallowedtologon)
-   [<span data-ttu-id="67f21-123">**Método LogonNotify**</span><span class="sxs-lookup"><span data-stu-id="67f21-123">**LogonNotify method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-logonnotify)
-   [<span data-ttu-id="67f21-124">**Método NotifySessionId**</span><span class="sxs-lookup"><span data-stu-id="67f21-124">**NotifySessionId method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-notifysessionid)
-   [<span data-ttu-id="67f21-125">**Método QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="67f21-125">**QueryProperty method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty)
-   [<span data-ttu-id="67f21-126">**Método SendBeep**</span><span class="sxs-lookup"><span data-stu-id="67f21-126">**SendBeep method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sendbeep)
-   [<span data-ttu-id="67f21-127">**Método SendPolicyData**</span><span class="sxs-lookup"><span data-stu-id="67f21-127">**SendPolicyData method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sendpolicydata)
-   [<span data-ttu-id="67f21-128">**Método SessionArbitrationEnumeration**</span><span class="sxs-lookup"><span data-stu-id="67f21-128">**SessionArbitrationEnumeration method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sessionarbitrationenumeration)
-   [<span data-ttu-id="67f21-129">**método SetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="67f21-129">**SetErrorInfo method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-seterrorinfo)

 

 




