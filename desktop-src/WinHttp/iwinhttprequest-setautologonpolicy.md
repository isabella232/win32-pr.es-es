---
description: Establece la Directiva de inicio de sesión automático actual.
ms.assetid: bc8e8c9c-574e-4392-b336-2c06947022ee
title: 'IWinHttpRequest:: SetAutoLogonPolicy (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetAutoLogonPolicy
- WinHttpRequest.SetAutoLogonPolicy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: cad8bd0080d10a1395a0a9d275951ff961a60bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716643"
---
# <a name="iwinhttprequestsetautologonpolicy-method"></a><span data-ttu-id="602b8-103">IWinHttpRequest:: SetAutoLogonPolicy (método)</span><span class="sxs-lookup"><span data-stu-id="602b8-103">IWinHttpRequest::SetAutoLogonPolicy method</span></span>

<span data-ttu-id="602b8-104">El método **SetAutoLogonPolicy** establece la [Directiva de inicio de sesión automático](authentication-in-winhttp.md)actual.</span><span class="sxs-lookup"><span data-stu-id="602b8-104">The **SetAutoLogonPolicy** method sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="602b8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="602b8-105">Syntax</span></span>


```C++
HRESULT SetAutoLogonPolicy(
  [in] WinHttpRequestAutoLogonPolicy AutoLogonPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="602b8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="602b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="602b8-107">*AutoLogonPolicy* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="602b8-107">*AutoLogonPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="602b8-108">Especifica la Directiva de inicio de sesión automático actual.</span><span class="sxs-lookup"><span data-stu-id="602b8-108">Specifies the current automatic logon policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="602b8-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="602b8-109">Return value</span></span>

<span data-ttu-id="602b8-110">El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**</span><span class="sxs-lookup"><span data-stu-id="602b8-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="602b8-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="602b8-111">Remarks</span></span>

<span data-ttu-id="602b8-112">La directiva predeterminada es [**AutoLogonPolicy \_ OnlyIfBypassProxy**](winhttprequestautologonpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="602b8-112">The default policy is [**AutoLogonPolicy\_OnlyIfBypassProxy**](winhttprequestautologonpolicy.md).</span></span>

<span data-ttu-id="602b8-113">Llame a **SetAutoLogonPolicy** para establecer la Directiva de inicio de sesión automático antes de llamar a [**send**](iwinhttprequest-send.md) para enviar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="602b8-113">Call **SetAutoLogonPolicy** to set the automatic logon policy before calling [**Send**](iwinhttprequest-send.md) to send the request.</span></span>

> [!Note]  
> <span data-ttu-id="602b8-114">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="602b8-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="602b8-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="602b8-115">Examples</span></span>

<span data-ttu-id="602b8-116">En el ejemplo de scripting siguiente se muestra cómo establecer la Directiva de inicio de sesión automático para que nunca use NTLM o negociar la autenticación automáticamente.</span><span class="sxs-lookup"><span data-stu-id="602b8-116">The following scripting example shows how to set the automatic logon policy to never use NTLM or Negotiate authentication automatically.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Do not automatically send user credentials.
HttpReq.SetAutoLogonPolicy(2);

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="602b8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="602b8-117">Requirements</span></span>



| <span data-ttu-id="602b8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="602b8-118">Requirement</span></span> | <span data-ttu-id="602b8-119">Value</span><span class="sxs-lookup"><span data-stu-id="602b8-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="602b8-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="602b8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="602b8-121">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="602b8-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="602b8-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="602b8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="602b8-123">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="602b8-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="602b8-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="602b8-124">Redistributable</span></span><br/>          | <span data-ttu-id="602b8-125">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="602b8-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="602b8-126">IDL</span><span class="sxs-lookup"><span data-stu-id="602b8-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="602b8-127"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="602b8-127"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="602b8-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="602b8-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="602b8-129"><dt>Winhttp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="602b8-129"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="602b8-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="602b8-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="602b8-131"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="602b8-131"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="602b8-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="602b8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="602b8-133">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="602b8-133">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="602b8-134">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="602b8-134">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="602b8-135">Autenticación en WinHTTP</span><span class="sxs-lookup"><span data-stu-id="602b8-135">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="602b8-136">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="602b8-136">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




