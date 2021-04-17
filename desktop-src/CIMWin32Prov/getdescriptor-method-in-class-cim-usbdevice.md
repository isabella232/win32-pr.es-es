---
description: El método GetDescriptor devuelve el descriptor de dispositivo USB según lo especificado por los parámetros de entrada.
ms.assetid: 5f36ac8a-e751-4494-b91e-c6733bc3e349
ms.tgt_platform: multiple
title: Método GetDescriptor de la clase CIM_USBDevice (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice.GetDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35ce9a83efb580d6e5e44f55a01182e7390c120e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659480"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-wmcodecdsph"></a><span data-ttu-id="3db6f-103">Método GetDescriptor de la clase CIM_USBDevice (Wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="3db6f-103">GetDescriptor method of the CIM_USBDevice class (Wmcodecdsp.h)</span></span>

<span data-ttu-id="3db6f-104">El método **GetDescriptor** devuelve el descriptor de dispositivo USB según lo especificado por los parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="3db6f-104">The **GetDescriptor** method returns the USB device descriptor as specified by the input parameters.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3db6f-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="3db6f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3db6f-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3db6f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3db6f-107">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="3db6f-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3db6f-108">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3db6f-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3db6f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3db6f-109">Syntax</span></span>


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a><span data-ttu-id="3db6f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3db6f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3db6f-111">*RequestType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3db6f-111">*RequestType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3db6f-112">Identificador de asignación de bits para el tipo de solicitud de descriptor y el destinatario.</span><span class="sxs-lookup"><span data-stu-id="3db6f-112">Bit-mapped identifier for the type of descriptor request and the recipient.</span></span> <span data-ttu-id="3db6f-113">Consulte la especificación USB para ver los valores adecuados para cada bit.</span><span class="sxs-lookup"><span data-stu-id="3db6f-113">Refer to the USB specification for the appropriate values for each bit.</span></span>

</dd> <dt>

<span data-ttu-id="3db6f-114">*RequestValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3db6f-114">*RequestValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3db6f-115">Contiene el tipo de descriptor en el byte alto y el índice de descriptor (por ejemplo, índice o desplazamiento en la matriz de descriptores) en el byte bajo.</span><span class="sxs-lookup"><span data-stu-id="3db6f-115">Contains the descriptor type in the high byte and the descriptor index (for example, index or offset into the descriptor array) in the low byte.</span></span> <span data-ttu-id="3db6f-116">Para obtener más información, consulte la especificación USB.</span><span class="sxs-lookup"><span data-stu-id="3db6f-116">For more information, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="3db6f-117">*RequestIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3db6f-117">*RequestIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3db6f-118">Especifica el código de identificador de idioma de 2 bytes utilizado por el dispositivo USB al devolver los datos del descriptor de cadena.</span><span class="sxs-lookup"><span data-stu-id="3db6f-118">Specifies the 2-byte language identifier code used by the USB device when returning string descriptor data.</span></span> <span data-ttu-id="3db6f-119">El parámetro suele ser 0 (cero) para los descriptores que no son de cadena.</span><span class="sxs-lookup"><span data-stu-id="3db6f-119">The parameter is typically 0 (zero) for nonstring descriptors.</span></span> <span data-ttu-id="3db6f-120">Para obtener más información, consulte la especificación USB.</span><span class="sxs-lookup"><span data-stu-id="3db6f-120">For more information, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="3db6f-121">*RequestLength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3db6f-121">*RequestLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3db6f-122">En la entrada, la longitud (en octetos) del descriptor que se debe devolver.</span><span class="sxs-lookup"><span data-stu-id="3db6f-122">On input, length (in octets) of the descriptor that should be returned.</span></span> <span data-ttu-id="3db6f-123">Si este valor es menor que la longitud real del descriptor, solo se devuelve la longitud solicitada.</span><span class="sxs-lookup"><span data-stu-id="3db6f-123">If this value is less than the actual length of the descriptor, only the requested length is returned.</span></span> <span data-ttu-id="3db6f-124">Si es mayor que la longitud real, se devuelve la longitud real.</span><span class="sxs-lookup"><span data-stu-id="3db6f-124">If it is more than the actual length, the actual length is returned.</span></span>

<span data-ttu-id="3db6f-125">En la salida, la longitud (en octetos) del búfer que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="3db6f-125">On output, the length (in octets) of the buffer being returned.</span></span> <span data-ttu-id="3db6f-126">Si el descriptor solicitado no existe, el contenido de este parámetro es indefinido.</span><span class="sxs-lookup"><span data-stu-id="3db6f-126">If the requested descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="3db6f-127">*Búfer* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3db6f-127">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3db6f-128">Devuelve la información de descriptor solicitada.</span><span class="sxs-lookup"><span data-stu-id="3db6f-128">Returns the requested descriptor information.</span></span> <span data-ttu-id="3db6f-129">Si el descriptor no existe, el contenido de este parámetro es indefinido.</span><span class="sxs-lookup"><span data-stu-id="3db6f-129">If the descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3db6f-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3db6f-130">Return value</span></span>

<span data-ttu-id="3db6f-131">Devuelve un valor de 0 (cero) si el descriptor USB se devuelve correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="3db6f-131">Returns a value of 0 (zero) if the USB descriptor is successfully returned, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span> <span data-ttu-id="3db6f-132">En una subclase, el conjunto de códigos de retorno posibles puede especificarse mediante un calificador **ValueMap** en el método.</span><span class="sxs-lookup"><span data-stu-id="3db6f-132">In a subclass, the set of possible return codes could be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="3db6f-133">Las cadenas a las que se traduce el contenido de mofqualifier también se pueden especificar en la subclase como calificador de matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="3db6f-133">The strings to which the mofqualifier contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="3db6f-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3db6f-134">Remarks</span></span>

<span data-ttu-id="3db6f-135">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="3db6f-135">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="3db6f-136">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="3db6f-136">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="3db6f-137">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="3db6f-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3db6f-138">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="3db6f-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3db6f-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3db6f-139">Requirements</span></span>



| <span data-ttu-id="3db6f-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="3db6f-140">Requirement</span></span> | <span data-ttu-id="3db6f-141">Value</span><span class="sxs-lookup"><span data-stu-id="3db6f-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3db6f-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3db6f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3db6f-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3db6f-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3db6f-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3db6f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3db6f-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3db6f-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3db6f-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3db6f-146">Namespace</span></span><br/>                | <span data-ttu-id="3db6f-147">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3db6f-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3db6f-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3db6f-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="3db6f-149"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3db6f-149"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="3db6f-150">MOF</span><span class="sxs-lookup"><span data-stu-id="3db6f-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3db6f-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3db6f-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3db6f-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3db6f-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3db6f-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3db6f-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3db6f-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="3db6f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3db6f-155">**\_USBDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3db6f-155">**CIM\_USBDevice**</span></span>](getdescriptor-method-in-class-cim-usbdevice.md)
</dt> <dt>

[<span data-ttu-id="3db6f-156">**\_USBDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3db6f-156">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> </dl>

 

