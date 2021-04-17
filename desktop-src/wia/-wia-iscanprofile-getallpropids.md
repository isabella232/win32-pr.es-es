---
description: Obtiene todos los identificadores de propiedad disponibles en un perfil.
ms.assetid: 9ef2abdd-0b33-4be3-a124-7795f42d5e55
title: 'IScanProfile:: GetAllPropIDs (método) (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetAllPropIDs
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 34cd00f626bea3b8f1350950f0d2012ce019068e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696622"
---
# <a name="iscanprofilegetallpropids-method"></a><span data-ttu-id="49810-103">IScanProfile:: GetAllPropIDs (método)</span><span class="sxs-lookup"><span data-stu-id="49810-103">IScanProfile::GetAllPropIDs method</span></span>

<span data-ttu-id="49810-104">Obtiene todos los identificadores de propiedad disponibles en un perfil.</span><span class="sxs-lookup"><span data-stu-id="49810-104">Gets all available property IDs in a profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="49810-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49810-105">Syntax</span></span>


```C++
HRESULT GetAllPropIDs(
  [in, out] ULONG  *num,
  [out]     PROPID *ppid
);
```



## <a name="parameters"></a><span data-ttu-id="49810-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49810-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49810-107">*número* \[ de in, out\]</span><span class="sxs-lookup"><span data-stu-id="49810-107">*num* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="49810-108">Tipo: \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="49810-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="49810-109">Número de identificadores de propiedad solicitados o devueltos.</span><span class="sxs-lookup"><span data-stu-id="49810-109">The number of property IDs requested or returned.</span></span>

</dd> <dt>

<span data-ttu-id="49810-110">_ppid \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="49810-110">_ppid\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49810-111">Tipo: \**PROPID \** _</span><span class="sxs-lookup"><span data-stu-id="49810-111">Type: \**PROPID\** _</span></span>

<span data-ttu-id="49810-112">Puntero a una matriz de identificadores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="49810-112">A pointer to an array of property IDs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49810-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49810-113">Return value</span></span>

<span data-ttu-id="49810-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="49810-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="49810-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="49810-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="49810-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="49810-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="49810-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49810-117">Requirements</span></span>



| <span data-ttu-id="49810-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="49810-118">Requirement</span></span> | <span data-ttu-id="49810-119">Value</span><span class="sxs-lookup"><span data-stu-id="49810-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="49810-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49810-120">Minimum supported client</span></span><br/> | <span data-ttu-id="49810-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="49810-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="49810-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49810-122">Minimum supported server</span></span><br/> | <span data-ttu-id="49810-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="49810-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49810-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49810-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="49810-125"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="49810-125"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="49810-126">IDL</span><span class="sxs-lookup"><span data-stu-id="49810-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="49810-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="49810-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49810-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="49810-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49810-129">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="49810-129">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="49810-130">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="49810-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




