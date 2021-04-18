---
description: Obtiene los datos XML (enviados a través de la conexión) que representa el token.
ms.assetid: 52EC991A-0499-4182-AC4F-512BAFB4F896
title: 'IUpdateEndpointAuthToken:: TokenData (método) (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenData
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: e75df7f5b13eaf36854cf7ed9abc5988b02462ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715281"
---
# <a name="iupdateendpointauthtokentokendata-method"></a><span data-ttu-id="34102-103">IUpdateEndpointAuthToken:: TokenData (método)</span><span class="sxs-lookup"><span data-stu-id="34102-103">IUpdateEndpointAuthToken::TokenData method</span></span>

<span data-ttu-id="34102-104">Obtiene los datos XML (enviados a través de la conexión) que representa el token.</span><span class="sxs-lookup"><span data-stu-id="34102-104">Gets the XML data (sent over the wire) that represents the token.</span></span>

## <a name="syntax"></a><span data-ttu-id="34102-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34102-105">Syntax</span></span>


```C++
HRESULT TokenData(
  [out] BSTR *pszTokenData
);
```



## <a name="parameters"></a><span data-ttu-id="34102-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34102-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34102-107">*pszTokenData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="34102-107">*pszTokenData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34102-108">Datos XML (enviados a través de la conexión) que representa el token.</span><span class="sxs-lookup"><span data-stu-id="34102-108">The XML data (sent over the wire) that represents the token.</span></span> <span data-ttu-id="34102-109">Por ejemplo, los datos de un token WS-Security SAML (Lenguaje de marcado de aserción de seguridad) 1,1 es el código SAML que se agrega a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="34102-109">For example, the data for a WS-Security SAML (Security Assertion Markup Language) 1.1 token is the SAML code that is added to the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34102-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34102-110">Return value</span></span>

<span data-ttu-id="34102-111">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="34102-111">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="34102-112">De lo contrario, devuelve un código de error COM o Windows.</span><span class="sxs-lookup"><span data-stu-id="34102-112">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="34102-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34102-113">Requirements</span></span>



| <span data-ttu-id="34102-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="34102-114">Requirement</span></span> | <span data-ttu-id="34102-115">Value</span><span class="sxs-lookup"><span data-stu-id="34102-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34102-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34102-116">Minimum supported client</span></span><br/> | <span data-ttu-id="34102-117">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="34102-117">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="34102-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34102-118">Minimum supported server</span></span><br/> | <span data-ttu-id="34102-119">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="34102-119">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="34102-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34102-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="34102-121"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="34102-121"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="34102-122">IDL</span><span class="sxs-lookup"><span data-stu-id="34102-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="34102-123"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="34102-123"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="34102-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="34102-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="34102-125"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34102-125"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="34102-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="34102-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34102-127"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34102-127"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34102-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="34102-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34102-129">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="34102-129">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




