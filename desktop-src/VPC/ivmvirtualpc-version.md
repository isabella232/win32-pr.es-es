---
title: Propiedad de versión IVMVirtualPC (VPCCOMInterfaces. h)
description: Recupera la versión de esta instancia de Windows Virtual PC.
ms.assetid: efcd5e71-8752-45a2-8138-4bc214762f39
keywords:
- Propiedad de versión Virtual PC
- Propiedad version Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, propiedad version
topic_type:
- apiref
api_name:
- IVMVirtualPC.Version
- IVMVirtualPC.get_Version
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0dc84fd714c50c0a0adb3084603aeea2419d3ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493114"
---
# <a name="ivmvirtualpcversion-property"></a><span data-ttu-id="8532c-106">IVMVirtualPC:: version (propiedad)</span><span class="sxs-lookup"><span data-stu-id="8532c-106">IVMVirtualPC::Version property</span></span>

<span data-ttu-id="8532c-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8532c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8532c-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8532c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8532c-109">Recupera la versión de esta instancia de Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="8532c-109">Retrieves the version of this instance of Windows Virtual PC.</span></span>

<span data-ttu-id="8532c-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8532c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8532c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8532c-111">Syntax</span></span>


```C++
HRESULT get_Version(
  [out, retval] BSTR *version
);
```



## <a name="property-value"></a><span data-ttu-id="8532c-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8532c-112">Property value</span></span>

<span data-ttu-id="8532c-113">La versión.</span><span class="sxs-lookup"><span data-stu-id="8532c-113">The version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8532c-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="8532c-114">Error codes</span></span>



| <span data-ttu-id="8532c-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="8532c-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="8532c-116">Significado</span><span class="sxs-lookup"><span data-stu-id="8532c-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8532c-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8532c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="8532c-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8532c-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="8532c-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8532c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="8532c-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="8532c-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="8532c-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8532c-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="8532c-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="8532c-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="8532c-123"><dt>Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="8532c-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="8532c-124">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="8532c-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8532c-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8532c-125">Remarks</span></span>

<span data-ttu-id="8532c-126">La información de versión de Windows Virtual PC se devuelve como un valor de cadena con el siguiente formato: "*v*. *s*. *BBB*. *Tee*", donde *v* es el número de versión principal, *s* es el número de versión secundaria, *BBB* es el número de compilación, *t* es el tipo de compilación (0 = compilación de versión) y *EE* es Server Edition (se = Standard Edition, EE = Enterprise Edition).</span><span class="sxs-lookup"><span data-stu-id="8532c-126">The Windows Virtual PC version information is returned as a string value with the following format: "*v*.*s*.*bbb*.*tee*", where *v* is the major version number, *s* is the minor version number, *bbb* is the build number, *t* is the build type (0 = release build), and *ee* is the server edition (SE = Standard Edition, EE = Enterprise Edition).</span></span>

## <a name="requirements"></a><span data-ttu-id="8532c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8532c-127">Requirements</span></span>



| <span data-ttu-id="8532c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8532c-128">Requirement</span></span> | <span data-ttu-id="8532c-129">Value</span><span class="sxs-lookup"><span data-stu-id="8532c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8532c-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8532c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8532c-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="8532c-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8532c-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8532c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8532c-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8532c-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8532c-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="8532c-134">End of client support</span></span><br/>    | <span data-ttu-id="8532c-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8532c-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8532c-136">Producto</span><span class="sxs-lookup"><span data-stu-id="8532c-136">Product</span></span><br/>                  | <span data-ttu-id="8532c-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8532c-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8532c-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8532c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="8532c-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8532c-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8532c-140">IID</span><span class="sxs-lookup"><span data-stu-id="8532c-140">IID</span></span><br/>                      | <span data-ttu-id="8532c-141">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="8532c-141">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="8532c-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="8532c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8532c-143">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="8532c-143">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

