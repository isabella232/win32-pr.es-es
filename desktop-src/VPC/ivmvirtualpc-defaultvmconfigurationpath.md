---
title: Propiedad IVMVirtualPC DefaultVMConfigurationPath (VPCCOMInterfaces. h)
description: Directorio predeterminado en el que se buscarán los archivos de configuración de máquina virtual disponibles.
ms.assetid: 9ae63198-e3f6-4dcb-8edb-85adfbbdca26
keywords:
- Propiedad DefaultVMConfigurationPath Virtual PC
- Propiedad DefaultVMConfigurationPath Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, propiedad DefaultVMConfigurationPath
topic_type:
- apiref
api_name:
- IVMVirtualPC.DefaultVMConfigurationPath
- IVMVirtualPC.get_DefaultVMConfigurationPath
- IVMVirtualPC.put_DefaultVMConfigurationPath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e13fc2323cb15bdbeb8c42e61810a376e49b3988
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803199"
---
# <a name="ivmvirtualpcdefaultvmconfigurationpath-property"></a><span data-ttu-id="3e2d3-106">IVMVirtualPC::D propiedad efaultVMConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="3e2d3-106">IVMVirtualPC::DefaultVMConfigurationPath property</span></span>

<span data-ttu-id="3e2d3-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3e2d3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3e2d3-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3e2d3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3e2d3-109">Recupera y establece el directorio predeterminado en el que se buscarán los archivos de configuración de máquina virtual disponibles.</span><span class="sxs-lookup"><span data-stu-id="3e2d3-109">Retrieves and sets the default directory to be searched for available virtual machine configuration files.</span></span>

<span data-ttu-id="3e2d3-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3e2d3-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e2d3-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e2d3-111">Syntax</span></span>


```C++
HRESULT put_DefaultVMConfigurationPath(
  [in]          BSTR configurationPath
);

HRESULT get_DefaultVMConfigurationPath(
  [out, retval] BSTR *configurationPath
);
```



## <a name="property-value"></a><span data-ttu-id="3e2d3-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3e2d3-112">Property value</span></span>

<span data-ttu-id="3e2d3-113">Especifica la ruta de acceso del directorio para los archivos de configuración de la máquina virtual predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3e2d3-113">Specifies the directory path for the default virtual machine configuration files.</span></span> <span data-ttu-id="3e2d3-114">En la cadena de ruta de acceso, una barra diagonal inversa ( \) puede aparecer inmediatamente antes del carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="3e2d3-114">In the path string, a backslash (\) may appear immediately before the terminating null character.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3e2d3-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="3e2d3-115">Error codes</span></span>



| <span data-ttu-id="3e2d3-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="3e2d3-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="3e2d3-117">Significado</span><span class="sxs-lookup"><span data-stu-id="3e2d3-117">Meaning</span></span>                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e2d3-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3e2d3-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="3e2d3-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3e2d3-119">The operation was successful.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="3e2d3-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3e2d3-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="3e2d3-121">El parámetro *configurationPath* es **null**.</span><span class="sxs-lookup"><span data-stu-id="3e2d3-121">The *configurationPath* parameter is **NULL**.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="3e2d3-122"><dt>HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="3e2d3-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="3e2d3-123">El sistema no puede encontrar el directorio especificado por el parámetro *configurationPath* .</span><span class="sxs-lookup"><span data-stu-id="3e2d3-123">The system cannot find the directory specified by the *configurationPath* parameter.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="3e2d3-124"><dt>HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="3e2d3-124"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="3e2d3-125">El sistema no puede encontrar la ruta de acceso especificada por el parámetro *configurationPath* .</span><span class="sxs-lookup"><span data-stu-id="3e2d3-125">The system cannot find the path specified by the *configurationPath* parameter.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="3e2d3-126"><dt>HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="3e2d3-126"><dt>HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="3e2d3-127">El parámetro *configurationPath* contiene un carácter no válido (uno de los siguientes: " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="3e2d3-127">The *configurationPath* parameter contains an invalid character (one of the following: "\*?<>/\|":").</span></span><br/>                                   |
| <dl> <span data-ttu-id="3e2d3-128"><dt>HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="3e2d3-128"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="3e2d3-129">El parámetro *configurationPath* especifica una ruta de acceso relativa o vacía.</span><span class="sxs-lookup"><span data-stu-id="3e2d3-129">The *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="3e2d3-130">Se requiere una ruta de acceso absoluta.</span><span class="sxs-lookup"><span data-stu-id="3e2d3-130">An absolute path is required.</span></span><br/>                                          |
| <dl> <span data-ttu-id="3e2d3-131"><dt>HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="3e2d3-131"><dt>HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="3e2d3-132">La ruta de acceso especificada por el parámetro *configurationPath* es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="3e2d3-132">The path specified by the *configurationPath* parameter is too long.</span></span> <span data-ttu-id="3e2d3-133">La longitud de la ruta de acceso debe ser menor que el número máximo de caracteres de **\_ ruta de acceso** (260).</span><span class="sxs-lookup"><span data-stu-id="3e2d3-133">The length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="3e2d3-134"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3e2d3-134"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="3e2d3-135">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="3e2d3-135">An unexpected error has occurred.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="3e2d3-136"><dt>Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="3e2d3-136"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="3e2d3-137">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="3e2d3-137">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                          |



## <a name="remarks"></a><span data-ttu-id="3e2d3-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e2d3-138">Remarks</span></span>

<span data-ttu-id="3e2d3-139">De forma predeterminada, este valor de propiedad se establece en el siguiente directorio: "% LocalAppData% \\ Microsoft \\ Windows Virtual PC \\ virtual machines \\ ".</span><span class="sxs-lookup"><span data-stu-id="3e2d3-139">By default, this property value is set to the following directory: "%LocalAppData%\\Microsoft\\Windows Virtual PC\\Virtual Machines\\".</span></span>

## <a name="requirements"></a><span data-ttu-id="3e2d3-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e2d3-140">Requirements</span></span>



| <span data-ttu-id="3e2d3-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e2d3-141">Requirement</span></span> | <span data-ttu-id="3e2d3-142">Value</span><span class="sxs-lookup"><span data-stu-id="3e2d3-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e2d3-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e2d3-143">Minimum supported client</span></span><br/> | <span data-ttu-id="3e2d3-144">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e2d3-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e2d3-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e2d3-145">Minimum supported server</span></span><br/> | <span data-ttu-id="3e2d3-146">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3e2d3-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3e2d3-147">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3e2d3-147">End of client support</span></span><br/>    | <span data-ttu-id="3e2d3-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3e2d3-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3e2d3-149">Producto</span><span class="sxs-lookup"><span data-stu-id="3e2d3-149">Product</span></span><br/>                  | <span data-ttu-id="3e2d3-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3e2d3-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3e2d3-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e2d3-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e2d3-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e2d3-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3e2d3-153">IID</span><span class="sxs-lookup"><span data-stu-id="3e2d3-153">IID</span></span><br/>                      | <span data-ttu-id="3e2d3-154">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="3e2d3-154">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="3e2d3-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e2d3-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e2d3-156">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="3e2d3-156">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

