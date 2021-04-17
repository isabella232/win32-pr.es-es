---
description: Devuelve el descriptor de USBDevice tal y como lo especifican los parámetros de entrada.
ms.assetid: 89bb8a49-6fca-422c-808d-70ae77aae4c3
title: Método GetDescriptor de la clase CIM_USBDevice (administración de Hyper-V)
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
- vmms.exe
ms.openlocfilehash: f6aa8e7dc37f2bb7fe48ce0293bbaad9663150dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666904"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-hyper-v-management"></a><span data-ttu-id="b7aba-103">Método GetDescriptor de la clase CIM_USBDevice (administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="b7aba-103">GetDescriptor method of the CIM_USBDevice class (Hyper-V management)</span></span>

<span data-ttu-id="b7aba-104">Devuelve el descriptor de USBDevice tal y como lo especifican los parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="b7aba-104">Returns the USBDevice descriptor as specified by the input parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7aba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7aba-105">Syntax</span></span>


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a><span data-ttu-id="b7aba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7aba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7aba-107">*RequestType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b7aba-107">*RequestType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7aba-108">Mapa de bits que identifica el tipo de solicitud de descriptor y el destinatario.</span><span class="sxs-lookup"><span data-stu-id="b7aba-108">Bit-map that identifies the type of Descriptor request and the recipient.</span></span> <span data-ttu-id="b7aba-109">El tipo de solicitud puede ser ' Standard ', ' Class ' o ' specific Vendor '.</span><span class="sxs-lookup"><span data-stu-id="b7aba-109">The type of request may be 'standard', 'class' or 'vendor-specific'.</span></span> <span data-ttu-id="b7aba-110">El destinatario puede ser ' Device ', ' interface ', ' Endpoint ' u ' Other '.</span><span class="sxs-lookup"><span data-stu-id="b7aba-110">The recipient may be 'device', 'interface', 'endpoint' or 'other'.</span></span> <span data-ttu-id="b7aba-111">Consulte la especificación USB para ver los valores adecuados para cada bit.</span><span class="sxs-lookup"><span data-stu-id="b7aba-111">Refer to the USB Specification for the appropriate values for each bit.</span></span>

</dd> <dt>

<span data-ttu-id="b7aba-112">*RequestValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b7aba-112">*RequestValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7aba-113">Contiene el tipo de descriptor en el byte alto y el índice de descriptor (por ejemplo, índice o desplazamiento en la matriz de descriptores) en el byte bajo.</span><span class="sxs-lookup"><span data-stu-id="b7aba-113">Contains the Descriptor Type in the high byte and the Descriptor Index (for example, index or offset into the Descriptor array) in the low byte.</span></span> <span data-ttu-id="b7aba-114">Consulte la especificación de USB para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="b7aba-114">Refer to the USB Specification for more information.</span></span>

</dd> <dt>

<span data-ttu-id="b7aba-115">*RequestIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b7aba-115">*RequestIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7aba-116">Define el código de identificador de idioma de 2 bytes usado por USBDevice al devolver los datos del descriptor de cadena.</span><span class="sxs-lookup"><span data-stu-id="b7aba-116">Defines the 2 byte Language ID code used by the USBDevice when returning string Descriptor data.</span></span> <span data-ttu-id="b7aba-117">El parámetro suele ser 0 para los descriptores que no son de cadena.</span><span class="sxs-lookup"><span data-stu-id="b7aba-117">The parameter is typically 0 for non-string Descriptors.</span></span> <span data-ttu-id="b7aba-118">Consulte la especificación de USB para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="b7aba-118">Refer to the USB Specification for more information.</span></span>

</dd> <dt>

<span data-ttu-id="b7aba-119">*RequestLength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b7aba-119">*RequestLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7aba-120">En la entrada, contiene la longitud (en octetos) del descriptor que se debe devolver.</span><span class="sxs-lookup"><span data-stu-id="b7aba-120">On input, contains the length (in octets) of the Descriptor that should be returned.</span></span> <span data-ttu-id="b7aba-121">Si este valor es menor que la longitud real del descriptor, solo se devolverá la longitud solicitada.</span><span class="sxs-lookup"><span data-stu-id="b7aba-121">If this value is less than the actual length of the Descriptor, only the requested length will be returned.</span></span> <span data-ttu-id="b7aba-122">Si es mayor que la longitud real, se devuelve la longitud real.</span><span class="sxs-lookup"><span data-stu-id="b7aba-122">If it is more than the actual length, the actual length is returned.</span></span> <span data-ttu-id="b7aba-123">En la salida, este parámetro es la longitud, en octetos, del búfer que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="b7aba-123">On output, this parameter is the length, in octets, of the Buffer being returned.</span></span> <span data-ttu-id="b7aba-124">Si el descriptor solicitado no existe, el contenido de este parámetro es indefinido.</span><span class="sxs-lookup"><span data-stu-id="b7aba-124">If the requested Descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="b7aba-125">*Búfer* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b7aba-125">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7aba-126">Devuelve la información de descriptor solicitada.</span><span class="sxs-lookup"><span data-stu-id="b7aba-126">Returns the requested Descriptor information.</span></span> <span data-ttu-id="b7aba-127">Si el descriptor no existe, el contenido del parámetro es indefinido.</span><span class="sxs-lookup"><span data-stu-id="b7aba-127">If the Descriptor does not exist, the contents of the parameter are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7aba-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7aba-128">Return value</span></span>

<span data-ttu-id="b7aba-129">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="b7aba-129">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7aba-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7aba-130">Requirements</span></span>



| <span data-ttu-id="b7aba-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7aba-131">Requirement</span></span> | <span data-ttu-id="b7aba-132">Value</span><span class="sxs-lookup"><span data-stu-id="b7aba-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7aba-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7aba-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b7aba-134">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b7aba-134">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b7aba-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7aba-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b7aba-136">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b7aba-136">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b7aba-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b7aba-137">Namespace</span></span><br/>                | <span data-ttu-id="b7aba-138">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b7aba-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b7aba-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b7aba-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7aba-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7aba-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7aba-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b7aba-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7aba-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b7aba-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b7aba-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7aba-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7aba-144">**\_USBDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="b7aba-144">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> </dl>

 

 




