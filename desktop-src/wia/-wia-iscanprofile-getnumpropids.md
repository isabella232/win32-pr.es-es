---
description: Obtiene el número de identificadores de propiedad de un perfil.
ms.assetid: fa587c8a-8d09-4dfc-938a-5ec8cc9265f5
title: 'IScanProfile:: GetNumPropIDS (método) (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetNumPropIDS
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 13d8d276ca4b849fc1a2ae108369f84354d44361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154876"
---
# <a name="iscanprofilegetnumpropids-method"></a><span data-ttu-id="f29de-103">IScanProfile:: GetNumPropIDS (método)</span><span class="sxs-lookup"><span data-stu-id="f29de-103">IScanProfile::GetNumPropIDS method</span></span>

<span data-ttu-id="f29de-104">Obtiene el número de identificadores de propiedad de un perfil.</span><span class="sxs-lookup"><span data-stu-id="f29de-104">Gets the number of property IDs in a profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="f29de-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f29de-105">Syntax</span></span>


```C++
HRESULT GetNumPropIDS(
  [out] ULONG *num
);
```



## <a name="parameters"></a><span data-ttu-id="f29de-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f29de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f29de-107">*número* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f29de-107">*num* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f29de-108">Tipo: \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="f29de-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="f29de-109">El número de identificadores de propiedad en el perfil.</span><span class="sxs-lookup"><span data-stu-id="f29de-109">The number of property IDs in the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f29de-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f29de-110">Return value</span></span>

<span data-ttu-id="f29de-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f29de-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f29de-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f29de-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f29de-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f29de-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f29de-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f29de-114">Requirements</span></span>



| <span data-ttu-id="f29de-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f29de-115">Requirement</span></span> | <span data-ttu-id="f29de-116">Value</span><span class="sxs-lookup"><span data-stu-id="f29de-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f29de-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f29de-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f29de-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f29de-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f29de-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f29de-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f29de-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f29de-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f29de-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f29de-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f29de-122"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="f29de-122"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="f29de-123">IDL</span><span class="sxs-lookup"><span data-stu-id="f29de-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f29de-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f29de-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f29de-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f29de-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f29de-126">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="f29de-126">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="f29de-127">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="f29de-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




