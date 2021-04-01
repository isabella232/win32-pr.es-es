---
description: Devuelve el tipo de token de autenticación preferido para el extremo del servicio.
ms.assetid: DF60C49A-89FE-4EEB-8E82-C2C43F2D2F2A
title: 'IUpdateEndpointAuthProvider:: GetPreferredEndpointTokenType (método) (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetPreferredEndpointTokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 670835ee3c2dfd01ae46a7cf78395959ea9a26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275539"
---
# <a name="iupdateendpointauthprovidergetpreferredendpointtokentype-method"></a><span data-ttu-id="accd8-103">IUpdateEndpointAuthProvider:: GetPreferredEndpointTokenType (método)</span><span class="sxs-lookup"><span data-stu-id="accd8-103">IUpdateEndpointAuthProvider::GetPreferredEndpointTokenType method</span></span>

<span data-ttu-id="accd8-104">Devuelve el tipo de token de autenticación preferido para el extremo del servicio.</span><span class="sxs-lookup"><span data-stu-id="accd8-104">Returns the preferred type of authentication token for the endpoint of the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="accd8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="accd8-105">Syntax</span></span>


```C++
HRESULT GetPreferredEndpointTokenType(
  [in]  GUID               serviceId,
  [in]  UpdateEndpointType endpointType,
  [in]  ULONG              ulRequestedTypes,
  [out] ULONG              *pulPreferredTokenTypes
);
```



## <a name="parameters"></a><span data-ttu-id="accd8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="accd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="accd8-107">*serviceId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="accd8-107">*serviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="accd8-108">Identifica el servicio que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="accd8-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="accd8-109">*endpointType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="accd8-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="accd8-110">Identifica el tipo de punto de conexión tneeded para conectarse al servicio.</span><span class="sxs-lookup"><span data-stu-id="accd8-110">Identifies the type of endpoint tneeded to connect to the service.</span></span>

</dd> <dt>

<span data-ttu-id="accd8-111">*ulRequestedTypes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="accd8-111">*ulRequestedTypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="accd8-112">Identifica el conjunto de tokens ORed que admite el extremo.</span><span class="sxs-lookup"><span data-stu-id="accd8-112">Identifies the ORed set of tokens that are supported by the endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="accd8-113">*pulPreferredTokenTypes* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="accd8-113">*pulPreferredTokenTypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="accd8-114">Especifique el conjunto ORed de tipos de token de autenticación preferidos.</span><span class="sxs-lookup"><span data-stu-id="accd8-114">Specify the ORed set of authentication token types that are preferred.</span></span> <span data-ttu-id="accd8-115">(Se establece en 0 para indicar que no se necesita ningún token de autenticación).</span><span class="sxs-lookup"><span data-stu-id="accd8-115">(Set to 0 to indicate that no authentication token is needed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="accd8-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="accd8-116">Return value</span></span>

<span data-ttu-id="accd8-117">Devuelve S \_ correcto si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="accd8-117">Returns S\_OK if successful.</span></span> <span data-ttu-id="accd8-118">De lo contrario, devuelve un código de error COM o Windows.</span><span class="sxs-lookup"><span data-stu-id="accd8-118">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="accd8-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="accd8-119">Remarks</span></span>

<span data-ttu-id="accd8-120">Cuando se devuelve este método, WUA elige un tipo de token de los tipos preferidos y lo pasa al parámetro tokenType del método [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md) .</span><span class="sxs-lookup"><span data-stu-id="accd8-120">When this method is returned, WUA chooses a token type from the preferred types and passes it to the tokenType parameter of the [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="accd8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="accd8-121">Requirements</span></span>



| <span data-ttu-id="accd8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="accd8-122">Requirement</span></span> | <span data-ttu-id="accd8-123">Value</span><span class="sxs-lookup"><span data-stu-id="accd8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="accd8-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="accd8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="accd8-125">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="accd8-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="accd8-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="accd8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="accd8-127">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="accd8-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="accd8-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="accd8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="accd8-129"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="accd8-129"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="accd8-130">IDL</span><span class="sxs-lookup"><span data-stu-id="accd8-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="accd8-131"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="accd8-131"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="accd8-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="accd8-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="accd8-133"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="accd8-133"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="accd8-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="accd8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="accd8-135"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="accd8-135"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="accd8-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="accd8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="accd8-137">**IUpdateEndpointAuthProvider**</span><span class="sxs-lookup"><span data-stu-id="accd8-137">**IUpdateEndpointAuthProvider**</span></span>](iupdateendpointauthprovider.md)
</dt> <dt>

[<span data-ttu-id="accd8-138">**GetEndpointToken**</span><span class="sxs-lookup"><span data-stu-id="accd8-138">**GetEndpointToken**</span></span>](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




