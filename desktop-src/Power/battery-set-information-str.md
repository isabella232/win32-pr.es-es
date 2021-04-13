---
description: Contiene la información de la batería que se va a establecer.
ms.assetid: 535e56cb-2bab-458a-84a8-2d9a4d96412b
title: BATTERY_SET_INFORMATION estructura (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 0b23489bc5a7608e2e8afb297bb4be7ba35cecb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156520"
---
# <a name="battery_set_information-structure"></a><span data-ttu-id="78614-103">Estructura de información de \_ conjunto de batería \_</span><span class="sxs-lookup"><span data-stu-id="78614-103">BATTERY\_SET\_INFORMATION structure</span></span>

<span data-ttu-id="78614-104">Contiene la información de la batería que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="78614-104">Contains battery information to be set.</span></span> <span data-ttu-id="78614-105">Esta estructura se usa con el código de control de [**información del conjunto de baterías de ioctl \_ \_ \_**](ioctl-battery-set-information.md) .</span><span class="sxs-lookup"><span data-stu-id="78614-105">This structure is used with the [**IOCTL\_BATTERY\_SET\_INFORMATION**](ioctl-battery-set-information.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="78614-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78614-106">Syntax</span></span>


```C++
typedef struct _BATTERY_SET_INFORMATION {
  ULONG                         BatteryTag;
  BATTERY_SET_INFORMATION_LEVEL InformationLevel;
  UCHAR                         Buffer[1];
} BATTERY_SET_INFORMATION, *PBATTERY_SET_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="78614-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="78614-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="78614-108">**BatteryTag**</span><span class="sxs-lookup"><span data-stu-id="78614-108">**BatteryTag**</span></span>
</dt> <dd>

<span data-ttu-id="78614-109">La etiqueta de la batería actual para la batería.</span><span class="sxs-lookup"><span data-stu-id="78614-109">The current battery tag for the battery.</span></span> <span data-ttu-id="78614-110">Solo se puede devolver información de una batería que coincida con la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="78614-110">Information for a battery matching the tag can only be returned.</span></span> <span data-ttu-id="78614-111">Siempre que este valor no coincida con la etiqueta actual de la batería, se completará la solicitud IOCTL con el archivo de ERROR \_ \_ no \_ encontrado, que indica al autor de la llamada que ya no existe la batería para la que tiene una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="78614-111">Whenever this value does not match the battery's current tag, the IOCTL request will be completed with ERROR\_FILE\_NOT\_FOUND, which indicates to the caller that the battery for which it has a tag for no longer exists.</span></span> <span data-ttu-id="78614-112">El autor de la llamada puede optar por usar la operación de etiqueta de consulta de la [**\_ batería \_ \_ ioctl**](ioctl-battery-query-tag.md) para determinar la etiqueta de la batería recién instalada, si existe alguna.</span><span class="sxs-lookup"><span data-stu-id="78614-112">The caller may opt to use the [**IOCTL\_BATTERY\_QUERY\_TAG**](ioctl-battery-query-tag.md) operation to determine the tag of the newly installed battery, if one exists.</span></span> <span data-ttu-id="78614-113">(Consulte [etiquetas de batería](battery-information.md) para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="78614-113">(See [Battery Tags](battery-information.md) for more information.)</span></span>

<span data-ttu-id="78614-114">Cuando se realiza una solicitud de información de consulta, se comprueba este valor.</span><span class="sxs-lookup"><span data-stu-id="78614-114">When a query information request is made, this value is verified.</span></span> <span data-ttu-id="78614-115">Además, si la solicitud está en curso mientras este valor cambia, la solicitud se anula con el estado \_ \_ no se encontró el archivo de error \_ .</span><span class="sxs-lookup"><span data-stu-id="78614-115">In addition, if the request is in progress while this value changes, the request is aborted with the status of ERROR\_FILE\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="78614-116">**InformationLevel**</span><span class="sxs-lookup"><span data-stu-id="78614-116">**InformationLevel**</span></span>
</dt> <dd>

<span data-ttu-id="78614-117">Información de la batería que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="78614-117">The battery information to be set.</span></span> <span data-ttu-id="78614-118">El tipo de datos del miembro de **búfer** depende del valor de este miembro.</span><span class="sxs-lookup"><span data-stu-id="78614-118">The type of data in the **Buffer** member depends on the value of this member.</span></span> <span data-ttu-id="78614-119">Este miembro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="78614-119">This member can be one of the following values.</span></span>



| <span data-ttu-id="78614-120">Value</span><span class="sxs-lookup"><span data-stu-id="78614-120">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="78614-121">Significado</span><span class="sxs-lookup"><span data-stu-id="78614-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryCharge"></span><span id="batterycharge"></span><span id="BATTERYCHARGE"></span><dl> <span data-ttu-id="78614-122"><dt>**BatteryCharge**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="78614-122"><dt>**BatteryCharge**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="78614-123">Informa al dispositivo de la batería de que el usuario ha solicitado que la batería se debe cargar en este momento.</span><span class="sxs-lookup"><span data-stu-id="78614-123">Informs the battery device that the user has requested that the battery should be charging at this time.</span></span> <span data-ttu-id="78614-124">Por ejemplo, con una batería/cargador/selector inteligentes, la aplicación podría cobrar una batería a la vez.</span><span class="sxs-lookup"><span data-stu-id="78614-124">For example, with a smart battery/charger/selector, the application could charge one battery at a time.</span></span> <span data-ttu-id="78614-125">Se omite el miembro de **búfer** de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="78614-125">The **Buffer** member of this structure is ignored.</span></span><br/>                                                                      |
| <span id="BatteryCriticalBias"></span><span id="batterycriticalbias"></span><span id="BATTERYCRITICALBIAS"></span><dl> <span data-ttu-id="78614-126"><dt>**BatteryCriticalBias**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="78614-126"><dt>**BatteryCriticalBias**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="78614-127">Establece el ajuste de la diferencia crítica de la batería.</span><span class="sxs-lookup"><span data-stu-id="78614-127">Sets the battery's critical bias adjustment.</span></span> <span data-ttu-id="78614-128">Tenga en cuenta que no se ha aprovisionado que este valor lo cambiaría normalmente el software, y está presente en las interfaces solo como una característica de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="78614-128">Note it is not envisioned that this value would normally be changed by software, and is present in the interfaces only as a maintenance feature.</span></span> <span data-ttu-id="78614-129">No todas las baterías pueden mantener este valor y se debe leer la información de la batería para confirmar que la batería aceptó la configuración.</span><span class="sxs-lookup"><span data-stu-id="78614-129">Not all batteries can maintain such a setting, and the battery information should be read to confirm that the battery accepted the setting.</span></span><br/> |
| <span id="BatteryDischarge"></span><span id="batterydischarge"></span><span id="BATTERYDISCHARGE"></span><dl> <span data-ttu-id="78614-130"><dt>**BatteryDischarge**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="78614-130"><dt>**BatteryDischarge**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="78614-131">Informa al dispositivo de la batería de que el usuario ha solicitado que la batería se esté descargando en este momento.</span><span class="sxs-lookup"><span data-stu-id="78614-131">Informs the battery device that the user has requested that the battery be discharging at this time.</span></span> <span data-ttu-id="78614-132">Por ejemplo, se podría usar para indicar qué batería desea que el usuario desee alimentar el sistema actualmente.</span><span class="sxs-lookup"><span data-stu-id="78614-132">For example, this could be used to indicate which battery the user currently wants to power the system.</span></span> <span data-ttu-id="78614-133">Se omite el miembro de **búfer** de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="78614-133">The **Buffer** member of this structure is ignored.</span></span><br/>                                                                          |



 

</dd> <dt>

<span data-ttu-id="78614-134">**Buffer**</span><span class="sxs-lookup"><span data-stu-id="78614-134">**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="78614-135">Información de la batería que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="78614-135">The battery information to be set.</span></span> <span data-ttu-id="78614-136">Los datos dependen del valor de **InformationLevel**.</span><span class="sxs-lookup"><span data-stu-id="78614-136">The data depends on the value of **InformationLevel**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78614-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78614-137">Remarks</span></span>

<span data-ttu-id="78614-138">La estructura de **\_ \_ información del conjunto de batería** es una estructura de longitud variable y debe asignar un búfer de tamaño adecuado para la información que se va a incluir en la estructura.</span><span class="sxs-lookup"><span data-stu-id="78614-138">The **BATTERY\_SET\_INFORMATION** structure is a variable-length structure, and you must allocate a buffer of suitable size for the information to be included in the structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="78614-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78614-139">Requirements</span></span>



| <span data-ttu-id="78614-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="78614-140">Requirement</span></span> | <span data-ttu-id="78614-141">Value</span><span class="sxs-lookup"><span data-stu-id="78614-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78614-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78614-142">Minimum supported client</span></span><br/> | <span data-ttu-id="78614-143">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="78614-143">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="78614-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78614-144">Minimum supported server</span></span><br/> | <span data-ttu-id="78614-145">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="78614-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="78614-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="78614-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="78614-147"><dt>Poclass. h; </dt> <dt>Batclass. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="78614-147"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78614-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="78614-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78614-149">**\_información del \_ conjunto de baterías de ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="78614-149">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

 




