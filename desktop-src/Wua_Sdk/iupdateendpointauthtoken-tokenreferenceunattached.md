---
description: Obtiene el formato XML de una referencia no adjunta al token.
ms.assetid: D5D61ED7-68FB-4FC0-9C2A-90D3B1219351
title: 'IUpdateEndpointAuthToken:: TokenReferenceUnattached (método) (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceUnattached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 7f9a25c444cf1ba8421d3787a9ead242750e5756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705725"
---
# <a name="iupdateendpointauthtokentokenreferenceunattached-method"></a><span data-ttu-id="c4fce-103">IUpdateEndpointAuthToken:: TokenReferenceUnattached (método)</span><span class="sxs-lookup"><span data-stu-id="c4fce-103">IUpdateEndpointAuthToken::TokenReferenceUnattached method</span></span>

<span data-ttu-id="c4fce-104">Obtiene el formato XML de una referencia no adjunta al token.</span><span class="sxs-lookup"><span data-stu-id="c4fce-104">Gets the XML format of an unattached reference to the token.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4fce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4fce-105">Syntax</span></span>


```C++
HRESULT TokenReferenceUnattached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a><span data-ttu-id="c4fce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4fce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4fce-107">*pszTokenReference* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c4fce-107">*pszTokenReference* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4fce-108">Puntero a la referencia de token no adjunta.</span><span class="sxs-lookup"><span data-stu-id="c4fce-108">Pointer to the unattached token reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4fce-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4fce-109">Return value</span></span>

<span data-ttu-id="c4fce-110">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="c4fce-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="c4fce-111">De lo contrario, devuelve un código de error COM o Windows.</span><span class="sxs-lookup"><span data-stu-id="c4fce-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4fce-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4fce-112">Remarks</span></span>

<span data-ttu-id="c4fce-113">Una referencia no adjunta hace referencia a un referece (como el signiture que usa el token) que no está en el mensaje en el que reside el token.</span><span class="sxs-lookup"><span data-stu-id="c4fce-113">An unattached reference refers a referece (such as the signiture that is using the token) that is not in the message where the token resides.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4fce-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4fce-114">Requirements</span></span>



| <span data-ttu-id="c4fce-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4fce-115">Requirement</span></span> | <span data-ttu-id="c4fce-116">Value</span><span class="sxs-lookup"><span data-stu-id="c4fce-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4fce-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4fce-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c4fce-118">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="c4fce-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="c4fce-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4fce-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c4fce-120">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="c4fce-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="c4fce-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4fce-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4fce-122"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4fce-122"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4fce-123">IDL</span><span class="sxs-lookup"><span data-stu-id="c4fce-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c4fce-124"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c4fce-124"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="c4fce-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c4fce-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="c4fce-126"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4fce-126"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="c4fce-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c4fce-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4fce-128"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4fce-128"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4fce-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4fce-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4fce-130">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="c4fce-130">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




