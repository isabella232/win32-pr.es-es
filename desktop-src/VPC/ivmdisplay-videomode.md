---
title: Propiedad VideoMode de IVMDisplay (VPCCOMInterfaces. h)
description: Recupera el modo de vídeo actual.
ms.assetid: e5a090c2-f7e6-4b85-8729-64d2ff68fcf3
keywords:
- Propiedad del modo videocomputadora Virtual PC
- Propiedad VideoMode Virtual PC, interfaz IVMDisplay
- Interfaz IVMDisplay Virtual PC, propiedad VideoMode
topic_type:
- apiref
api_name:
- IVMDisplay.VideoMode
- IVMDisplay.get_VideoMode
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0164a658766cb8973a7c1ac403756ee888abab1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996345"
---
# <a name="ivmdisplayvideomode-property"></a><span data-ttu-id="d445a-106">IVMDisplay:: VideoMode (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d445a-106">IVMDisplay::VideoMode property</span></span>

<span data-ttu-id="d445a-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d445a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d445a-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d445a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d445a-109">Recupera el modo de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="d445a-109">Retrieves the current video mode.</span></span>

<span data-ttu-id="d445a-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d445a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d445a-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d445a-111">Syntax</span></span>


```C++
HRESULT get_VideoMode(
  [out, retval] VMDisplayVideoMode *videoMode
);
```



## <a name="property-value"></a><span data-ttu-id="d445a-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d445a-112">Property value</span></span>

<span data-ttu-id="d445a-113">El modo de vídeo actual del sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="d445a-113">The current video mode of the guest operating system.</span></span> <span data-ttu-id="d445a-114">Para obtener una lista de valores, vea [**VMDisplayVideoMode**](vmdisplayvideomode.md).</span><span class="sxs-lookup"><span data-stu-id="d445a-114">For a list of values, see [**VMDisplayVideoMode**](vmdisplayvideomode.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="d445a-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="d445a-115">Error codes</span></span>



| <span data-ttu-id="d445a-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="d445a-116">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="d445a-117">Significado</span><span class="sxs-lookup"><span data-stu-id="d445a-117">Meaning</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d445a-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d445a-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="d445a-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d445a-119">The operation was successful.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d445a-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d445a-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="d445a-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="d445a-121">The parameter is **NULL**.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d445a-122"><dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="d445a-122"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="d445a-123">La máquina virtual debe estar en ejecución para esta operación.</span><span class="sxs-lookup"><span data-stu-id="d445a-123">The virtual machine must be running for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="d445a-124"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d445a-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="d445a-125">La máquina virtual no es válida o no se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="d445a-125">The virtual machine is not valid or is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="d445a-126"><dt>Máquina virtual \_ E \_ no \_ Mostrar</dt> <dt>0xA0040850</dt></span><span class="sxs-lookup"><span data-stu-id="d445a-126"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>      | <span data-ttu-id="d445a-127">No se puede encontrar una pantalla válida para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d445a-127">Unable to locate a valid display for the virtual machine.</span></span><br/>     |
| <dl> <span data-ttu-id="d445a-128"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d445a-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="d445a-129">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="d445a-129">An unexpected error has occurred.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="d445a-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d445a-130">Requirements</span></span>



| <span data-ttu-id="d445a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d445a-131">Requirement</span></span> | <span data-ttu-id="d445a-132">Value</span><span class="sxs-lookup"><span data-stu-id="d445a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d445a-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d445a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d445a-134">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="d445a-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d445a-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d445a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d445a-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d445a-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d445a-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d445a-137">End of client support</span></span><br/>    | <span data-ttu-id="d445a-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d445a-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d445a-139">Producto</span><span class="sxs-lookup"><span data-stu-id="d445a-139">Product</span></span><br/>                  | <span data-ttu-id="d445a-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d445a-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d445a-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d445a-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="d445a-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d445a-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d445a-143">IID</span><span class="sxs-lookup"><span data-stu-id="d445a-143">IID</span></span><br/>                      | <span data-ttu-id="d445a-144">IID \_ IVMDisplay se define como 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="d445a-144">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="d445a-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="d445a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d445a-146">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="d445a-146">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

