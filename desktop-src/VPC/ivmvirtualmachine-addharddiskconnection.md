---
title: Método IVMVirtualMachine AddHardDiskConnection (VPCCOMInterfaces. h)
description: Agrega una nueva conexión de disco duro a la máquina virtual.
ms.assetid: 0f4e0666-2cfd-4c73-884d-6f8b43186c05
keywords:
- Método AddHardDiskConnection Virtual PC
- Método AddHardDiskConnection Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método AddHardDiskConnection
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0111577fd5cab614988e7295f3b8cdd59b8805c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651400"
---
# <a name="ivmvirtualmachineaddharddiskconnection-method"></a><span data-ttu-id="20e6c-106">IVMVirtualMachine:: AddHardDiskConnection (método)</span><span class="sxs-lookup"><span data-stu-id="20e6c-106">IVMVirtualMachine::AddHardDiskConnection method</span></span>

<span data-ttu-id="20e6c-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="20e6c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="20e6c-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="20e6c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="20e6c-109">Agrega una nueva conexión de disco duro a la máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="20e6c-109">Adds a new hard disk connection to the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="20e6c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20e6c-110">Syntax</span></span>


```C++
HRESULT AddHardDiskConnection(
  [in]          BSTR                  hardDiskPath,
  [in]          long                  busNumber,
  [in]          long                  deviceNumber,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="parameters"></a><span data-ttu-id="20e6c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20e6c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20e6c-112">*hardDiskPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="20e6c-112">*hardDiskPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20e6c-113">La ruta de acceso completa del archivo de disco duro virtual (VHD) que se va a conectar.</span><span class="sxs-lookup"><span data-stu-id="20e6c-113">The full path of the virtual hard disk (VHD) file to connect.</span></span>

</dd> <dt>

<span data-ttu-id="20e6c-114">*busNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="20e6c-114">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20e6c-115">El bus al que se conectará la unidad.</span><span class="sxs-lookup"><span data-stu-id="20e6c-115">The bus to which the drive will be attached.</span></span>



| <span data-ttu-id="20e6c-116">Value</span><span class="sxs-lookup"><span data-stu-id="20e6c-116">Value</span></span>                                                                        | <span data-ttu-id="20e6c-117">Significado</span><span class="sxs-lookup"><span data-stu-id="20e6c-117">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="20e6c-118"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="20e6c-118"><dt>0</dt></span></span> </dl> | <span data-ttu-id="20e6c-119">La unidad se conectará al primer bus.</span><span class="sxs-lookup"><span data-stu-id="20e6c-119">The drive will be attached to the first bus.</span></span><br/>  |
| <dl> <span data-ttu-id="20e6c-120"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="20e6c-120"><dt>1</dt></span></span> </dl> | <span data-ttu-id="20e6c-121">La unidad se conectará al segundo bus.</span><span class="sxs-lookup"><span data-stu-id="20e6c-121">The drive will be attached to the second bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="20e6c-122">*deviceNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="20e6c-122">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20e6c-123">El dispositivo al que se conectará la unidad.</span><span class="sxs-lookup"><span data-stu-id="20e6c-123">The device to which the drive will be attached.</span></span>



| <span data-ttu-id="20e6c-124">Value</span><span class="sxs-lookup"><span data-stu-id="20e6c-124">Value</span></span>                                                                        | <span data-ttu-id="20e6c-125">Significado</span><span class="sxs-lookup"><span data-stu-id="20e6c-125">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="20e6c-126"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="20e6c-126"><dt>0</dt></span></span> </dl> | <span data-ttu-id="20e6c-127">La unidad se conectará al primer dispositivo del bus.</span><span class="sxs-lookup"><span data-stu-id="20e6c-127">The drive will be attached to the first device on the bus.</span></span><br/>  |
| <dl> <span data-ttu-id="20e6c-128"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="20e6c-128"><dt>1</dt></span></span> </dl> | <span data-ttu-id="20e6c-129">La unidad se conectará al segundo dispositivo del bus.</span><span class="sxs-lookup"><span data-stu-id="20e6c-129">The drive will be attached to the second device on the bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="20e6c-130">*hardDiskConnection* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="20e6c-130">*hardDiskConnection* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="20e6c-131">Objeto [**IVMHardDiskConnection**](ivmharddiskconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="20e6c-131">An [**IVMHardDiskConnection**](ivmharddiskconnection.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20e6c-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20e6c-132">Return value</span></span>

<span data-ttu-id="20e6c-133">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="20e6c-133">This method can return one of these values.</span></span>



| <span data-ttu-id="20e6c-134">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20e6c-134">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="20e6c-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="20e6c-135">Description</span></span>                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="20e6c-136"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="20e6c-136"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="20e6c-137">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="20e6c-137">The operation was successful.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="20e6c-138"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="20e6c-138"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="20e6c-139">El parámetro *hardDiskConnection* es **null**.</span><span class="sxs-lookup"><span data-stu-id="20e6c-139">The *hardDiskConnection* parameter is **NULL**.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="20e6c-140"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="20e6c-140"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="20e6c-141">Un parámetro *hardDiskPath* es **null** o el parámetro *busNumber* o *deviceNumber* no es válido.</span><span class="sxs-lookup"><span data-stu-id="20e6c-141">A *hardDiskPath* parameter is **NULL** or the *busNumber* or *deviceNumber* parameter is not valid.</span></span><br/>                                            |
| <dl> <span data-ttu-id="20e6c-142"><dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="20e6c-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl>   | <span data-ttu-id="20e6c-143">El sistema no encuentra el archivo especificado por el parámetro *hardDiskPath* .</span><span class="sxs-lookup"><span data-stu-id="20e6c-143">The system cannot find the file specified by the *hardDiskPath* parameter.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="20e6c-144"><dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="20e6c-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="20e6c-145">El sistema no puede encontrar la ruta de acceso especificada por el parámetro *hardDiskPath* .</span><span class="sxs-lookup"><span data-stu-id="20e6c-145">The system cannot find the path specified by the *hardDiskPath* parameter.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="20e6c-146"><dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="20e6c-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="20e6c-147">El parámetro *hardDiskPath* contiene un carácter no válido (uno de " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="20e6c-147">The *hardDiskPath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                                        |
| <dl> <span data-ttu-id="20e6c-148"><dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="20e6c-148"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="20e6c-149">El parámetro *hardDiskPath* especifica una ruta de acceso relativa o vacía.</span><span class="sxs-lookup"><span data-stu-id="20e6c-149">The *hardDiskPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="20e6c-150">Se requiere una ruta de acceso absoluta.</span><span class="sxs-lookup"><span data-stu-id="20e6c-150">An absolute path is required.</span></span><br/>                                                |
| <dl> <span data-ttu-id="20e6c-151"><dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="20e6c-151"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="20e6c-152">La ruta de acceso especificada por el parámetro *hardDiskPath* es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="20e6c-152">The path specified by the *hardDiskPath* parameter is too long.</span></span> <span data-ttu-id="20e6c-153">La ruta de acceso debe tener menos de 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="20e6c-153">The path must be less than 260 characters.</span></span><br/>                                     |
| <dl> <span data-ttu-id="20e6c-154"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="20e6c-154"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                              | <span data-ttu-id="20e6c-155">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="20e6c-155">The configuration is unknown.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="20e6c-156"><dt>**Máquina virtual \_ \_Máquina virtual en \_ ejecución \_ o \_ guardada**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="20e6c-156"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>                   | <span data-ttu-id="20e6c-157">La máquina virtual está en estado en ejecución o guardada.</span><span class="sxs-lookup"><span data-stu-id="20e6c-157">The VM is in a running or saved state.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="20e6c-158"><dt>**Máquina virtual \_ E \_ unidad \_ \_ de bus \_ de disco en \_ uso**</dt> <dt>0xA00400503</dt></span><span class="sxs-lookup"><span data-stu-id="20e6c-158"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl>                | <span data-ttu-id="20e6c-159">La ubicación de bus especificada está en uso.</span><span class="sxs-lookup"><span data-stu-id="20e6c-159">The specified bus location is in use.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="20e6c-160"><dt>**Máquina virtual \_ E 0xA0040682 de \_ \_ \_ archivo HD no válido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="20e6c-160"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="20e6c-161">El VHD es superior a 127 GB y no se puede conectar al bus IDE.</span><span class="sxs-lookup"><span data-stu-id="20e6c-161">The VHD is greater than 127 GB and cannot be connected to the IDE bus.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="20e6c-162"><dt>**Máquina virtual \_ E \_ no compatible con \_ el \_ \_ tipo de disco HD**</dt> <dt>0xA00400686</dt></span><span class="sxs-lookup"><span data-stu-id="20e6c-162"><dt>**VM\_E\_UNSUPPORTED\_HD\_DISK\_TYPE**</dt> <dt>0xA00400686</dt></span></span> </dl>             | <span data-ttu-id="20e6c-163">El parámetro *hardDiskPath* hace referencia a un VHD vinculado o a un disco duro virtual de diferenciación en un VHD vinculado.</span><span class="sxs-lookup"><span data-stu-id="20e6c-163">The *hardDiskPath* parameter refers to a linked VHD or a differencing VHD to a linked VHD.</span></span> <span data-ttu-id="20e6c-164">Los VHD vinculados no se pueden conectar a las máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="20e6c-164">Linked VHDs cannot be attached to virtual machines.</span></span><br/> |
| <dl> <span data-ttu-id="20e6c-165"><dt>**HRESULT \_ De \_ Win32 ( \_ \_ infracción de uso compartido de errores)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="20e6c-165"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="20e6c-166">El disco duro virtual especificado ya está conectado a otra ubicación de bus para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="20e6c-166">The specified VHD is already connected to another bus location for this VM.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="20e6c-167"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="20e6c-167"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="20e6c-168">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="20e6c-168">An unexpected error has occurred.</span></span><br/>                                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="20e6c-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20e6c-169">Remarks</span></span>

<span data-ttu-id="20e6c-170">Solo puede Agregar una nueva conexión de disco duro a una máquina virtual detenida.</span><span class="sxs-lookup"><span data-stu-id="20e6c-170">You can only add a new hard disk connection to a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="20e6c-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20e6c-171">Requirements</span></span>



| <span data-ttu-id="20e6c-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="20e6c-172">Requirement</span></span> | <span data-ttu-id="20e6c-173">Value</span><span class="sxs-lookup"><span data-stu-id="20e6c-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="20e6c-174">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20e6c-174">Minimum supported client</span></span><br/> | <span data-ttu-id="20e6c-175">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="20e6c-175">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="20e6c-176">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20e6c-176">Minimum supported server</span></span><br/> | <span data-ttu-id="20e6c-177">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="20e6c-177">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="20e6c-178">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="20e6c-178">End of client support</span></span><br/>    | <span data-ttu-id="20e6c-179">Windows 7</span><span class="sxs-lookup"><span data-stu-id="20e6c-179">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="20e6c-180">Producto</span><span class="sxs-lookup"><span data-stu-id="20e6c-180">Product</span></span><br/>                  | <span data-ttu-id="20e6c-181">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="20e6c-181">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="20e6c-182">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20e6c-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="20e6c-183"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="20e6c-183"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="20e6c-184">IID</span><span class="sxs-lookup"><span data-stu-id="20e6c-184">IID</span></span><br/>                      | <span data-ttu-id="20e6c-185">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="20e6c-185">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="20e6c-186">Vea también</span><span class="sxs-lookup"><span data-stu-id="20e6c-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20e6c-187">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="20e6c-187">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

