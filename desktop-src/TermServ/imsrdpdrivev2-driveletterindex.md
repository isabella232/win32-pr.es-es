---
title: Propiedad DriveLetterIndex de IMsRdpDriveV2
description: Contiene el índice de la letra de la unidad.
ms.assetid: 9091d1c4-b97e-4e4c-9563-5a0b881ec250
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DriveLetterIndex
- Propiedad DriveLetterIndex Servicios de Escritorio remoto, interfaz IMsRdpDriveV2
- Servicios de Escritorio remoto de la interfaz IMsRdpDriveV2, propiedad DriveLetterIndex
topic_type:
- apiref
api_name:
- IMsRdpDriveV2.DriveLetterIndex
- IMsRdpDriveV2.get_DriveLetterIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39284a94950935e2d273483db871a9b08f7daf36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997146"
---
# <a name="imsrdpdrivev2driveletterindex-property"></a><span data-ttu-id="edd8e-106">IMsRdpDriveV2::D propiedad riveLetterIndex</span><span class="sxs-lookup"><span data-stu-id="edd8e-106">IMsRdpDriveV2::DriveLetterIndex property</span></span>

<span data-ttu-id="edd8e-107">Contiene el índice de la letra de la unidad.</span><span class="sxs-lookup"><span data-stu-id="edd8e-107">Contains the index of the letter for the drive.</span></span>

<span data-ttu-id="edd8e-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="edd8e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="edd8e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="edd8e-109">Syntax</span></span>


```C++
HRESULT get_DriveLetterIndex(
  [out, retval] ULONG *pDriveLetterIndex
);
```



## <a name="property-value"></a><span data-ttu-id="edd8e-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="edd8e-110">Property value</span></span>

<span data-ttu-id="edd8e-111">Índice de la letra de la unidad.</span><span class="sxs-lookup"><span data-stu-id="edd8e-111">The index of the letter for the drive.</span></span> <span data-ttu-id="edd8e-112">0 = "A", 1 = "B", etc.</span><span class="sxs-lookup"><span data-stu-id="edd8e-112">0 = "A", 1 = "B", and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="edd8e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edd8e-113">Requirements</span></span>



| <span data-ttu-id="edd8e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="edd8e-114">Requirement</span></span> | <span data-ttu-id="edd8e-115">Value</span><span class="sxs-lookup"><span data-stu-id="edd8e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="edd8e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edd8e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="edd8e-117">Windows 7 con SP1</span><span class="sxs-lookup"><span data-stu-id="edd8e-117">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="edd8e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edd8e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="edd8e-119">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="edd8e-119">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="edd8e-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="edd8e-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="edd8e-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edd8e-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="edd8e-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="edd8e-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edd8e-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edd8e-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edd8e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="edd8e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edd8e-125">**IMsRdpDriveV2**</span><span class="sxs-lookup"><span data-stu-id="edd8e-125">**IMsRdpDriveV2**</span></span>](imsrdpdrivev2.md)
</dt> </dl>

 

 





