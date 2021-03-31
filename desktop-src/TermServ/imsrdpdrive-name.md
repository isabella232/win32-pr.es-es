---
title: Propiedad nombre de IMsRdpDrive
description: Recupera el nombre de la unidad.
ms.assetid: 5aabb7df-fd46-48aa-ad1d-51da45495782
ms.tgt_platform: multiple
keywords:
- Propiedad Nombre Servicios de Escritorio remoto
- Propiedad Nombre Servicios de Escritorio remoto, interfaz IMsRdpDrive
- Servicios de Escritorio remoto de la interfaz IMsRdpDrive, propiedad Name
topic_type:
- apiref
api_name:
- IMsRdpDrive.Name
- IMsRdpDrive.get_Name
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38eeb0f6112983f508bb43ba69d721aeb52c314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491632"
---
# <a name="imsrdpdrivename-property"></a><span data-ttu-id="787b0-106">IMsRdpDrive:: Name (propiedad)</span><span class="sxs-lookup"><span data-stu-id="787b0-106">IMsRdpDrive::Name property</span></span>

<span data-ttu-id="787b0-107">Recupera el nombre de la unidad.</span><span class="sxs-lookup"><span data-stu-id="787b0-107">Retrieves the name of the drive.</span></span>

<span data-ttu-id="787b0-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="787b0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="787b0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="787b0-109">Syntax</span></span>


```C++
HRESULT get_Name(
  [out] BSTR *pName
);
```



## <a name="property-value"></a><span data-ttu-id="787b0-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="787b0-110">Property value</span></span>

<span data-ttu-id="787b0-111">El nombre de la unidad.</span><span class="sxs-lookup"><span data-stu-id="787b0-111">The drive name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="787b0-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="787b0-112">Error codes</span></span>

<span data-ttu-id="787b0-113">Si el método se ejecuta correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="787b0-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="787b0-114">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="787b0-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="787b0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="787b0-115">Requirements</span></span>



| <span data-ttu-id="787b0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="787b0-116">Requirement</span></span> | <span data-ttu-id="787b0-117">Value</span><span class="sxs-lookup"><span data-stu-id="787b0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="787b0-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="787b0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="787b0-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="787b0-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="787b0-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="787b0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="787b0-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="787b0-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="787b0-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="787b0-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="787b0-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="787b0-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="787b0-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="787b0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="787b0-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="787b0-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="787b0-126">IID</span><span class="sxs-lookup"><span data-stu-id="787b0-126">IID</span></span><br/>                      | <span data-ttu-id="787b0-127">IID \_ IMsRdpDrive se define como d28b5458-f694-47a8-8e61-40356a767e46</span><span class="sxs-lookup"><span data-stu-id="787b0-127">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="787b0-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="787b0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="787b0-129">**IMsRdpDrive**</span><span class="sxs-lookup"><span data-stu-id="787b0-129">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

 





