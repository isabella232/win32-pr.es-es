---
title: Propiedad IVMDisplay CanResize (VPCCOMInterfaces. h)
description: Determina si el invitado permite cambios de resolución.
ms.assetid: 97f2aad9-aa27-4db2-ac5d-fa9645f0e674
keywords:
- Propiedad CanResize Virtual PC
- Propiedad CanResize Virtual PC, interfaz IVMDisplay
- Interfaz IVMDisplay Virtual PC, propiedad CanResize
topic_type:
- apiref
api_name:
- IVMDisplay.CanResize
- IVMDisplay.get_CanResize
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca865189b1fd155e0edf85bac9a36d94ffe5d656
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803752"
---
# <a name="ivmdisplaycanresize-property"></a><span data-ttu-id="70efa-106">IVMDisplay:: CanResize (propiedad)</span><span class="sxs-lookup"><span data-stu-id="70efa-106">IVMDisplay::CanResize property</span></span>

<span data-ttu-id="70efa-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="70efa-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="70efa-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="70efa-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="70efa-109">Determina si el invitado permite cambios de resolución.</span><span class="sxs-lookup"><span data-stu-id="70efa-109">Determines whether the Guest allows resolution changes.</span></span>

<span data-ttu-id="70efa-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="70efa-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="70efa-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70efa-111">Syntax</span></span>


```C++
HRESULT get_CanResize(
  [out, retval] VARIANT_BOOL *canResize
);
```



## <a name="property-value"></a><span data-ttu-id="70efa-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="70efa-112">Property value</span></span>

<span data-ttu-id="70efa-113">**Variante \_ TRUE** si el invitado permite cambios de resolución y **Variant \_ false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="70efa-113">**VARIANT\_TRUE** if the Guest allows resolution changes and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="70efa-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="70efa-114">Error codes</span></span>



| <span data-ttu-id="70efa-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="70efa-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="70efa-116">Significado</span><span class="sxs-lookup"><span data-stu-id="70efa-116">Meaning</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="70efa-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="70efa-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="70efa-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="70efa-118">The operation was successful.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="70efa-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="70efa-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="70efa-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="70efa-120">The parameter is **NULL**.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="70efa-121"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="70efa-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="70efa-122">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="70efa-122">The configuration is unknown.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="70efa-123"><dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="70efa-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="70efa-124">La máquina virtual debe estar en ejecución para esta operación.</span><span class="sxs-lookup"><span data-stu-id="70efa-124">The virtual machine must be running for this operation.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="70efa-125"><dt>Máquina virtual \_ E \_ no \_ Mostrar</dt> <dt>0xA0040850</dt></span><span class="sxs-lookup"><span data-stu-id="70efa-125"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>                    | <span data-ttu-id="70efa-126">No se encontró ningún dispositivo de vídeo para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="70efa-126">There was no video device found for the virtual machine.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="70efa-127"><dt>Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="70efa-127"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="70efa-128">La característica componentes de integración no está disponible; los componentes de integración no están instalados o la característica se ha deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="70efa-128">The integration components feature is not available; either the integration components are not installed or the feature has been disabled.</span></span><br/> |
| <dl> <span data-ttu-id="70efa-129"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="70efa-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="70efa-130">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="70efa-130">An unexpected error has occurred.</span></span><br/>                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="70efa-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70efa-131">Requirements</span></span>



| <span data-ttu-id="70efa-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="70efa-132">Requirement</span></span> | <span data-ttu-id="70efa-133">Value</span><span class="sxs-lookup"><span data-stu-id="70efa-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="70efa-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70efa-134">Minimum supported client</span></span><br/> | <span data-ttu-id="70efa-135">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="70efa-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="70efa-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70efa-136">Minimum supported server</span></span><br/> | <span data-ttu-id="70efa-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="70efa-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="70efa-138">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="70efa-138">End of client support</span></span><br/>    | <span data-ttu-id="70efa-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="70efa-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="70efa-140">Producto</span><span class="sxs-lookup"><span data-stu-id="70efa-140">Product</span></span><br/>                  | <span data-ttu-id="70efa-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="70efa-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="70efa-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70efa-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="70efa-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="70efa-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="70efa-144">IID</span><span class="sxs-lookup"><span data-stu-id="70efa-144">IID</span></span><br/>                      | <span data-ttu-id="70efa-145">IID \_ IVMDisplay se define como 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="70efa-145">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="70efa-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="70efa-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70efa-147">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="70efa-147">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

