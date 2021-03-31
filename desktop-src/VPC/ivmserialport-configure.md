---
title: Método de configuración de IVMSerialPort (VPCCOMInterfaces. h)
description: Configura el puerto serie.
ms.assetid: fee2e373-8e7c-4f1d-84d0-f0f187a41e9f
keywords:
- Configurar método virtual PC
- Configurar método virtual PC, interfaz IVMSerialPort
- Interfaz IVMSerialPort Virtual PC, configurar método
topic_type:
- apiref
api_name:
- IVMSerialPort.Configure
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99440263dbf52282b6f3c2756ff7dd76151ff73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079442"
---
# <a name="ivmserialportconfigure-method"></a><span data-ttu-id="d5404-106">IVMSerialPort:: Configure (método)</span><span class="sxs-lookup"><span data-stu-id="d5404-106">IVMSerialPort::Configure method</span></span>

<span data-ttu-id="d5404-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d5404-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d5404-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d5404-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d5404-109">Configura el puerto serie.</span><span class="sxs-lookup"><span data-stu-id="d5404-109">Configures the serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5404-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5404-110">Syntax</span></span>


```C++
HRESULT Configure(
  [in] VMSerialPortType portType,
  [in] BSTR             portName,
  [in] VARIANT_BOOL     vmConnectImmediately
);
```



## <a name="parameters"></a><span data-ttu-id="d5404-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5404-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5404-112">*portType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5404-112">*portType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5404-113">El tipo de puerto serie.</span><span class="sxs-lookup"><span data-stu-id="d5404-113">The type of serial port.</span></span> <span data-ttu-id="d5404-114">Para obtener una lista de valores, vea [**VMSerialPortType**](vmserialporttype.md).</span><span class="sxs-lookup"><span data-stu-id="d5404-114">For a list of values, see [**VMSerialPortType**](vmserialporttype.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5404-115">*portName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5404-115">*portName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5404-116">Nombre del puerto serie.</span><span class="sxs-lookup"><span data-stu-id="d5404-116">The name of the serial port.</span></span> <span data-ttu-id="d5404-117">Por ejemplo, "COM1" para **vmSerialPort \_ denominaba hostport**, "C: \\SerialPort.txt" para **vmSerialPort \_ TextFile** o " \\ \\ *ServerName* \\ Pipe \\ *pipename*" para **vmSerialPort \_ NamedPipe**.</span><span class="sxs-lookup"><span data-stu-id="d5404-117">For example, "COM1" for **vmSerialPort\_HostPort**, "C:\\SerialPort.txt" for **vmSerialPort\_TextFile**, or "\\\\*servername*\\pipe\\*pipename*" for **vmSerialPort\_NamedPipe**.</span></span>

</dd> <dt>

<span data-ttu-id="d5404-118">*vmConnectImmediately* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5404-118">*vmConnectImmediately* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5404-119">**True** si el puerto serie del host debe abrirse inmediatamente cuando se inicia la máquina virtual y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d5404-119">**TRUE** if the host serial port should be opened immediately when the virtual machine is started and **FALSE** otherwise.</span></span> <span data-ttu-id="d5404-120">Se omite si *portType* no es **vmSerialPort \_ denominaba hostport**.</span><span class="sxs-lookup"><span data-stu-id="d5404-120">Ignored if *portType* is not **vmSerialPort\_HostPort**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5404-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5404-121">Return value</span></span>

<span data-ttu-id="d5404-122">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="d5404-122">This method can return one of these values.</span></span>



| <span data-ttu-id="d5404-123">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5404-123">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="d5404-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5404-124">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d5404-125"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d5404-125"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="d5404-126">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d5404-126">The operation was successful.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="d5404-127"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="d5404-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="d5404-128">El parámetro *portType* no es válido.</span><span class="sxs-lookup"><span data-stu-id="d5404-128">The *portType* parameter is not valid.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="d5404-129"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d5404-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="d5404-130">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="d5404-130">An unexpected error has occurred.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="d5404-131"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d5404-131"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="d5404-132">El parámetro *portName* es **null**.</span><span class="sxs-lookup"><span data-stu-id="d5404-132">The *portName* parameter is **NULL**.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="d5404-133"><dt>**HRESULT \_ DE \_ Win32 (error \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span><span class="sxs-lookup"><span data-stu-id="d5404-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>      | <span data-ttu-id="d5404-134">No hay suficiente memoria disponible para completar esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="d5404-134">There is not enough memory available to complete this request.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="d5404-135"><dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="d5404-135"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="d5404-136">La ruta de acceso especificada por el parámetro *portName* es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="d5404-136">The path specified by the *portName* parameter is too long.</span></span> <span data-ttu-id="d5404-137">La ruta de acceso debe ser menor que el número máximo de caracteres de **\_ ruta de acceso** (260).</span><span class="sxs-lookup"><span data-stu-id="d5404-137">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="d5404-138"><dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="d5404-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="d5404-139">El parámetro *portName* contiene un carácter no válido (uno de " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="d5404-139">The *portName* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="d5404-140"><dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="d5404-140"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="d5404-141">El parámetro *portName* especifica una ruta de acceso relativa o vacía.</span><span class="sxs-lookup"><span data-stu-id="d5404-141">The *portName* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="d5404-142">Se requiere una ruta de acceso absoluta.</span><span class="sxs-lookup"><span data-stu-id="d5404-142">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="d5404-143"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d5404-143"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="d5404-144">La configuración de esta máquina virtual no es válida.</span><span class="sxs-lookup"><span data-stu-id="d5404-144">The configuration for this virtual machine is not valid.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="d5404-145"><dt>**Máquina virtual \_ E \_ prefe el \_ \_ valor no válido**</dt> <dt>0xA0040301</dt></span><span class="sxs-lookup"><span data-stu-id="d5404-145"><dt>**VM\_E\_PREF\_ILLEGAL\_VALUE**</dt> <dt>0xA0040301</dt></span></span> </dl>                   | <span data-ttu-id="d5404-146">El puerto especificado ya está en uso.</span><span class="sxs-lookup"><span data-stu-id="d5404-146">The specified port is already in use.</span></span><br/>                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="d5404-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5404-147">Requirements</span></span>



| <span data-ttu-id="d5404-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5404-148">Requirement</span></span> | <span data-ttu-id="d5404-149">Value</span><span class="sxs-lookup"><span data-stu-id="d5404-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5404-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5404-150">Minimum supported client</span></span><br/> | <span data-ttu-id="d5404-151">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5404-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d5404-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5404-152">Minimum supported server</span></span><br/> | <span data-ttu-id="d5404-153">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d5404-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d5404-154">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d5404-154">End of client support</span></span><br/>    | <span data-ttu-id="d5404-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d5404-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d5404-156">Producto</span><span class="sxs-lookup"><span data-stu-id="d5404-156">Product</span></span><br/>                  | <span data-ttu-id="d5404-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d5404-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d5404-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5404-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5404-159"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5404-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d5404-160">IID</span><span class="sxs-lookup"><span data-stu-id="d5404-160">IID</span></span><br/>                      | <span data-ttu-id="d5404-161">IID \_ IVMSerialPort se define como 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="d5404-161">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="d5404-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5404-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5404-163">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="d5404-163">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

