---
title: Método IVMDisplay SetDimensions (VPCCOMInterfaces. h)
description: Establece el alto y el ancho de la pantalla de la máquina virtual, en píxeles.
ms.assetid: 8ad5cfc4-59b4-4327-b088-d54adf9c6fda
keywords:
- Método SetDimensions Virtual PC
- Método SetDimensions Virtual PC, interfaz IVMDisplay
- Interfaz IVMDisplay Virtual PC, método SetDimensions
topic_type:
- apiref
api_name:
- IVMDisplay.SetDimensions
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4730d73e06074714c8e6ed31fda992259d5c19ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676911"
---
# <a name="ivmdisplaysetdimensions-method"></a><span data-ttu-id="99743-106">IVMDisplay:: SetDimensions (método)</span><span class="sxs-lookup"><span data-stu-id="99743-106">IVMDisplay::SetDimensions method</span></span>

<span data-ttu-id="99743-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="99743-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="99743-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="99743-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="99743-109">Establece el alto y el ancho de la pantalla (VM) de la máquina virtual, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="99743-109">Sets the height and width of the virtual machine's (VM's) display, in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="99743-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99743-110">Syntax</span></span>


```C++
HRESULT SetDimensions(
  [in] long displayPixelWidth,
  [in] long displayPixelHeight
);
```



## <a name="parameters"></a><span data-ttu-id="99743-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99743-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99743-112">*displayPixelWidth* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99743-112">*displayPixelWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99743-113">Ancho, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="99743-113">The width, in pixels.</span></span> <span data-ttu-id="99743-114">El valor debe estar entre los valores 640 y 2048.</span><span class="sxs-lookup"><span data-stu-id="99743-114">The value must be between the values of 640 and 2048.</span></span> <span data-ttu-id="99743-115">Si el valor no es divisible por 8, se reducirá al siguiente múltiplo inferior de 8.</span><span class="sxs-lookup"><span data-stu-id="99743-115">If the value is not evenly divisible by 8, then it will be reduced to the next lower multiple of 8.</span></span>

</dd> <dt>

<span data-ttu-id="99743-116">*displayPixelHeight* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99743-116">*displayPixelHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99743-117">Alto, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="99743-117">The height, in pixels.</span></span> <span data-ttu-id="99743-118">El valor debe estar entre los valores 480 y 1920.</span><span class="sxs-lookup"><span data-stu-id="99743-118">The value must be between the values of 480 and 1920.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99743-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99743-119">Return value</span></span>

<span data-ttu-id="99743-120">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="99743-120">This method can return one of these values.</span></span>



| <span data-ttu-id="99743-121">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99743-121">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="99743-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="99743-122">Description</span></span>                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="99743-123"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="99743-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="99743-124">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="99743-124">The operation was successful.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="99743-125"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="99743-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="99743-126">El parámetro *displayPixelWidth* no es divisible de forma uniforme por 8 o el parámetro *displayPixelWidth* o *displayPixelHeight* está fuera de los valores mínimo permitido (640x480) o máximo 2048x1920).</span><span class="sxs-lookup"><span data-stu-id="99743-126">The *displayPixelWidth* parameter is not evenly divisible by 8 or the *displayPixelWidth* or *displayPixelHeight* parameter is outside of the allowed minimum (640x480) or maximum 2048x1920) values.</span></span><br/> |
| <dl> <span data-ttu-id="99743-127"><dt>**Máquina virtual \_ 0xA0040202 \_ agotó el tiempo de \_ espera**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="99743-127"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="99743-128">El cambio de resolución no finalizó a tiempo.</span><span class="sxs-lookup"><span data-stu-id="99743-128">The resolution change did not finish in a timely manner.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="99743-129"><dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="99743-129"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="99743-130">La máquina virtual debe estar en ejecución para esta operación.</span><span class="sxs-lookup"><span data-stu-id="99743-130">The virtual machine must be running for this operation.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="99743-131"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="99743-131"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="99743-132">La máquina virtual no es válida o no se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="99743-132">The virtual machine is not valid or is not currently running.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="99743-133"><dt>**Máquina virtual \_ E \_ no \_ Mostrar**</dt> <dt>0xA0040850</dt></span><span class="sxs-lookup"><span data-stu-id="99743-133"><dt>**VM\_E\_NO\_DISPLAY**</dt> <dt>0xA0040850</dt></span></span> </dl>                    | <span data-ttu-id="99743-134">No se puede encontrar una presentación válida para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="99743-134">Unable to locate a valid display for the VM.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="99743-135"><dt>**Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="99743-135"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="99743-136">La versión de los componentes de integración instalados en el sistema operativo invitado no admite esta operación.</span><span class="sxs-lookup"><span data-stu-id="99743-136">The version of the integration components installed in the guest operating system does not support this operation.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="99743-137"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="99743-137"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="99743-138">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="99743-138">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="99743-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99743-139">Remarks</span></span>

<span data-ttu-id="99743-140">El tamaño mínimo de la pantalla de la máquina virtual es 640 x 480 píxeles.</span><span class="sxs-lookup"><span data-stu-id="99743-140">The minimum size of the virtual machine's display is 640 x 480 pixels.</span></span> <span data-ttu-id="99743-141">El tamaño máximo es 2048 x 1920.</span><span class="sxs-lookup"><span data-stu-id="99743-141">The maximum size is 2048 x 1920.</span></span> <span data-ttu-id="99743-142">Los intentos de establecer el tamaño de la pantalla en valores fuera de estos límites, o en cualquier ancho que no sea divisible uniformemente por 8, darán lugar a que se devuelva un error de **E \_ INVALIDARG** .</span><span class="sxs-lookup"><span data-stu-id="99743-142">Attempts to set the display size to values outside these limits, or to any width not evenly divisible by 8, will result in an **E\_INVALIDARG** error being returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="99743-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99743-143">Requirements</span></span>



| <span data-ttu-id="99743-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="99743-144">Requirement</span></span> | <span data-ttu-id="99743-145">Value</span><span class="sxs-lookup"><span data-stu-id="99743-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="99743-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99743-146">Minimum supported client</span></span><br/> | <span data-ttu-id="99743-147">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="99743-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="99743-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99743-148">Minimum supported server</span></span><br/> | <span data-ttu-id="99743-149">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="99743-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="99743-150">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="99743-150">End of client support</span></span><br/>    | <span data-ttu-id="99743-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="99743-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="99743-152">Producto</span><span class="sxs-lookup"><span data-stu-id="99743-152">Product</span></span><br/>                  | <span data-ttu-id="99743-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="99743-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="99743-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99743-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="99743-155"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="99743-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="99743-156">IID</span><span class="sxs-lookup"><span data-stu-id="99743-156">IID</span></span><br/>                      | <span data-ttu-id="99743-157">IID \_ IVMDisplay se define como 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="99743-157">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="99743-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="99743-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99743-159">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="99743-159">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

