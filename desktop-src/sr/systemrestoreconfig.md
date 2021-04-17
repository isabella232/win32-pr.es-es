---
title: Clase SystemRestoreConfig
description: Proporciona propiedades para controlar la frecuencia de creación de puntos de restauración programados y la cantidad de espacio en disco consumido en cada unidad.
ms.assetid: ed09e03f-8cc1-4923-8f39-bbe7d9a19b44
keywords:
- Restauración del sistema de la clase SystemRestoreConfig
- SystemRestoreConfig (clase) restauración del sistema, descrito
topic_type:
- apiref
api_name:
- SystemRestoreConfig
- SystemRestoreConfig.RPSessionInterval
- SystemRestoreConfig.RPGlobalInterval
- SystemRestoreConfig.RPLifeInterval
- SystemRestoreConfig.DiskPercent
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ded8a17cc4800e1aa2917ba7750c6c69434916
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422406"
---
# <a name="systemrestoreconfig-class"></a><span data-ttu-id="9f4d6-105">Clase SystemRestoreConfig</span><span class="sxs-lookup"><span data-stu-id="9f4d6-105">SystemRestoreConfig class</span></span>

<span data-ttu-id="9f4d6-106">Proporciona propiedades para controlar la frecuencia de creación de puntos de restauración programados y la cantidad de espacio en disco consumido en cada unidad.</span><span class="sxs-lookup"><span data-stu-id="9f4d6-106">Provides properties for controlling the frequency of scheduled restore point creation and the amount of disk space consumed on each drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f4d6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f4d6-107">Syntax</span></span>

``` syntax
class SystemRestoreConfig
{
  uint32 RPSessionInterval;
  uint32 RPGlobalInterval;
  uint32 RPLifeInterval;
  uint32 DiskPercent;
};
```

## <a name="members"></a><span data-ttu-id="9f4d6-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9f4d6-108">Members</span></span>

<span data-ttu-id="9f4d6-109">La clase **SystemRestoreConfig** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9f4d6-109">The **SystemRestoreConfig** class has these types of members:</span></span>

-   [<span data-ttu-id="9f4d6-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9f4d6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f4d6-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9f4d6-111">Properties</span></span>

<span data-ttu-id="9f4d6-112">La clase **SystemRestoreConfig** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9f4d6-112">The **SystemRestoreConfig** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f4d6-113">**DiskPercent**</span><span class="sxs-lookup"><span data-stu-id="9f4d6-113">**DiskPercent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4d6-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f4d6-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f4d6-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9f4d6-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f4d6-116">La cantidad máxima de espacio en disco en cada unidad que puede usar Restaurar sistema.</span><span class="sxs-lookup"><span data-stu-id="9f4d6-116">The maximum amount of disk space on each drive that can be used by System Restore.</span></span> <span data-ttu-id="9f4d6-117">Este valor se especifica como un porcentaje del espacio total de la unidad.</span><span class="sxs-lookup"><span data-stu-id="9f4d6-117">This value is specified as a percentage of the total drive space.</span></span> <span data-ttu-id="9f4d6-118">El valor predeterminado es 12 por ciento.</span><span class="sxs-lookup"><span data-stu-id="9f4d6-118">The default value is 12 percent.</span></span>

<span data-ttu-id="9f4d6-119">**Windows Vista:** Recibe un valor de la Servicio de instantáneas de volumen (VSS).</span><span class="sxs-lookup"><span data-stu-id="9f4d6-119">**Windows Vista:** Receives a value from the Volume Shadow Copy Service (VSS).</span></span> <span data-ttu-id="9f4d6-120">Esta es la cantidad máxima de espacio en disco en cada unidad que puede usar Restaurar sistema.</span><span class="sxs-lookup"><span data-stu-id="9f4d6-120">This this is the maximum amount of disk space on each drive that can be used by System Restore.</span></span> <span data-ttu-id="9f4d6-121">El valor predeterminado es el 15 por ciento del espacio total de la unidad o el 30 por ciento del espacio libre disponible, lo que sea menor.</span><span class="sxs-lookup"><span data-stu-id="9f4d6-121">The default value is 15 percent of the total drive space or 30 percent of the available free space, whichever is smaller.</span></span>

</dd> <dt>

<span data-ttu-id="9f4d6-122">**RPGlobalInterval**</span><span class="sxs-lookup"><span data-stu-id="9f4d6-122">**RPGlobalInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4d6-123">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f4d6-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f4d6-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9f4d6-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f4d6-125">El intervalo de tiempo absoluto en el que se crean los puntos de control del sistema programados, en segundos.</span><span class="sxs-lookup"><span data-stu-id="9f4d6-125">The absolute time interval at which scheduled system checkpoints are created, in seconds.</span></span> <span data-ttu-id="9f4d6-126">El valor predeterminado es 86.400 (24 horas).</span><span class="sxs-lookup"><span data-stu-id="9f4d6-126">The default value is 86,400 (24 hours).</span></span>

<span data-ttu-id="9f4d6-127">**Windows Vista:** Recibe un valor del programador de tareas para restaurar el sistema.</span><span class="sxs-lookup"><span data-stu-id="9f4d6-127">**Windows Vista:** Receives a value from the task scheduler for System Restore.</span></span> <span data-ttu-id="9f4d6-128">Cero si la tarea está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="9f4d6-128">Zero if the task is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="9f4d6-129">**RPLifeInterval**</span><span class="sxs-lookup"><span data-stu-id="9f4d6-129">**RPLifeInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4d6-130">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f4d6-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f4d6-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9f4d6-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f4d6-132">Intervalo de tiempo para el que se conservan los puntos de restauración, en segundos.</span><span class="sxs-lookup"><span data-stu-id="9f4d6-132">The time interval for which restore points are preserved, in seconds.</span></span> <span data-ttu-id="9f4d6-133">Cuando un punto de restauración es más antiguo que este intervalo especificado, se elimina.</span><span class="sxs-lookup"><span data-stu-id="9f4d6-133">When a restore point becomes older than this specified interval, it is deleted.</span></span> <span data-ttu-id="9f4d6-134">El límite de antigüedad predeterminado es de 90 días.</span><span class="sxs-lookup"><span data-stu-id="9f4d6-134">The default age limit is 90 days.</span></span>

<span data-ttu-id="9f4d6-135">**Windows Vista:** Recibe un valor de **UINTMAX**.</span><span class="sxs-lookup"><span data-stu-id="9f4d6-135">**Windows Vista:** Receives a value of **UINTMAX**.</span></span>

</dd> <dt>

<span data-ttu-id="9f4d6-136">**RPSessionInterval**</span><span class="sxs-lookup"><span data-stu-id="9f4d6-136">**RPSessionInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f4d6-137">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f4d6-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f4d6-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9f4d6-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f4d6-139">El intervalo de tiempo en que se crean los puntos de control del sistema programados durante la sesión, en segundos.</span><span class="sxs-lookup"><span data-stu-id="9f4d6-139">The time interval at which scheduled system checkpoints are created during the session, in seconds.</span></span> <span data-ttu-id="9f4d6-140">El valor predeterminado es cero, lo que indica que la característica está desactivada.</span><span class="sxs-lookup"><span data-stu-id="9f4d6-140">The default value is zero, indicating that the feature is turned off.</span></span>

<span data-ttu-id="9f4d6-141">**Windows Vista:** Recibe cero si está deshabilitada la restauración del sistema.</span><span class="sxs-lookup"><span data-stu-id="9f4d6-141">**Windows Vista:** Receives zero if System Restore is disabled.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9f4d6-142">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9f4d6-142">Examples</span></span>

<span data-ttu-id="9f4d6-143">No se admite el siguiente código de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9f4d6-143">The following sample code is not supported.</span></span> <span data-ttu-id="9f4d6-144">Use la herramienta de línea de comandos Vssadmin.exe para cambiar el tamaño del espacio de la unidad reservada.</span><span class="sxs-lookup"><span data-stu-id="9f4d6-144">Use the command-line tool Vssadmin.exe to change the size of reserved drive space.</span></span>

<span data-ttu-id="9f4d6-145">**Windows XP:** Este ejemplo es compatible.</span><span class="sxs-lookup"><span data-stu-id="9f4d6-145">**Windows XP:** This sample is supported.</span></span>


```VB
'The SystemRestoreConfig class provides properties for controlling the frequency of 
'scheduled restore point creation and the amount of disk space consumed on each drive.

Set Args = wscript.Arguments
Set regSR = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestoreConfig='SR'")

If Args.Count() = 0 Then
    Wscript.Echo "Usage: RegSR [RP{Session|Global|Life}Interval[=value]] [DiskPercent[=value]]"
Else    
For i = 0 To Args.Count() - 1
    Myarg = Args.Item(i)
    Pos = InStr(Myarg, "=")
    If Pos <> 0 Then
        Myarray = Split(Myarg, "=", -1, 1)
        myoption = Myarray(0)
        value = Myarray(1)
    Else 
        myoption = Myarg
    End If    
    If myoption = "RPSessionInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPSessionInterval = " & regSR.RPSessionInterval
        Else    
            regSR.RPSessionInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPGlobalInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPGlobalInterval = " & regSR.RPGlobalInterval
        Else    
            regSR.RPGlobalInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPLifeInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPLifeInterval = " & regSR.RPLifeInterval
        Else    
            regSR.RPLifeInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "DiskPercent" Then
        If Pos = 0 Then
            Wscript.Echo "DiskPercent = " & regSR.DiskPercent
        Else    
            regSR.DiskPercent = value
            regSR.Put_
        End If
    End If
Next
End If
```



## <a name="requirements"></a><span data-ttu-id="9f4d6-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f4d6-146">Requirements</span></span>



| <span data-ttu-id="9f4d6-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f4d6-147">Requirement</span></span> | <span data-ttu-id="9f4d6-148">Value</span><span class="sxs-lookup"><span data-stu-id="9f4d6-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9f4d6-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f4d6-149">Minimum supported client</span></span><br/> | <span data-ttu-id="9f4d6-150">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="9f4d6-150">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9f4d6-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f4d6-151">Minimum supported server</span></span><br/> | <span data-ttu-id="9f4d6-152">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9f4d6-152">None supported</span></span><br/>                                                         |
| <span data-ttu-id="9f4d6-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9f4d6-153">Namespace</span></span><br/>                | <span data-ttu-id="9f4d6-154">Raíz \\ predeterminada</span><span class="sxs-lookup"><span data-stu-id="9f4d6-154">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="9f4d6-155">MOF</span><span class="sxs-lookup"><span data-stu-id="9f4d6-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f4d6-156"><dt>MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9f4d6-156"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f4d6-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f4d6-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f4d6-158">Puntos de restauración</span><span class="sxs-lookup"><span data-stu-id="9f4d6-158">Restore Points</span></span>](restore-points.md)
</dt> <dt>

[<span data-ttu-id="9f4d6-159">Instrumental de administración de Windows</span><span class="sxs-lookup"><span data-stu-id="9f4d6-159">Windows Management Instrumentation</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

