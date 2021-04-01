---
description: Obtiene el nombre descriptivo del perfil.
ms.assetid: db2f8229-ce43-4608-af3f-a06011b4fac0
title: 'IScanProfile:: GetName (método) (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 81d1a0293802ea137f4e23b4571d32fd3d54ee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275638"
---
# <a name="iscanprofilegetname-method"></a><span data-ttu-id="7fa5f-103">IScanProfile:: GetName (método)</span><span class="sxs-lookup"><span data-stu-id="7fa5f-103">IScanProfile::GetName method</span></span>

<span data-ttu-id="7fa5f-104">Obtiene el nombre descriptivo del perfil.</span><span class="sxs-lookup"><span data-stu-id="7fa5f-104">Gets the friendly name of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fa5f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7fa5f-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a><span data-ttu-id="7fa5f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fa5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fa5f-107">*pbstrName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7fa5f-107">*pbstrName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fa5f-108">Tipo: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="7fa5f-108">Type: \**BSTR\** _</span></span>

<span data-ttu-id="7fa5f-109">Nombre descriptivo del perfil.</span><span class="sxs-lookup"><span data-stu-id="7fa5f-109">The friendly name of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fa5f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7fa5f-110">Return value</span></span>

<span data-ttu-id="7fa5f-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="7fa5f-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="7fa5f-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="7fa5f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7fa5f-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7fa5f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fa5f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fa5f-114">Remarks</span></span>

<span data-ttu-id="7fa5f-115">Este método es necesario porque el GUID de un perfil no se puede usar para mostrar el perfil de digitalización a un usuario.</span><span class="sxs-lookup"><span data-stu-id="7fa5f-115">This method is required because the GUID of a profile cannot be used to display the scan profile to a user.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fa5f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fa5f-116">Requirements</span></span>



| <span data-ttu-id="7fa5f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fa5f-117">Requirement</span></span> | <span data-ttu-id="7fa5f-118">Value</span><span class="sxs-lookup"><span data-stu-id="7fa5f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fa5f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fa5f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7fa5f-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7fa5f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="7fa5f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fa5f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7fa5f-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7fa5f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7fa5f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7fa5f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fa5f-124"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fa5f-124"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="7fa5f-125">IDL</span><span class="sxs-lookup"><span data-stu-id="7fa5f-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7fa5f-126"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7fa5f-126"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fa5f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fa5f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fa5f-128">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="7fa5f-128">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="7fa5f-129">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="7fa5f-129">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




