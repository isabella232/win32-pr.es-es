---
title: Método IVMDVDDriveEvents OnMediaEject (VPCCOMInterfaces. h)
description: Recibe la notificación de que se ha expulsado el medio de la unidad. | Método IVMDVDDriveEvents OnMediaEject (VPCCOMInterfaces. h)
ms.assetid: ec90fbce-7123-4bfa-abab-300e916fa089
keywords:
- Método OnMediaEject Virtual PC
- Método OnMediaEject Virtual PC, interfaz IVMDVDDriveEvents
- Interfaz IVMDVDDriveEvents Virtual PC, método OnMediaEject
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b66091dcc6cc5ee28ab6e0cb3d58e3e647e41cb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914353"
---
# <a name="ivmdvddriveeventsonmediaeject-method"></a><span data-ttu-id="06de2-107">IVMDVDDriveEvents:: OnMediaEject (método)</span><span class="sxs-lookup"><span data-stu-id="06de2-107">IVMDVDDriveEvents::OnMediaEject method</span></span>

<span data-ttu-id="06de2-108">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="06de2-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="06de2-109">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="06de2-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="06de2-110">Recibe la notificación de que se ha expulsado el medio de la unidad.</span><span class="sxs-lookup"><span data-stu-id="06de2-110">Receives notification that media has been ejected from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="06de2-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06de2-111">Syntax</span></span>


```C++
HRESULT OnMediaEject(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a><span data-ttu-id="06de2-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06de2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06de2-113">*mediaPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06de2-113">*mediaPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06de2-114">La letra de la unidad del host, o ruta de acceso, a la imagen ISO.</span><span class="sxs-lookup"><span data-stu-id="06de2-114">The host drive letter, or path, to the ISO image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06de2-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06de2-115">Return value</span></span>

<span data-ttu-id="06de2-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="06de2-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="06de2-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="06de2-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="06de2-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06de2-118">Remarks</span></span>

<span data-ttu-id="06de2-119">Se llama a este método cuando se expulsa un medio (una imagen ISO o un disco de una unidad de host).</span><span class="sxs-lookup"><span data-stu-id="06de2-119">This method is called when media (an ISO image or a disc in a host drive) is ejected.</span></span> <span data-ttu-id="06de2-120">El programa cliente debe implementar este método de interfaz para recibir la notificación del \_ evento VmDVDDriveEvent EJECT que se origina desde [**IVMDVDDrive**](ivmdvddrive.md).</span><span class="sxs-lookup"><span data-stu-id="06de2-120">The client program must implement this interface method to receive notification of the vmDVDDriveEvent\_OnEject event originating from [**IVMDVDDrive**](ivmdvddrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="06de2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06de2-121">Requirements</span></span>



| <span data-ttu-id="06de2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="06de2-122">Requirement</span></span> | <span data-ttu-id="06de2-123">Value</span><span class="sxs-lookup"><span data-stu-id="06de2-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="06de2-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06de2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="06de2-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="06de2-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="06de2-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06de2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="06de2-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="06de2-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="06de2-128">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="06de2-128">End of client support</span></span><br/>    | <span data-ttu-id="06de2-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="06de2-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="06de2-130">Producto</span><span class="sxs-lookup"><span data-stu-id="06de2-130">Product</span></span><br/>                  | <span data-ttu-id="06de2-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="06de2-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="06de2-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06de2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="06de2-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="06de2-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="06de2-134">IID</span><span class="sxs-lookup"><span data-stu-id="06de2-134">IID</span></span><br/>                      | <span data-ttu-id="06de2-135">DIID \_ IVMDVDDriveEvents se define como c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span><span class="sxs-lookup"><span data-stu-id="06de2-135">DIID\_IVMDVDDriveEvents is defined as c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="06de2-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="06de2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06de2-137">**IVMDVDDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="06de2-137">**IVMDVDDriveEvents**</span></span>](ivmdvddriveevents.md)
</dt> </dl>

 

