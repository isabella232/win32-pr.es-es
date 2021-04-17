---
title: Propiedad DriveByIndex de IMsRdpDriveCollection
description: Recupera la unidad en el índice especificado.
ms.assetid: 28bb2a44-00ac-4892-881d-fdd3fe6adb6b
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DriveByIndex
- Propiedad DriveByIndex Servicios de Escritorio remoto, interfaz IMsRdpDriveCollection
- Servicios de Escritorio remoto de la interfaz IMsRdpDriveCollection, propiedad DriveByIndex
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveByIndex
- IMsRdpDriveCollection.get_DriveByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2789656b328f9615787ff2cd50a1b69c712a8138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422475"
---
# <a name="imsrdpdrivecollectiondrivebyindex-property"></a><span data-ttu-id="ddba4-106">IMsRdpDriveCollection::D propiedad riveByIndex</span><span class="sxs-lookup"><span data-stu-id="ddba4-106">IMsRdpDriveCollection::DriveByIndex property</span></span>

<span data-ttu-id="ddba4-107">Recupera la unidad en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="ddba4-107">Retrieves the drive at the specified index.</span></span>

<span data-ttu-id="ddba4-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ddba4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddba4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ddba4-109">Syntax</span></span>


```C++
HRESULT get_DriveByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDrive **ppDevice
);
```



## <a name="property-value"></a><span data-ttu-id="ddba4-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ddba4-110">Property value</span></span>

<span data-ttu-id="ddba4-111">Puntero a la interfaz [**IMsRdpDrive**](imsrdpdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="ddba4-111">An [**IMsRdpDrive**](imsrdpdrive.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ddba4-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ddba4-112">Error codes</span></span>

<span data-ttu-id="ddba4-113">Si el método se ejecuta correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="ddba4-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="ddba4-114">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="ddba4-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddba4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddba4-115">Requirements</span></span>



| <span data-ttu-id="ddba4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddba4-116">Requirement</span></span> | <span data-ttu-id="ddba4-117">Value</span><span class="sxs-lookup"><span data-stu-id="ddba4-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddba4-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddba4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ddba4-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ddba4-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="ddba4-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddba4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ddba4-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ddba4-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ddba4-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ddba4-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="ddba4-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddba4-123"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="ddba4-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ddba4-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddba4-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddba4-125"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="ddba4-126">IID</span><span class="sxs-lookup"><span data-stu-id="ddba4-126">IID</span></span><br/>                      | <span data-ttu-id="ddba4-127">IID \_ IMsRdpDriveCollection se define como 7ff17599-da2c-4677-Ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="ddba4-127">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ddba4-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddba4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddba4-129">**IMsRdpDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="ddba4-129">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





