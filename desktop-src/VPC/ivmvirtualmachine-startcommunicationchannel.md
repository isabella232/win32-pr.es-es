---
title: Método IVMVirtualMachine StartCommunicationChannel (VPCCOMInterfaces. h)
description: Configura un canal de comunicación entre el host y el sistema operativo invitado.
ms.assetid: e4b04aa8-8400-4aa4-ad54-71ef57dec82a
keywords:
- Método StartCommunicationChannel Virtual PC
- Método StartCommunicationChannel Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método StartCommunicationChannel
topic_type:
- apiref
api_name:
- IVMVirtualMachine.StartCommunicationChannel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac6ab73b6a955b6810eaea280dc25732e2a6721
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492215"
---
# <a name="ivmvirtualmachinestartcommunicationchannel-method"></a><span data-ttu-id="a7cad-106">IVMVirtualMachine:: StartCommunicationChannel (método)</span><span class="sxs-lookup"><span data-stu-id="a7cad-106">IVMVirtualMachine::StartCommunicationChannel method</span></span>

<span data-ttu-id="a7cad-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a7cad-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a7cad-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a7cad-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a7cad-109">Configura un canal de comunicación entre el host y el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="a7cad-109">Sets up a communication channel between host and guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7cad-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7cad-110">Syntax</span></span>


```C++
HRESULT StartCommunicationChannel(
  [in] VMEndpointType inHostEndpointType,
  [in] BSTR           inHostEndPointName,
  [in] VMEndpointType inGuestEndpointType,
  [in] BSTR           inGuestEndpointName
);
```



## <a name="parameters"></a><span data-ttu-id="a7cad-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7cad-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7cad-112">*inHostEndpointType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a7cad-112">*inHostEndpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7cad-113">Este parámetro debe ser **vmEndpoint \_ NamedPipe** (0).</span><span class="sxs-lookup"><span data-stu-id="a7cad-113">This parameter must be **vmEndpoint\_NamedPipe** (0).</span></span>

</dd> <dt>

<span data-ttu-id="a7cad-114">*inHostEndPointName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a7cad-114">*inHostEndPointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7cad-115">Nombre único de la canalización.</span><span class="sxs-lookup"><span data-stu-id="a7cad-115">The unique pipe name.</span></span> <span data-ttu-id="a7cad-116">Esta cadena debe tener el formato siguiente: " \\ \\ . \\ canalización \\ *pipename*".</span><span class="sxs-lookup"><span data-stu-id="a7cad-116">This string must have the following form: "\\\\.\\pipe\\*pipename*".</span></span> <span data-ttu-id="a7cad-117">La parte *pipename* del nombre puede incluir cualquier carácter que no sea una barra diagonal inversa, incluidos los números y los caracteres especiales.</span><span class="sxs-lookup"><span data-stu-id="a7cad-117">The *pipename* part of the name can include any character other than a backslash, including numbers and special characters.</span></span> <span data-ttu-id="a7cad-118">Toda la cadena de nombre de canalización puede tener una longitud de hasta 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a7cad-118">The entire pipe name string can be up to 256 characters long.</span></span> <span data-ttu-id="a7cad-119">Los nombres de canalización no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a7cad-119">Pipe names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="a7cad-120">*inGuestEndpointType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a7cad-120">*inGuestEndpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7cad-121">Este parámetro debe ser **vmEndpoint \_ TCPIP** (1).</span><span class="sxs-lookup"><span data-stu-id="a7cad-121">This parameter must be **vmEndpoint\_TCPIP** (1).</span></span>

</dd> <dt>

<span data-ttu-id="a7cad-122">*inGuestEndpointName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a7cad-122">*inGuestEndpointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7cad-123">Número de puerto en el que escucha el servidor TCP en el invitado.</span><span class="sxs-lookup"><span data-stu-id="a7cad-123">The port number on which the TCP server in the guest is listening.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7cad-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7cad-124">Return value</span></span>

<span data-ttu-id="a7cad-125">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="a7cad-125">This method can return one of these values.</span></span>



| <span data-ttu-id="a7cad-126">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7cad-126">Return code/value</span></span>                                                                                                                                                                                  | <span data-ttu-id="a7cad-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7cad-127">Description</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a7cad-128"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a7cad-128"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                        | <span data-ttu-id="a7cad-129">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a7cad-129">The operation was successful.</span></span><br/>                                                                                                                    |
| <dl> <span data-ttu-id="a7cad-130"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="a7cad-130"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                       | <span data-ttu-id="a7cad-131">El parámetro *inHostEndpointType* no es **vmEndpoint \_ NamedPipe** (0) o el parámetro *inGuestEndpointType* no es **vmEndpoint \_ TCPIP** (1).</span><span class="sxs-lookup"><span data-stu-id="a7cad-131">The *inHostEndpointType* parameter is not **vmEndpoint\_NamedPipe** (0) or the *inGuestEndpointType* parameter is not **vmEndpoint\_TCPIP** (1).</span></span><br/> |
| <dl> <span data-ttu-id="a7cad-132"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a7cad-132"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                          | <span data-ttu-id="a7cad-133">El parámetro *inHostEndPointName* o *inGuestEndpointName* es **null** o no es un valor válido.</span><span class="sxs-lookup"><span data-stu-id="a7cad-133">The *inHostEndPointName* or *inGuestEndpointName* parameter is **NULL** or not a valid value.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="a7cad-134"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a7cad-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                                  | <span data-ttu-id="a7cad-135">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="a7cad-135">An unexpected error has occurred.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="a7cad-136"><dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ identificador no válido)**</dt> <dt>0x80070006</dt></span><span class="sxs-lookup"><span data-stu-id="a7cad-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_HANDLE)**</dt> <dt>0x80070006</dt></span></span> </dl>        | <span data-ttu-id="a7cad-137">Un identificador no es válido.</span><span class="sxs-lookup"><span data-stu-id="a7cad-137">A handle is not valid.</span></span><br/>                                                                                                                           |
| <dl> <span data-ttu-id="a7cad-138"><dt>**HRESULT \_ DE \_ Win32 (error \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span><span class="sxs-lookup"><span data-stu-id="a7cad-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>            | <span data-ttu-id="a7cad-139">No hay suficiente memoria disponible para completar esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="a7cad-139">There is not enough memory available to complete this request.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="a7cad-140"><dt>**HRESULT \_ DESDE \_ Win32 (error \_ no \_ preparado)**</dt> <dt>0x80070015</dt></span><span class="sxs-lookup"><span data-stu-id="a7cad-140"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_READY)**</dt> <dt>0x80070015</dt></span></span> </dl>             | <span data-ttu-id="a7cad-141">El sistema subyacente que usa para proporcionar servicios de red se está inicializando actualmente.</span><span class="sxs-lookup"><span data-stu-id="a7cad-141">The underlying system it uses to provide network services is currently being initialized.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="a7cad-142"><dt>**HRESULT \_ DESDE \_ Win32 (error \_ ya \_ existe)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="a7cad-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>        | <span data-ttu-id="a7cad-143">El nombre de la canalización ya está en uso.</span><span class="sxs-lookup"><span data-stu-id="a7cad-143">The pipe name is already in use.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="a7cad-144"><dt>**HRESULT \_ De \_ Win32 ( \_ canalización de errores \_ ocupado)**</dt> <dt>0x800700e7</dt></span><span class="sxs-lookup"><span data-stu-id="a7cad-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PIPE\_BUSY)**</dt> <dt>0x800700e7</dt></span></span> </dl>             | <span data-ttu-id="a7cad-145">Uno o más canales se están ejecutando y pueden estar disponibles en breve.</span><span class="sxs-lookup"><span data-stu-id="a7cad-145">One or more channels are running down and may become available shortly.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="a7cad-146"><dt>**HRESULT \_ Desde \_ Win32 (error \_ máximo de \_ sesiones \_ alcanzadas)**</dt> <dt>0x80070161</dt></span><span class="sxs-lookup"><span data-stu-id="a7cad-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_MAX\_SESSIONS\_REACHED)**</dt> <dt>0x80070161</dt></span></span> </dl> | <span data-ttu-id="a7cad-147">El número máximo de canales de comunicación disponible está en uso.</span><span class="sxs-lookup"><span data-stu-id="a7cad-147">The maximum numbers of communication channels available are in-use.</span></span> <span data-ttu-id="a7cad-148">No se puede iniciar otro canal en este momento.</span><span class="sxs-lookup"><span data-stu-id="a7cad-148">Another channel cannot be started at this time.</span></span><br/>                              |
| <dl> <span data-ttu-id="a7cad-149"><dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ coincidencia de revisión)**</dt> <dt>0x8007051a</dt></span><span class="sxs-lookup"><span data-stu-id="a7cad-149"><dt>**HRESULT\_FROM\_WIN32(ERROR\_REVISION\_MISMATCH)**</dt> <dt>0x8007051a</dt></span></span> </dl>     | <span data-ttu-id="a7cad-150">Hay una discrepancia entre la versión del host y los subsistemas invitados.</span><span class="sxs-lookup"><span data-stu-id="a7cad-150">There is a mismatch between the version of the host and guest subsystems.</span></span> <span data-ttu-id="a7cad-151">Vea el registro de eventos de Windows para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="a7cad-151">See the Windows Event Log for more detail.</span></span><br/>                             |
| <dl> <span data-ttu-id="a7cad-152"><dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="a7cad-152"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                             | <span data-ttu-id="a7cad-153">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="a7cad-153">The VM is not running.</span></span><br/>                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="a7cad-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7cad-154">Remarks</span></span>

<span data-ttu-id="a7cad-155">La implementación actual solo admite la interfaz de canalización con nombre en el host y la interfaz TCP/IP en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="a7cad-155">The current implementation supports only named pipe interface on the host and TCP/IP interface on the guest operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7cad-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7cad-156">Requirements</span></span>



| <span data-ttu-id="a7cad-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7cad-157">Requirement</span></span> | <span data-ttu-id="a7cad-158">Value</span><span class="sxs-lookup"><span data-stu-id="a7cad-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7cad-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7cad-159">Minimum supported client</span></span><br/> | <span data-ttu-id="a7cad-160">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a7cad-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a7cad-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7cad-161">Minimum supported server</span></span><br/> | <span data-ttu-id="a7cad-162">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a7cad-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a7cad-163">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a7cad-163">End of client support</span></span><br/>    | <span data-ttu-id="a7cad-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a7cad-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a7cad-165">Producto</span><span class="sxs-lookup"><span data-stu-id="a7cad-165">Product</span></span><br/>                  | <span data-ttu-id="a7cad-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a7cad-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a7cad-167">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7cad-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7cad-168"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7cad-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a7cad-169">IID</span><span class="sxs-lookup"><span data-stu-id="a7cad-169">IID</span></span><br/>                      | <span data-ttu-id="a7cad-170">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="a7cad-170">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="a7cad-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7cad-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7cad-172">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="a7cad-172">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="a7cad-173">**VMEndpointType**</span><span class="sxs-lookup"><span data-stu-id="a7cad-173">**VMEndpointType**</span></span>](vmendpointtype.md)
</dt> </dl>

 

