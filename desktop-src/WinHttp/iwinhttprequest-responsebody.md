---
description: Recupera el cuerpo de la entidad de respuesta como una matriz de bytes sin signo.
ms.assetid: 557913e0-9f19-42fc-bfca-9ed248972b4b
title: 'IWinHttpRequest:: ResponseBody (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseBody
- IWinHttpRequest.get_ResponseBody
- WinHttpRequest.ResponseBody
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 5a608f2744ad2880ecf7c4862b03821afcef9630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707220"
---
# <a name="iwinhttprequestresponsebody-property"></a><span data-ttu-id="ea104-103">IWinHttpRequest:: ResponseBody (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ea104-103">IWinHttpRequest::ResponseBody property</span></span>

<span data-ttu-id="ea104-104">La propiedad **ResponseBody** recupera el cuerpo de la entidad de respuesta como una matriz de bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="ea104-104">The **ResponseBody** property retrieves the response entity body as an array of unsigned bytes.</span></span>

<span data-ttu-id="ea104-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ea104-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea104-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea104-106">Syntax</span></span>


```C++
HRESULT get_ResponseBody(
  [out, retval] VARIANT *Body
);
```


```JScript

vtResponseBody = WinHttpRequest.ResponseBody
```





## <a name="property-value"></a><span data-ttu-id="ea104-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ea104-107">Property value</span></span>

<span data-ttu-id="ea104-108">Un valor **Variant** que recibe el cuerpo de la entidad de respuesta como una matriz de bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="ea104-108">A **Variant** value that receives the response entity body as an array of unsigned bytes.</span></span> <span data-ttu-id="ea104-109">Esta matriz contiene los datos sin procesar recibidos directamente desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="ea104-109">This array contains the raw data as received directly from the server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ea104-110">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ea104-110">Error codes</span></span>

<span data-ttu-id="ea104-111">El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**</span><span class="sxs-lookup"><span data-stu-id="ea104-111">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea104-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea104-112">Remarks</span></span>

<span data-ttu-id="ea104-113">Esta propiedad devuelve los datos de la respuesta en una matriz de bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="ea104-113">This property returns the response data in an array of unsigned bytes.</span></span> <span data-ttu-id="ea104-114">Si la respuesta no tiene un cuerpo de respuesta, se devuelve una variante vacía.</span><span class="sxs-lookup"><span data-stu-id="ea104-114">If the response does not have a response body, an empty variant is returned.</span></span> <span data-ttu-id="ea104-115">Esta propiedad solo se puede invocar después de que se haya llamado al método [**send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="ea104-115">This property can only be invoked after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="ea104-116">Para obtener más información acerca de la implementación de Windows XP y Windows 2000, consulte [requisitos de tiempo de ejecución](winhttp-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="ea104-116">For more information about implementation for Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ea104-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea104-117">Requirements</span></span>



| <span data-ttu-id="ea104-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea104-118">Requirement</span></span> | <span data-ttu-id="ea104-119">Value</span><span class="sxs-lookup"><span data-stu-id="ea104-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea104-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea104-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ea104-121">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="ea104-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="ea104-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea104-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ea104-123">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="ea104-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="ea104-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="ea104-124">Redistributable</span></span><br/>          | <span data-ttu-id="ea104-125">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ea104-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="ea104-126">IDL</span><span class="sxs-lookup"><span data-stu-id="ea104-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ea104-127"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ea104-127"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="ea104-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea104-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="ea104-129"><dt>Winhttp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea104-129"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="ea104-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ea104-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea104-131"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea104-131"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ea104-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea104-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea104-133">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="ea104-133">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="ea104-134">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="ea104-134">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="ea104-135">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="ea104-135">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)
</dt> <dt>

[<span data-ttu-id="ea104-136">**ResponseText**</span><span class="sxs-lookup"><span data-stu-id="ea104-136">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)
</dt> <dt>

[<span data-ttu-id="ea104-137">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="ea104-137">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




