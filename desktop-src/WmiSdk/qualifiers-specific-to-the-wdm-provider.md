---
description: El proveedor de WDM usa los siguientes calificadores en archivos MOF de controlador de dispositivo cuando extraen datos de WNODEs para generar instancias de clases de controlador WDM.
ms.assetid: 11b0af59-979f-4908-baef-c9ec564b3cfd
ms.tgt_platform: multiple
title: Calificadores específicos del proveedor de WDM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: be2bc4593c19555dd5a851de89a1dc2e5db00596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696668"
---
# <a name="qualifiers-specific-to-the-wdm-provider"></a><span data-ttu-id="d22c3-103">Calificadores específicos del proveedor de WDM</span><span class="sxs-lookup"><span data-stu-id="d22c3-103">Qualifiers Specific to the WDM Provider</span></span>

<span data-ttu-id="d22c3-104">El [proveedor de WDM](/windows/desktop/WmiCoreProv/wdm-provider) usa los siguientes calificadores en archivos MOF de controlador de dispositivo cuando extraen datos de WNODEs para generar instancias de clases de controlador WDM.</span><span class="sxs-lookup"><span data-stu-id="d22c3-104">The following qualifiers are used by the [WDM Provider](/windows/desktop/WmiCoreProv/wdm-provider) in device driver MOF files when they are extracting data from WNODEs to generate instances of WDM driver classes.</span></span>

<dt>

<span data-ttu-id="d22c3-105"><span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**MissingValue**</span><span class="sxs-lookup"><span data-stu-id="d22c3-105"><span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**MissingValue**</span></span>
</dt> <dd>

<span data-ttu-id="d22c3-106">Tipo de datos: **DWORD, array, Uint8, UInt16, UInt32, sint8, sint16 o sint32.**</span><span class="sxs-lookup"><span data-stu-id="d22c3-106">Data type: **DWORD, array, uint8, uint16, uint32, sint8, sint16, or sint32.**</span></span>

<span data-ttu-id="d22c3-107">Se aplica a: propiedades</span><span class="sxs-lookup"><span data-stu-id="d22c3-107">Applies to: properties</span></span>

<span data-ttu-id="d22c3-108">Un valor que falta para esta propiedad debe estar representado por **null** en lugar de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="d22c3-108">A missing value for this property should be represented by **NULL** rather than 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="d22c3-109"><span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**WMIDataId**</span><span class="sxs-lookup"><span data-stu-id="d22c3-109"><span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**WMIDataId**</span></span>
</dt> <dd>

<span data-ttu-id="d22c3-110">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d22c3-110">Data type: **uint32**</span></span>

<span data-ttu-id="d22c3-111">Se aplica a: propiedades</span><span class="sxs-lookup"><span data-stu-id="d22c3-111">Applies to: properties</span></span>

<span data-ttu-id="d22c3-112">Índice en el WNODE de los datos para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d22c3-112">Index in the WNODE of the data for the property.</span></span> <span data-ttu-id="d22c3-113">El proveedor WDM utiliza este calificador para determinar cómo se da formato a los datos al extraer datos de WNODE y generar clases WMI.</span><span class="sxs-lookup"><span data-stu-id="d22c3-113">The WDM provider uses this qualifier to determine how the data is formatted while extracting data from the WNODE and generating WMI classes.</span></span> <span data-ttu-id="d22c3-114">El valor inicial es 1.</span><span class="sxs-lookup"><span data-stu-id="d22c3-114">The starting value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="d22c3-115"><span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMIExpense**</span><span class="sxs-lookup"><span data-stu-id="d22c3-115"><span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMIExpense**</span></span>
</dt> <dd>

<span data-ttu-id="d22c3-116">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d22c3-116">Data type: **uint32**</span></span>

<span data-ttu-id="d22c3-117">Se aplica a: clases</span><span class="sxs-lookup"><span data-stu-id="d22c3-117">Applies to: classes</span></span>

<span data-ttu-id="d22c3-118">Indicación del costo de recursos para tener acceso al bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="d22c3-118">Indication of the resource cost to access the data block.</span></span> <span data-ttu-id="d22c3-119">Por ejemplo, la información de geometría de disco no requiere una gran cantidad de recursos para obtener porque está disponible en la extensión de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d22c3-119">For example, disk geometry information does not require a lot of resources to obtain because it is available in the device extension.</span></span> <span data-ttu-id="d22c3-120">El rendimiento de lectura y escritura de disco es más intensivo porque requiere trabajo adicional en cada operación de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="d22c3-120">Disk read/write performance is more resource-intensive because it requires extra work on each read/write operation.</span></span> <span data-ttu-id="d22c3-121">Por lo tanto, el valor de calificador **WMIExpense** es mayor para el rendimiento de lectura y escritura de disco.</span><span class="sxs-lookup"><span data-stu-id="d22c3-121">Therefore, the **WMIExpense** qualifier value is larger for disk read/write performance.</span></span>

</dd> <dt>

<span data-ttu-id="d22c3-122"><span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**WMIMethodId**</span><span class="sxs-lookup"><span data-stu-id="d22c3-122"><span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**WMIMethodId**</span></span>
</dt> <dd>

<span data-ttu-id="d22c3-123">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d22c3-123">Data type: **uint32**</span></span>

<span data-ttu-id="d22c3-124">Se aplica a: métodos</span><span class="sxs-lookup"><span data-stu-id="d22c3-124">Applies to: methods</span></span>

<span data-ttu-id="d22c3-125">Índice en el WNODE de los datos para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d22c3-125">Index in the WNODE of the data for the property.</span></span> <span data-ttu-id="d22c3-126">El proveedor WDM utiliza este calificador para determinar cómo se da formato a los datos al extraer datos de WNODE y generar clases WMI.</span><span class="sxs-lookup"><span data-stu-id="d22c3-126">The WDM provider uses this qualifier to determine how the data is formatted while extracting data from the WNODE and generating WMI classes.</span></span> <span data-ttu-id="d22c3-127">El valor inicial es 1.</span><span class="sxs-lookup"><span data-stu-id="d22c3-127">The starting value is 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d22c3-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d22c3-128">Requirements</span></span>



| <span data-ttu-id="d22c3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d22c3-129">Requirement</span></span> | <span data-ttu-id="d22c3-130">Value</span><span class="sxs-lookup"><span data-stu-id="d22c3-130">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d22c3-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d22c3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d22c3-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d22c3-132">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d22c3-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d22c3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d22c3-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d22c3-134">Windows Server 2008</span></span><br/> |



 

