---
title: Clase SystemRestore
description: Proporciona métodos para deshabilitar y habilitar la supervisión, enumerar los puntos de restauración disponibles e iniciar una restauración en el sistema local.
ms.assetid: 87216a56-6d40-44ea-a1ab-d43590b639a4
keywords:
- Restauración del sistema de la clase SystemRestore
- SystemRestore (clase) restauración del sistema, descrito
topic_type:
- apiref
api_name:
- SystemRestore
- SystemRestore.Description
- SystemRestore.RestorePointType
- SystemRestore.EventType
- SystemRestore.SequenceNumber
- SystemRestore.CreationTime
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64d2b609a7a49a9b319c15745600aa54193350e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079495"
---
# <a name="systemrestore-class"></a><span data-ttu-id="dae50-105">Clase SystemRestore</span><span class="sxs-lookup"><span data-stu-id="dae50-105">SystemRestore class</span></span>

<span data-ttu-id="dae50-106">Proporciona métodos para deshabilitar y habilitar la supervisión, enumerar los puntos de restauración disponibles e iniciar una restauración en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="dae50-106">Provides methods for disabling and enabling monitoring, listing available restore points, and initiating a restore on the local system.</span></span>

## <a name="syntax"></a><span data-ttu-id="dae50-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dae50-107">Syntax</span></span>

``` syntax
class SystemRestore
{
  String Description;
  uint32 RestorePointType;
  uint32 EventType;
  uint32 SequenceNumber;
  String CreationTime;
};
```

## <a name="members"></a><span data-ttu-id="dae50-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="dae50-108">Members</span></span>

<span data-ttu-id="dae50-109">La clase **SystemRestore** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dae50-109">The **SystemRestore** class has these types of members:</span></span>

-   [<span data-ttu-id="dae50-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="dae50-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="dae50-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dae50-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dae50-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="dae50-112">Methods</span></span>

<span data-ttu-id="dae50-113">La clase **SystemRestore** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="dae50-113">The **SystemRestore** class has these methods.</span></span>



| <span data-ttu-id="dae50-114">Método</span><span class="sxs-lookup"><span data-stu-id="dae50-114">Method</span></span>                                                             | <span data-ttu-id="dae50-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="dae50-115">Description</span></span>                                                 |
|:-------------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="dae50-116">**CreateRestorePoint**</span><span class="sxs-lookup"><span data-stu-id="dae50-116">**CreateRestorePoint**</span></span>](createrestorepoint-systemrestore.md)     | <span data-ttu-id="dae50-117">Crea un punto de restauración.</span><span class="sxs-lookup"><span data-stu-id="dae50-117">Creates a restore point.</span></span><br/>                         |
| [<span data-ttu-id="dae50-118">**Disable**</span><span class="sxs-lookup"><span data-stu-id="dae50-118">**Disable**</span></span>](disable-systemrestore.md)                           | <span data-ttu-id="dae50-119">Deshabilita la supervisión en una unidad determinada.</span><span class="sxs-lookup"><span data-stu-id="dae50-119">Disables monitoring on a particular drive.</span></span><br/>       |
| [<span data-ttu-id="dae50-120">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="dae50-120">**Enable**</span></span>](enable-systemrestore.md)                             | <span data-ttu-id="dae50-121">Habilita la supervisión en una unidad determinada.</span><span class="sxs-lookup"><span data-stu-id="dae50-121">Enables monitoring on a particular drive.</span></span><br/>        |
| [<span data-ttu-id="dae50-122">**GetLastRestoreStatus**</span><span class="sxs-lookup"><span data-stu-id="dae50-122">**GetLastRestoreStatus**</span></span>](getlastrestorestatus-systemrestore.md) | <span data-ttu-id="dae50-123">Recupera el estado de la última restauración del sistema.</span><span class="sxs-lookup"><span data-stu-id="dae50-123">Retrieves the status of the last system restore.</span></span><br/> |
| [<span data-ttu-id="dae50-124">**Restaurar**</span><span class="sxs-lookup"><span data-stu-id="dae50-124">**Restore**</span></span>](restore-systemrestore.md)                           | <span data-ttu-id="dae50-125">Inicia una restauración del sistema.</span><span class="sxs-lookup"><span data-stu-id="dae50-125">Initiates a system restore.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="dae50-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dae50-126">Properties</span></span>

<span data-ttu-id="dae50-127">La clase **SystemRestore** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dae50-127">The **SystemRestore** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dae50-128">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="dae50-128">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae50-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dae50-129">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="dae50-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dae50-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dae50-131">La hora a la que se produjo el cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="dae50-131">The time at which the state change occurred.</span></span>

</dd> <dt>

<span data-ttu-id="dae50-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dae50-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae50-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dae50-133">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="dae50-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dae50-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dae50-135">La descripción que se va a mostrar para que el usuario pueda identificar fácilmente un punto de restauración.</span><span class="sxs-lookup"><span data-stu-id="dae50-135">The description to be displayed so the user can easily identify a restore point.</span></span> <span data-ttu-id="dae50-136">La longitud máxima de una cadena ANSI es MAX \_ desc.</span><span class="sxs-lookup"><span data-stu-id="dae50-136">The maximum length of an ANSI string is MAX\_DESC.</span></span> <span data-ttu-id="dae50-137">La longitud máxima de una cadena Unicode es MAX \_ DESC \_ W.</span><span class="sxs-lookup"><span data-stu-id="dae50-137">The maximum length of a Unicode string is MAX\_DESC\_W.</span></span> <span data-ttu-id="dae50-138">Para obtener más información, vea [texto de descripción de punto de restauración](restore-point-description-text.md).</span><span class="sxs-lookup"><span data-stu-id="dae50-138">For more information, see [Restore Point Description Text](restore-point-description-text.md).</span></span>

</dd> <dt>

<span data-ttu-id="dae50-139">**EventType**</span><span class="sxs-lookup"><span data-stu-id="dae50-139">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae50-140">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dae50-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dae50-141">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dae50-141">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dae50-142">Tipo del evento.</span><span class="sxs-lookup"><span data-stu-id="dae50-142">The type of event.</span></span> <span data-ttu-id="dae50-143">Este miembro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="dae50-143">This member can be one of the following values.</span></span>



| <span data-ttu-id="dae50-144">Value</span><span class="sxs-lookup"><span data-stu-id="dae50-144">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="dae50-145">Significado</span><span class="sxs-lookup"><span data-stu-id="dae50-145">Meaning</span></span>                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <span data-ttu-id="dae50-146"><dt>**Inicio \_ de Cambio de \_ sistema \_ anidado**</dt> <dt>102</dt></span><span class="sxs-lookup"><span data-stu-id="dae50-146"><dt>**BEGIN\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>102</dt></span></span> </dl> | <span data-ttu-id="dae50-147">Ha empezado un cambio en el sistema.</span><span class="sxs-lookup"><span data-stu-id="dae50-147">A system change has begun.</span></span> <span data-ttu-id="dae50-148">Una llamada subsiguiente anidada no crea un nuevo punto de restauración.</span><span class="sxs-lookup"><span data-stu-id="dae50-148">A subsequent nested call does not create a new restore point.</span></span> <br/> <span data-ttu-id="dae50-149">Las llamadas subsiguientes deben usar END \_ Nested \_ System \_ Change, no end \_ System \_ Change.</span><span class="sxs-lookup"><span data-stu-id="dae50-149">Subsequent calls must use END\_NESTED\_SYSTEM\_CHANGE, not END\_SYSTEM\_CHANGE.</span></span><br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <span data-ttu-id="dae50-150"><dt>**Inicio \_ de \_Cambio del sistema**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="dae50-150"><dt>**BEGIN\_SYSTEM\_CHANGE**</dt> <dt>100</dt></span></span> </dl>                       | <span data-ttu-id="dae50-151">Ha empezado un cambio en el sistema.</span><span class="sxs-lookup"><span data-stu-id="dae50-151">A system change has begun.</span></span><br/>                                                                                                                                                           |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <span data-ttu-id="dae50-152"><dt>**Fin \_ de Cambio de \_ sistema \_ anidado**</dt> <dt>103</dt></span><span class="sxs-lookup"><span data-stu-id="dae50-152"><dt>**END\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>103</dt></span></span> </dl>       | <span data-ttu-id="dae50-153">Ha finalizado un cambio de sistema.</span><span class="sxs-lookup"><span data-stu-id="dae50-153">A system change has ended.</span></span><br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <span data-ttu-id="dae50-154"><dt>**Fin \_ de \_Cambio del sistema**</dt> <dt>101</dt></span><span class="sxs-lookup"><span data-stu-id="dae50-154"><dt>**END\_SYSTEM\_CHANGE**</dt> <dt>101</dt></span></span> </dl>                             | <span data-ttu-id="dae50-155">Ha finalizado un cambio de sistema.</span><span class="sxs-lookup"><span data-stu-id="dae50-155">A system change has ended.</span></span><br/>                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="dae50-156">**RestorePointType**</span><span class="sxs-lookup"><span data-stu-id="dae50-156">**RestorePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae50-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dae50-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dae50-158">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dae50-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dae50-159">El tipo de punto de restauración.</span><span class="sxs-lookup"><span data-stu-id="dae50-159">The type of restore point.</span></span> <span data-ttu-id="dae50-160">Este miembro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="dae50-160">This member can be one of the following values.</span></span>



| <span data-ttu-id="dae50-161">Value</span><span class="sxs-lookup"><span data-stu-id="dae50-161">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="dae50-162">Significado</span><span class="sxs-lookup"><span data-stu-id="dae50-162">Meaning</span></span>                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <span data-ttu-id="dae50-163"><dt>**Aplicación \_ de INSTALAR**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dae50-163"><dt>**APPLICATION\_INSTALL**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="dae50-164">Se ha instalado una aplicación.</span><span class="sxs-lookup"><span data-stu-id="dae50-164">An application has been installed.</span></span><br/>                                                                                                                 |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <span data-ttu-id="dae50-165"><dt>**Aplicación \_ de Desinstalar**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="dae50-165"><dt>**APPLICATION\_UNINSTALL**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="dae50-166">Se ha desinstalado una aplicación.</span><span class="sxs-lookup"><span data-stu-id="dae50-166">An application has been uninstalled.</span></span><br/>                                                                                                               |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <span data-ttu-id="dae50-167"><dt>**Cancelado \_ OPERACIÓN**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="dae50-167"><dt>**CANCELLED\_OPERATION**</dt> <dt>13</dt></span></span> </dl>        | <span data-ttu-id="dae50-168">Una aplicación debe eliminar el punto de restauración que creó.</span><span class="sxs-lookup"><span data-stu-id="dae50-168">An application needs to delete the restore point it created.</span></span> <span data-ttu-id="dae50-169">Por ejemplo, una aplicación usaría esta marca cuando un usuario cancela una instalación.</span><span class="sxs-lookup"><span data-stu-id="dae50-169">For example, an application would use this flag when a user cancels an installation.</span></span> <br/> |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <span data-ttu-id="dae50-170"><dt>**Dispositivo \_ de \_Instalación del controlador**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="dae50-170"><dt>**DEVICE\_DRIVER\_INSTALL**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="dae50-171">Se ha instalado un controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dae50-171">A device driver has been installed.</span></span><br/>                                                                                                                |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <span data-ttu-id="dae50-172"><dt>**Modificar \_ CONFIGURACIÓN**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="dae50-172"><dt>**MODIFY\_SETTINGS**</dt> <dt>12</dt></span></span> </dl>                    | <span data-ttu-id="dae50-173">Una aplicación tiene características agregadas o eliminadas.</span><span class="sxs-lookup"><span data-stu-id="dae50-173">An application has had features added or removed.</span></span><br/>                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="dae50-174">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="dae50-174">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae50-175">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dae50-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dae50-176">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dae50-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dae50-177">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="dae50-177">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="dae50-178">Número de secuencia del punto de restauración.</span><span class="sxs-lookup"><span data-stu-id="dae50-178">The sequence number of the restore point.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dae50-179">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dae50-179">Remarks</span></span>

<span data-ttu-id="dae50-180">Puede obtener una lista de puntos de restauración mediante el método [**SWbemServices. instances**](/windows/desktop/WmiSdk/swbemservices-instancesof) para recuperar una colección de objetos **SystemRestore** .</span><span class="sxs-lookup"><span data-stu-id="dae50-180">You can obtain a list of restore points by using the [**SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) method to retrieve a collection of **SystemRestore** objects.</span></span> <span data-ttu-id="dae50-181">Puede usar las propiedades de clase para identificar el punto de restauración.</span><span class="sxs-lookup"><span data-stu-id="dae50-181">You can use the class properties to identify the restore point.</span></span>

## <a name="examples"></a><span data-ttu-id="dae50-182">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="dae50-182">Examples</span></span>

<span data-ttu-id="dae50-183">En el siguiente script de ejemplo se enumeran los puntos de restauración actuales.</span><span class="sxs-lookup"><span data-stu-id="dae50-183">The following sample script enumerates the current restore points.</span></span>


```VB
'SystemRestore Class
'Provides methods for disabling and enabling monitoring, 
'listing available restore points, and initiating a 
'restore on the local system.

Set RPSet = GetObject("winmgmts:root/default").InstancesOf ("SystemRestore")
for each RP in RPSet
    wscript.Echo "Dir: RP" & RP.SequenceNumber & ", Name: " & RP.Description & ", Type: ", RP.RestorePointType & ", Time: " & RP.CreationTime
next
```



## <a name="requirements"></a><span data-ttu-id="dae50-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dae50-184">Requirements</span></span>



| <span data-ttu-id="dae50-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="dae50-185">Requirement</span></span> | <span data-ttu-id="dae50-186">Value</span><span class="sxs-lookup"><span data-stu-id="dae50-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="dae50-187">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dae50-187">Minimum supported client</span></span><br/> | <span data-ttu-id="dae50-188">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="dae50-188">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="dae50-189">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dae50-189">Minimum supported server</span></span><br/> | <span data-ttu-id="dae50-190">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="dae50-190">None supported</span></span><br/>                                                         |
| <span data-ttu-id="dae50-191">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dae50-191">Namespace</span></span><br/>                | <span data-ttu-id="dae50-192">Raíz \\ predeterminada</span><span class="sxs-lookup"><span data-stu-id="dae50-192">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="dae50-193">MOF</span><span class="sxs-lookup"><span data-stu-id="dae50-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dae50-194"><dt>MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dae50-194"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dae50-195">Vea también</span><span class="sxs-lookup"><span data-stu-id="dae50-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dae50-196">Instrumental de administración de Windows</span><span class="sxs-lookup"><span data-stu-id="dae50-196">Windows Management Instrumentation</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

