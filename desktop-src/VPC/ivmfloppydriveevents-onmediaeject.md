---
title: Método IVMFloppyDriveEvents OnMediaEject (VPCCOMInterfaces. h)
description: Recibe la notificación de que se ha expulsado el medio de la unidad. | Método IVMFloppyDriveEvents OnMediaEject (VPCCOMInterfaces. h)
ms.assetid: 3e9c0b5d-8fec-4f34-93d2-c5975403798b
keywords:
- Método OnMediaEject Virtual PC
- Método OnMediaEject Virtual PC, interfaz IVMFloppyDriveEvents
- Interfaz IVMFloppyDriveEvents Virtual PC, método OnMediaEject
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd640f7b8eb143eba4f3b19e984792f2b6779ad6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914673"
---
# <a name="ivmfloppydriveeventsonmediaeject-method"></a><span data-ttu-id="57d2b-107">IVMFloppyDriveEvents:: OnMediaEject (método)</span><span class="sxs-lookup"><span data-stu-id="57d2b-107">IVMFloppyDriveEvents::OnMediaEject method</span></span>

<span data-ttu-id="57d2b-108">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="57d2b-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="57d2b-109">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="57d2b-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="57d2b-110">Recibe la notificación de que se ha expulsado el medio de la unidad.</span><span class="sxs-lookup"><span data-stu-id="57d2b-110">Receives notification that media has been ejected from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="57d2b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57d2b-111">Syntax</span></span>


```C++
HRESULT OnMediaEject(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a><span data-ttu-id="57d2b-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57d2b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57d2b-113">*mediaPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="57d2b-113">*mediaPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57d2b-114">La letra de unidad del host, o ruta de acceso, a la imagen de disquete.</span><span class="sxs-lookup"><span data-stu-id="57d2b-114">The host drive letter, or path, to floppy image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57d2b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57d2b-115">Return value</span></span>

<span data-ttu-id="57d2b-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="57d2b-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="57d2b-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="57d2b-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="57d2b-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57d2b-118">Remarks</span></span>

<span data-ttu-id="57d2b-119">Se llama a este método cuando se expulsa un medio (una imagen de disquete o un disquete en una unidad de host).</span><span class="sxs-lookup"><span data-stu-id="57d2b-119">This method is called when media (a floppy disk image or a floppy disk in a host drive) is ejected.</span></span> <span data-ttu-id="57d2b-120">El programa cliente debe implementar este método de interfaz para recibir la notificación del \_ evento vmFloppyDriveEvent OnMediaEject que se origina desde [**IVMFloppyDrive**](ivmfloppydrive.md).</span><span class="sxs-lookup"><span data-stu-id="57d2b-120">The client program must implement this interface method to receive notification of the vmFloppyDriveEvent\_OnMediaEject event originating from [**IVMFloppyDrive**](ivmfloppydrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="57d2b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57d2b-121">Requirements</span></span>



| <span data-ttu-id="57d2b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="57d2b-122">Requirement</span></span> | <span data-ttu-id="57d2b-123">Value</span><span class="sxs-lookup"><span data-stu-id="57d2b-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="57d2b-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57d2b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="57d2b-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="57d2b-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="57d2b-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57d2b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="57d2b-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="57d2b-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="57d2b-128">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="57d2b-128">End of client support</span></span><br/>    | <span data-ttu-id="57d2b-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="57d2b-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="57d2b-130">Producto</span><span class="sxs-lookup"><span data-stu-id="57d2b-130">Product</span></span><br/>                  | <span data-ttu-id="57d2b-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="57d2b-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="57d2b-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57d2b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="57d2b-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="57d2b-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="57d2b-134">IID</span><span class="sxs-lookup"><span data-stu-id="57d2b-134">IID</span></span><br/>                      | <span data-ttu-id="57d2b-135">DIID \_ IVMFloppyDriveEvents se define como a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span><span class="sxs-lookup"><span data-stu-id="57d2b-135">DIID\_IVMFloppyDriveEvents is defined as a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="57d2b-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="57d2b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57d2b-137">**IVMFloppyDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="57d2b-137">**IVMFloppyDriveEvents**</span></span>](ivmfloppydriveevents.md)
</dt> </dl>

 

