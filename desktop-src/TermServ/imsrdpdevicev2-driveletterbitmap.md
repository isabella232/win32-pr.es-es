---
title: Propiedad DriveLetterBitmap de IMsRdpDeviceV2
description: Contiene un campo de bits que representa una asignación de Letras de unidad incluidas en el dispositivo.
ms.assetid: 13b7c9b9-a97f-4474-b5ad-833abff384f5
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DriveLetterBitmap
- Propiedad DriveLetterBitmap Servicios de Escritorio remoto, interfaz IMsRdpDeviceV2
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceV2, propiedad DriveLetterBitmap
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.DriveLetterBitmap
- IMsRdpDeviceV2.get_DriveLetterBitmap
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d13189415630539ac47d7a0e0a094b7b3212e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801147"
---
# <a name="imsrdpdevicev2driveletterbitmap-property"></a><span data-ttu-id="8a3c8-106">IMsRdpDeviceV2::D propiedad riveLetterBitmap</span><span class="sxs-lookup"><span data-stu-id="8a3c8-106">IMsRdpDeviceV2::DriveLetterBitmap property</span></span>

<span data-ttu-id="8a3c8-107">Contiene un campo de bits que representa una asignación de Letras de unidad incluidas en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a3c8-107">Contains a bitfield that represents a map of drive letters contained within the device.</span></span>

<span data-ttu-id="8a3c8-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8a3c8-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a3c8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a3c8-109">Syntax</span></span>


```C++
HRESULT get_DriveLetterBitmap(
  [out, retval] ULONG *pDriveLetterBitmap
);
```



## <a name="property-value"></a><span data-ttu-id="8a3c8-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8a3c8-110">Property value</span></span>

<span data-ttu-id="8a3c8-111">Un mapa de las letras de unidad incluidas en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a3c8-111">A map of drive letters contained within the device.</span></span> <span data-ttu-id="8a3c8-112">Cada bit del valor representa una letra de unidad.</span><span class="sxs-lookup"><span data-stu-id="8a3c8-112">Each bit in the value represents a drive letter.</span></span> <span data-ttu-id="8a3c8-113">El bit menos significativo representa la letra de unidad "A", el siguiente bit representa la letra de unidad "B", etc.</span><span class="sxs-lookup"><span data-stu-id="8a3c8-113">The least significant bit represents drive letter "A", the next bit represents drive letter "B", and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a3c8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a3c8-114">Requirements</span></span>



| <span data-ttu-id="8a3c8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a3c8-115">Requirement</span></span> | <span data-ttu-id="8a3c8-116">Value</span><span class="sxs-lookup"><span data-stu-id="8a3c8-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a3c8-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a3c8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8a3c8-118">Windows 7 con SP1</span><span class="sxs-lookup"><span data-stu-id="8a3c8-118">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="8a3c8-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a3c8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8a3c8-120">Windows Server 2008 R2 con SP1</span><span class="sxs-lookup"><span data-stu-id="8a3c8-120">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="8a3c8-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8a3c8-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="8a3c8-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a3c8-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8a3c8-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8a3c8-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a3c8-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a3c8-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8a3c8-125">IID</span><span class="sxs-lookup"><span data-stu-id="8a3c8-125">IID</span></span><br/>                      | <span data-ttu-id="8a3c8-126">IID \_ IMsRdpDeviceV2 se define como 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="8a3c8-126">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="8a3c8-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a3c8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a3c8-128">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="8a3c8-128">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





