---
title: Método IVMDVDDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
description: Recibe la notificación de que los medios se han insertado en la unidad. | Método IVMDVDDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
ms.assetid: a246e2dd-638e-4d2f-9089-74771cd8bb2b
keywords:
- Método OnMediaInsert Virtual PC
- Método OnMediaInsert Virtual PC, interfaz IVMDVDDriveEvents
- Interfaz IVMDVDDriveEvents Virtual PC, método OnMediaInsert
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 883f7990de17a9d1dbb21db9651e0f5ad4ec74aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003524"
---
# <a name="ivmdvddriveeventsonmediainsert-method"></a><span data-ttu-id="c2cd3-107">IVMDVDDriveEvents:: OnMediaInsert (método)</span><span class="sxs-lookup"><span data-stu-id="c2cd3-107">IVMDVDDriveEvents::OnMediaInsert method</span></span>

<span data-ttu-id="c2cd3-108">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c2cd3-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c2cd3-109">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c2cd3-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c2cd3-110">Recibe la notificación de que los medios se han insertado en la unidad.</span><span class="sxs-lookup"><span data-stu-id="c2cd3-110">Receives notification that media has been inserted into the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2cd3-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2cd3-111">Syntax</span></span>


```C++
HRESULT OnMediaInsert(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a><span data-ttu-id="c2cd3-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2cd3-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2cd3-113">*mediaPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c2cd3-113">*mediaPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2cd3-114">La letra de la unidad del host, o ruta de acceso, a la imagen ISO.</span><span class="sxs-lookup"><span data-stu-id="c2cd3-114">The host drive letter, or path, to the ISO image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2cd3-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2cd3-115">Return value</span></span>

<span data-ttu-id="c2cd3-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c2cd3-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c2cd3-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c2cd3-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2cd3-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2cd3-118">Remarks</span></span>

<span data-ttu-id="c2cd3-119">Se llama a este método cuando se inserta un medio (una imagen ISO o un disco en una unidad de host).</span><span class="sxs-lookup"><span data-stu-id="c2cd3-119">This method is called when media (an ISO image or a disc in a host drive) is inserted.</span></span> <span data-ttu-id="c2cd3-120">El programa cliente debe implementar este método de interfaz para recibir la notificación del \_ evento vmDVDDriveEvent alinsert que se origina desde [**IVMDVDDrive**](ivmdvddrive.md).</span><span class="sxs-lookup"><span data-stu-id="c2cd3-120">The client program must implement this interface method to receive notification of the vmDVDDriveEvent\_OnInsert event originating from [**IVMDVDDrive**](ivmdvddrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2cd3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2cd3-121">Requirements</span></span>



| <span data-ttu-id="c2cd3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2cd3-122">Requirement</span></span> | <span data-ttu-id="c2cd3-123">Value</span><span class="sxs-lookup"><span data-stu-id="c2cd3-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2cd3-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2cd3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c2cd3-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c2cd3-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c2cd3-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2cd3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c2cd3-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c2cd3-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c2cd3-128">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="c2cd3-128">End of client support</span></span><br/>    | <span data-ttu-id="c2cd3-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c2cd3-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c2cd3-130">Producto</span><span class="sxs-lookup"><span data-stu-id="c2cd3-130">Product</span></span><br/>                  | <span data-ttu-id="c2cd3-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c2cd3-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c2cd3-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2cd3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2cd3-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2cd3-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c2cd3-134">IID</span><span class="sxs-lookup"><span data-stu-id="c2cd3-134">IID</span></span><br/>                      | <span data-ttu-id="c2cd3-135">DIID \_ IVMDVDDriveEvents se define como c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span><span class="sxs-lookup"><span data-stu-id="c2cd3-135">DIID\_IVMDVDDriveEvents is defined as c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="c2cd3-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2cd3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2cd3-137">**IVMDVDDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="c2cd3-137">**IVMDVDDriveEvents**</span></span>](ivmdvddriveevents.md)
</dt> </dl>

 

