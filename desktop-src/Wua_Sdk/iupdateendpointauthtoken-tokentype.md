---
description: Obtiene el tipo del token del punto de conexión, como un token WS-Security SAML (Lenguaje de marcado de aserción de seguridad) 1,1.
ms.assetid: 1C6FFAD7-DC80-4957-96B4-FA0D954786DD
title: 'IUpdateEndpointAuthToken:: TokenType (método) (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bc2373c5dd49a3bf01d39b63360a3cf9df9f57d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542262"
---
# <a name="iupdateendpointauthtokentokentype-method"></a><span data-ttu-id="334af-103">IUpdateEndpointAuthToken:: TokenType (método)</span><span class="sxs-lookup"><span data-stu-id="334af-103">IUpdateEndpointAuthToken::TokenType method</span></span>

<span data-ttu-id="334af-104">Obtiene el tipo del token del punto de conexión, como un token WS-Security SAML (Lenguaje de marcado de aserción de seguridad) 1,1.</span><span class="sxs-lookup"><span data-stu-id="334af-104">Gets the type of the endpoint token, such as a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span>

## <a name="syntax"></a><span data-ttu-id="334af-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="334af-105">Syntax</span></span>


```C++
HRESULT TokenType(
  [out] UpdateEndpointAuthTokenType *pTokenType
);
```



## <a name="parameters"></a><span data-ttu-id="334af-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="334af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="334af-107">*pTokenType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="334af-107">*pTokenType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="334af-108">Tipo del token del extremo.</span><span class="sxs-lookup"><span data-stu-id="334af-108">The type of the endpoint token.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="334af-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="334af-109">Return value</span></span>

<span data-ttu-id="334af-110">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="334af-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="334af-111">De lo contrario, devuelve un código de error COM o Windows.</span><span class="sxs-lookup"><span data-stu-id="334af-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="334af-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="334af-112">Requirements</span></span>



| <span data-ttu-id="334af-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="334af-113">Requirement</span></span> | <span data-ttu-id="334af-114">Value</span><span class="sxs-lookup"><span data-stu-id="334af-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="334af-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="334af-115">Minimum supported client</span></span><br/> | <span data-ttu-id="334af-116">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="334af-116">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="334af-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="334af-117">Minimum supported server</span></span><br/> | <span data-ttu-id="334af-118">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="334af-118">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="334af-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="334af-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="334af-120"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="334af-120"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="334af-121">IDL</span><span class="sxs-lookup"><span data-stu-id="334af-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="334af-122"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="334af-122"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="334af-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="334af-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="334af-124"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="334af-124"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="334af-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="334af-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="334af-126"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="334af-126"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="334af-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="334af-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="334af-128">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="334af-128">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




