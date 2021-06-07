---
title: Propiedad IVMVirtualPC DefaultVMConfigurationPath (VPCCOMInterfaces.h)
description: Directorio predeterminado en el que se buscarán los archivos de configuración de máquina virtual disponibles.
ms.assetid: 9ae63198-e3f6-4dcb-8edb-85adfbbdca26
keywords:
- Equipo virtual de la propiedad DefaultVMConfigurationPath
- Propiedad DefaultVMConfigurationPath De PC virtual, interfaz IVMVirtualPC
- IVMVirtualPC interface Virtual PC , Propiedad DefaultVMConfigurationPath
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
ms.openlocfilehash: 09f6370dfb868ec386e05f361240a74412f13a7d
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387641"
---
# <a name="ivmvirtualpcdefaultvmconfigurationpath-property"></a><span data-ttu-id="9b08d-106">IVMVirtualPC::D efaultVMConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="9b08d-106">IVMVirtualPC::DefaultVMConfigurationPath property</span></span>

<span data-ttu-id="9b08d-107">\[Windows Virtual PC ya no está disponible para su uso a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9b08d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9b08d-108">En su lugar, use el proveedor WMI de [Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]</span><span class="sxs-lookup"><span data-stu-id="9b08d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9b08d-109">Recupera y establece el directorio predeterminado en el que se buscarán los archivos de configuración de máquina virtual disponibles.</span><span class="sxs-lookup"><span data-stu-id="9b08d-109">Retrieves and sets the default directory to be searched for available virtual machine configuration files.</span></span>

<span data-ttu-id="9b08d-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="9b08d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b08d-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b08d-111">Syntax</span></span>


```C++
HRESULT put_DefaultVMConfigurationPath(
  [in]          BSTR configurationPath
);

HRESULT get_DefaultVMConfigurationPath(
  [out, retval] BSTR *configurationPath
);
```



## <a name="property-value"></a><span data-ttu-id="9b08d-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9b08d-112">Property value</span></span>

<span data-ttu-id="9b08d-113">Especifica la ruta de acceso del directorio para los archivos de configuración de máquina virtual predeterminados.</span><span class="sxs-lookup"><span data-stu-id="9b08d-113">Specifies the directory path for the default virtual machine configuration files.</span></span> <span data-ttu-id="9b08d-114">En la cadena de ruta de acceso, puede aparecer una barra diagonal inversa ( \\ ) inmediatamente antes del carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="9b08d-114">In the path string, a backslash (\\) may appear immediately before the terminating null character.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9b08d-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="9b08d-115">Error codes</span></span>



| <span data-ttu-id="9b08d-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="9b08d-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="9b08d-117">Significado</span><span class="sxs-lookup"><span data-stu-id="9b08d-117">Meaning</span></span>                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9b08d-118"><dt>S \_ Ok</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9b08d-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="9b08d-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="9b08d-119">The operation was successful.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="9b08d-120"><dt>E \_ Puntero</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="9b08d-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="9b08d-121">El *parámetro configurationPath* es **NULL.**</span><span class="sxs-lookup"><span data-stu-id="9b08d-121">The *configurationPath* parameter is **NULL**.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="9b08d-122"><dt>HRESULT \_ DESDE \_ WIN32(ARCHIVO DE ERROR \_ \_ NO \_ ENCONTRADO)</dt> <dt>0X80070002</dt></span><span class="sxs-lookup"><span data-stu-id="9b08d-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="9b08d-123">El sistema no puede encontrar el directorio especificado por el *parámetro configurationPath.*</span><span class="sxs-lookup"><span data-stu-id="9b08d-123">The system cannot find the directory specified by the *configurationPath* parameter.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="9b08d-124"><dt>HRESULT \_ DESDE \_ WIN32(RUTA DE ACCESO DE ERROR \_ \_ NO \_ ENCONTRADA)</dt> <dt>0X80070003</dt></span><span class="sxs-lookup"><span data-stu-id="9b08d-124"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="9b08d-125">El sistema no puede encontrar la ruta de acceso especificada por el *parámetro configurationPath.*</span><span class="sxs-lookup"><span data-stu-id="9b08d-125">The system cannot find the path specified by the *configurationPath* parameter.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="9b08d-126"><dt>HRESULT \_ DESDE \_ WIN32(ERROR \_ NOMBRE NO \_ VÁLIDO)</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="9b08d-126"><dt>HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="9b08d-127">El *parámetro configurationPath* contiene un carácter no válido (uno de los siguientes: " \* ?<>/ \| ":").</span><span class="sxs-lookup"><span data-stu-id="9b08d-127">The *configurationPath* parameter contains an invalid character (one of the following: "\*?<>/\|":").</span></span><br/>                                   |
| <dl> <span data-ttu-id="9b08d-128"><dt>HRESULT \_ DESDE \_ WIN32(ERROR \_ BAD \_ PATHNAME)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="9b08d-128"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="9b08d-129">El *parámetro configurationPath* especifica una ruta de acceso vacía o relativa.</span><span class="sxs-lookup"><span data-stu-id="9b08d-129">The *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="9b08d-130">Se requiere una ruta de acceso absoluta.</span><span class="sxs-lookup"><span data-stu-id="9b08d-130">An absolute path is required.</span></span><br/>                                          |
| <dl> <span data-ttu-id="9b08d-131"><dt>HRESULT \_ DESDE \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="9b08d-131"><dt>HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="9b08d-132">La ruta de acceso especificada por el *parámetro configurationPath* es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="9b08d-132">The path specified by the *configurationPath* parameter is too long.</span></span> <span data-ttu-id="9b08d-133">La longitud de la ruta de acceso debe ser inferior a **MAX \_ PATH** (260) caracteres.</span><span class="sxs-lookup"><span data-stu-id="9b08d-133">The length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="9b08d-134"><dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="9b08d-134"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="9b08d-135">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="9b08d-135">An unexpected error has occurred.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="9b08d-136"><dt>Máquina virtual \_ E \_ \_ VIRTUALIZACIÓN DE HARDWARE \_ DESHABILITADA</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="9b08d-136"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="9b08d-137">El procesador no admite extensiones de virtualización acelerada de hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="9b08d-137">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                          |



## <a name="remarks"></a><span data-ttu-id="9b08d-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9b08d-138">Remarks</span></span>

<span data-ttu-id="9b08d-139">De forma predeterminada, este valor de propiedad se establece en el directorio siguiente: "%LocalAppData% \\ Microsoft Windows Virtual PC \\ \\ \\ Virtual Machines".</span><span class="sxs-lookup"><span data-stu-id="9b08d-139">By default, this property value is set to the following directory: "%LocalAppData%\\Microsoft\\Windows Virtual PC\\Virtual Machines\\".</span></span>

## <a name="requirements"></a><span data-ttu-id="9b08d-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b08d-140">Requirements</span></span>



| <span data-ttu-id="9b08d-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b08d-141">Requirement</span></span> | <span data-ttu-id="9b08d-142">Valor</span><span class="sxs-lookup"><span data-stu-id="9b08d-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b08d-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b08d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="9b08d-144">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b08d-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9b08d-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b08d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="9b08d-146">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9b08d-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9b08d-147">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="9b08d-147">End of client support</span></span><br/>    | <span data-ttu-id="9b08d-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9b08d-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9b08d-149">Producto</span><span class="sxs-lookup"><span data-stu-id="9b08d-149">Product</span></span><br/>                  | <span data-ttu-id="9b08d-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9b08d-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9b08d-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b08d-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b08d-152"><dt>VPCCOMInterfaces.h</dt></span><span class="sxs-lookup"><span data-stu-id="9b08d-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9b08d-153">IID</span><span class="sxs-lookup"><span data-stu-id="9b08d-153">IID</span></span><br/>                      | <span data-ttu-id="9b08d-154">IID IVMVirtualPC se define como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="9b08d-154">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="9b08d-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b08d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b08d-156">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="9b08d-156">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

