---
description: Especifica una lista de cadenas Unicode que representan las funciones de dispositivo requeridas por la transformación del sensor.
ms.assetid: 4A129FEB-E650-47C9-ABC0-9A512EE4121D
title: MF_DEVICESTREAM_REQUIRED_CAPABILITIES atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cac47d60c38e41d44ecf0776ea8bf7588559dfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154636"
---
# <a name="mf_devicestream_required_capabilities-attribute"></a><span data-ttu-id="9e03b-103">\_ \_ Atributo required CAPABILITIES de MF DEVICESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="9e03b-103">MF\_DEVICESTREAM\_REQUIRED\_CAPABILITIES attribute</span></span>

<span data-ttu-id="9e03b-104">Especifica una lista de cadenas Unicode que representan las funciones de dispositivo requeridas por la transformación del sensor.</span><span class="sxs-lookup"><span data-stu-id="9e03b-104">Specifies a list of unicode strings representing the device capabilities required by the sensor transform.</span></span>

## <a name="data-type"></a><span data-ttu-id="9e03b-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9e03b-105">Data type</span></span>

<span data-ttu-id="9e03b-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="9e03b-106">\**WCHAR\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="9e03b-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e03b-107">Remarks</span></span>

<span data-ttu-id="9e03b-108">Este atributo es opcional y solo es necesario si la transformación del sensor tiene acceso a un recurso protegido.</span><span class="sxs-lookup"><span data-stu-id="9e03b-108">This attribute is optional and only required if the sensor transform accesses a protected resource.</span></span> <span data-ttu-id="9e03b-109">El valor debe ser una lista delimitada por punto y coma de tokens de cadena definidos en [_ *DeviceCapability* \*](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability).</span><span class="sxs-lookup"><span data-stu-id="9e03b-109">The value must be a semicolon delimited list of string tokens defined in [_ *DeviceCapability*\*](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e03b-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e03b-110">Requirements</span></span>



| <span data-ttu-id="9e03b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e03b-111">Requirement</span></span> | <span data-ttu-id="9e03b-112">Value</span><span class="sxs-lookup"><span data-stu-id="9e03b-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9e03b-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e03b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9e03b-114">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e03b-114">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9e03b-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e03b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9e03b-116">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9e03b-116">None supported</span></span><br/>                                                          |
| <span data-ttu-id="9e03b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e03b-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e03b-118"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e03b-118"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
