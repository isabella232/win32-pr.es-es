---
title: Método IVMFloppyDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
description: Recibe la notificación de que los medios se han insertado en la unidad. | Método IVMFloppyDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
ms.assetid: 922fca14-8ef6-4d3d-b1b6-72d2ea83e8ef
keywords:
- Método OnMediaInsert Virtual PC
- Método OnMediaInsert Virtual PC, interfaz IVMFloppyDriveEvents
- Interfaz IVMFloppyDriveEvents Virtual PC, método OnMediaInsert
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d607a2f63836ca1cb151e602b2d3b2021f4e3913
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698169"
---
# <a name="ivmfloppydriveeventsonmediainsert-method"></a><span data-ttu-id="26f12-107">IVMFloppyDriveEvents:: OnMediaInsert (método)</span><span class="sxs-lookup"><span data-stu-id="26f12-107">IVMFloppyDriveEvents::OnMediaInsert method</span></span>

<span data-ttu-id="26f12-108">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="26f12-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="26f12-109">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="26f12-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="26f12-110">Recibe la notificación de que los medios se han insertado en la unidad.</span><span class="sxs-lookup"><span data-stu-id="26f12-110">Receives notification that media has been inserted into the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f12-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26f12-111">Syntax</span></span>


```C++
HRESULT OnMediaInsert(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a><span data-ttu-id="26f12-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26f12-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26f12-113">*mediaPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="26f12-113">*mediaPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26f12-114">La letra de unidad del host, o ruta de acceso, a la imagen de disquete.</span><span class="sxs-lookup"><span data-stu-id="26f12-114">The host drive letter, or path, to floppy image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26f12-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26f12-115">Return value</span></span>

<span data-ttu-id="26f12-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="26f12-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="26f12-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="26f12-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="26f12-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26f12-118">Remarks</span></span>

<span data-ttu-id="26f12-119">Se llama a este método cuando se inserta un medio (una imagen de disquete o un disquete en una unidad de host).</span><span class="sxs-lookup"><span data-stu-id="26f12-119">This method is called when media (a floppy disk image or a floppy disk in a host drive) is inserted.</span></span> <span data-ttu-id="26f12-120">El programa cliente debe implementar este método de interfaz para recibir la notificación del \_ evento vmFloppyDriveEvent OnMediaInsert que se origina desde [**IVMFloppyDrive**](ivmfloppydrive.md).</span><span class="sxs-lookup"><span data-stu-id="26f12-120">The client program must implement this interface method to receive notification of the vmFloppyDriveEvent\_OnMediaInsert event originating from [**IVMFloppyDrive**](ivmfloppydrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="26f12-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26f12-121">Requirements</span></span>



| <span data-ttu-id="26f12-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="26f12-122">Requirement</span></span> | <span data-ttu-id="26f12-123">Value</span><span class="sxs-lookup"><span data-stu-id="26f12-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="26f12-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26f12-124">Minimum supported client</span></span><br/> | <span data-ttu-id="26f12-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="26f12-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="26f12-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26f12-126">Minimum supported server</span></span><br/> | <span data-ttu-id="26f12-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="26f12-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="26f12-128">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="26f12-128">End of client support</span></span><br/>    | <span data-ttu-id="26f12-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="26f12-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="26f12-130">Producto</span><span class="sxs-lookup"><span data-stu-id="26f12-130">Product</span></span><br/>                  | <span data-ttu-id="26f12-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="26f12-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="26f12-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26f12-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="26f12-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="26f12-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="26f12-134">IID</span><span class="sxs-lookup"><span data-stu-id="26f12-134">IID</span></span><br/>                      | <span data-ttu-id="26f12-135">DIID \_ IVMFloppyDriveEvents se define como a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span><span class="sxs-lookup"><span data-stu-id="26f12-135">DIID\_IVMFloppyDriveEvents is defined as a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="26f12-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="26f12-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f12-137">**IVMFloppyDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="26f12-137">**IVMFloppyDriveEvents**</span></span>](ivmfloppydriveevents.md)
</dt> </dl>

 

