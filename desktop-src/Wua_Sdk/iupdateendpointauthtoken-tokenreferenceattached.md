---
description: Obtiene el formato XML de una referencia adjunta al token.
ms.assetid: F4329A2E-61FD-40E0-9E24-87C9A4585E55
title: 'IUpdateEndpointAuthToken:: TokenReferenceAttached (método) (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceAttached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 9582c54c42e2416d5d7a98e85eba3151fd6769a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686854"
---
# <a name="iupdateendpointauthtokentokenreferenceattached-method"></a><span data-ttu-id="5ecaf-103">IUpdateEndpointAuthToken:: TokenReferenceAttached (método)</span><span class="sxs-lookup"><span data-stu-id="5ecaf-103">IUpdateEndpointAuthToken::TokenReferenceAttached method</span></span>

<span data-ttu-id="5ecaf-104">Obtiene el formato XML de una referencia adjunta al token.</span><span class="sxs-lookup"><span data-stu-id="5ecaf-104">Gets the XML format of an attached reference to the token.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ecaf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ecaf-105">Syntax</span></span>


```C++
HRESULT TokenReferenceAttached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a><span data-ttu-id="5ecaf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ecaf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ecaf-107">*pszTokenReference* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5ecaf-107">*pszTokenReference* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ecaf-108">Puntero a la referencia de token adjunta.</span><span class="sxs-lookup"><span data-stu-id="5ecaf-108">Pointer to the attached token reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ecaf-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ecaf-109">Return value</span></span>

<span data-ttu-id="5ecaf-110">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="5ecaf-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="5ecaf-111">De lo contrario, devuelve un código de error COM o Windows.</span><span class="sxs-lookup"><span data-stu-id="5ecaf-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ecaf-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ecaf-112">Remarks</span></span>

<span data-ttu-id="5ecaf-113">Una referencia adjunta hace referencia a un referece (como el signiture que usa el token) que está en el mismo mensaje en el que reside el token.</span><span class="sxs-lookup"><span data-stu-id="5ecaf-113">An attached reference refers a referece (such as the signiture that is using the token) that is in the same message where the token resides.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ecaf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ecaf-114">Requirements</span></span>



| <span data-ttu-id="5ecaf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ecaf-115">Requirement</span></span> | <span data-ttu-id="5ecaf-116">Value</span><span class="sxs-lookup"><span data-stu-id="5ecaf-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ecaf-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ecaf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5ecaf-118">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="5ecaf-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="5ecaf-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ecaf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5ecaf-120">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="5ecaf-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="5ecaf-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ecaf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ecaf-122"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ecaf-122"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ecaf-123">IDL</span><span class="sxs-lookup"><span data-stu-id="5ecaf-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5ecaf-124"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5ecaf-124"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="5ecaf-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ecaf-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="5ecaf-126"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ecaf-126"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="5ecaf-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5ecaf-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ecaf-128"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ecaf-128"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ecaf-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ecaf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ecaf-130">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="5ecaf-130">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




