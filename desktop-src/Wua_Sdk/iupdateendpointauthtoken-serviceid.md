---
description: Obtiene el identificador del servicio que se va a autenticar con el token del extremo.
ms.assetid: FE110B8E-F8FB-4CC8-BDD8-6427BA8B7920
title: 'IUpdateEndpointAuthToken:: ServiceID (método) (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.ServiceID
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 8384baa0a4f8bb48e603e0f2f8bed417e783b7f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715282"
---
# <a name="iupdateendpointauthtokenserviceid-method"></a><span data-ttu-id="858ab-103">IUpdateEndpointAuthToken:: ServiceID (método)</span><span class="sxs-lookup"><span data-stu-id="858ab-103">IUpdateEndpointAuthToken::ServiceID method</span></span>

<span data-ttu-id="858ab-104">Obtiene el identificador del servicio que se va a autenticar con el token del extremo.</span><span class="sxs-lookup"><span data-stu-id="858ab-104">Gets the identifier of the service to be authenticated with the endpoint token.</span></span>

## <a name="syntax"></a><span data-ttu-id="858ab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="858ab-105">Syntax</span></span>


```C++
HRESULT ServiceID(
  [out] GUID *pServiceID
);
```



## <a name="parameters"></a><span data-ttu-id="858ab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="858ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="858ab-107">*pServiceID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="858ab-107">*pServiceID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="858ab-108">Identificador del servicio.</span><span class="sxs-lookup"><span data-stu-id="858ab-108">The identifier of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="858ab-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="858ab-109">Return value</span></span>

<span data-ttu-id="858ab-110">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="858ab-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="858ab-111">De lo contrario, devuelve un código de error COM o Windows.</span><span class="sxs-lookup"><span data-stu-id="858ab-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="858ab-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="858ab-112">Requirements</span></span>



| <span data-ttu-id="858ab-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="858ab-113">Requirement</span></span> | <span data-ttu-id="858ab-114">Value</span><span class="sxs-lookup"><span data-stu-id="858ab-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="858ab-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="858ab-115">Minimum supported client</span></span><br/> | <span data-ttu-id="858ab-116">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="858ab-116">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="858ab-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="858ab-117">Minimum supported server</span></span><br/> | <span data-ttu-id="858ab-118">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="858ab-118">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="858ab-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="858ab-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="858ab-120"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="858ab-120"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="858ab-121">IDL</span><span class="sxs-lookup"><span data-stu-id="858ab-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="858ab-122"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="858ab-122"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="858ab-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="858ab-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="858ab-124"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="858ab-124"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="858ab-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="858ab-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="858ab-126"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="858ab-126"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="858ab-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="858ab-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="858ab-128">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="858ab-128">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




