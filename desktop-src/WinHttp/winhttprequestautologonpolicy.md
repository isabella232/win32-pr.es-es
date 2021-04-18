---
description: Incluye posibles valores para la Directiva de inicio de sesión automático.
ms.assetid: dad4f6a7-8e84-4f4f-b962-4189e3dc01f7
title: Enumeración WinHttpRequestAutoLogonPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestAutoLogonPolicy
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: dab3dc14dd194e36b9b4d1225f77161005b9d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715160"
---
# <a name="winhttprequestautologonpolicy-enumeration"></a><span data-ttu-id="0df73-103">Enumeración WinHttpRequestAutoLogonPolicy</span><span class="sxs-lookup"><span data-stu-id="0df73-103">WinHttpRequestAutoLogonPolicy enumeration</span></span>

<span data-ttu-id="0df73-104">La enumeración **WinHttpRequestAutoLogonPolicy** incluye posibles valores para la [Directiva de inicio de sesión automático](authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="0df73-104">The **WinHttpRequestAutoLogonPolicy** enumeration includes possible settings for the [Automatic Logon Policy](authentication-in-winhttp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0df73-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0df73-105">Syntax</span></span>


```C++
typedef enum WinHttpRequestAutoLogonPolicy { 
  AutoLogonPolicy_Always             = 0,
  AutoLogonPolicy_OnlyIfBypassProxy  = 1,
  AutoLogonPolicy_Never              = 2
} WinHttpRequestAutoLogonPolicy;
```



## <a name="constants"></a><span data-ttu-id="0df73-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="0df73-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0df73-107"><span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**AutoLogonPolicy \_ siempre**</span><span class="sxs-lookup"><span data-stu-id="0df73-107"><span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**AutoLogonPolicy\_Always**</span></span>
</dt> <dd>

<span data-ttu-id="0df73-108">Se realiza un inicio de sesión autenticado con las credenciales predeterminadas para todas las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="0df73-108">An authenticated log on, using the default credentials, is performed for all requests.</span></span>

</dd> <dt>

<span data-ttu-id="0df73-109"><span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**AutoLogonPolicy \_ OnlyIfBypassProxy**</span><span class="sxs-lookup"><span data-stu-id="0df73-109"><span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**AutoLogonPolicy\_OnlyIfBypassProxy**</span></span>
</dt> <dd>

<span data-ttu-id="0df73-110">Un inicio de sesión autenticado, con las credenciales predeterminadas, solo se realiza para las solicitudes en la Intranet local.</span><span class="sxs-lookup"><span data-stu-id="0df73-110">An authenticated log on, using the default credentials, is performed only for requests on the local intranet.</span></span> <span data-ttu-id="0df73-111">La Intranet local se considera cualquier servidor de la lista de omisión de proxy en la configuración del proxy actual.</span><span class="sxs-lookup"><span data-stu-id="0df73-111">The local intranet is considered to be any server on the proxy bypass list in the current proxy configuration.</span></span>

</dd> <dt>

<span data-ttu-id="0df73-112"><span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**AutoLogonPolicy \_ nunca**</span><span class="sxs-lookup"><span data-stu-id="0df73-112"><span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**AutoLogonPolicy\_Never**</span></span>
</dt> <dd>

<span data-ttu-id="0df73-113">La autenticación no se utiliza automáticamente.</span><span class="sxs-lookup"><span data-stu-id="0df73-113">Authentication is not used automatically.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0df73-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0df73-114">Remarks</span></span>

<span data-ttu-id="0df73-115">Para establecer la Directiva de inicio de sesión automático, llame al método [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md) y especifique una de las constantes anteriores.</span><span class="sxs-lookup"><span data-stu-id="0df73-115">To set the automatic logon policy, call the [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md) method and specify one of the preceding constants.</span></span>

> [!Note]  
> <span data-ttu-id="0df73-116">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="0df73-116">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0df73-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0df73-117">Requirements</span></span>



| <span data-ttu-id="0df73-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0df73-118">Requirement</span></span> | <span data-ttu-id="0df73-119">Value</span><span class="sxs-lookup"><span data-stu-id="0df73-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0df73-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0df73-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0df73-121">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="0df73-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="0df73-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0df73-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0df73-123">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="0df73-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="0df73-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="0df73-124">Redistributable</span></span><br/>          | <span data-ttu-id="0df73-125">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="0df73-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="0df73-126">IDL</span><span class="sxs-lookup"><span data-stu-id="0df73-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0df73-127"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0df73-127"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0df73-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0df73-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0df73-129">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="0df73-129">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




