---
description: Permite a un administrador administrar las propiedades de cuota de disco de un volumen.
title: Objeto DiskQuotaControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 846297f2-b826-45de-8617-228790e87a63
ms.openlocfilehash: 5f7b1d700c73df56ce7aaef39e162517629f96f6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841556"
---
# <a name="diskquotacontrol-object"></a><span data-ttu-id="d3ce3-103">Objeto DiskQuotaControl</span><span class="sxs-lookup"><span data-stu-id="d3ce3-103">DiskQuotaControl object</span></span>

<span data-ttu-id="d3ce3-104">Permite a un administrador administrar las propiedades de cuota de disco de un volumen.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-104">Allows an administrator to manage a volume's disk quota properties.</span></span> <span data-ttu-id="d3ce3-105">El sistema de archivos NTFS permite a un administrador administrar el uso de disco en un volumen compartido mediante la asignación de una cantidad especificada de espacio en disco, o límite de *cuota,* a cada usuario.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-105">The NTFS file system allows an administrator to manage disk usage on a shared volume by allocating a specified amount of disk space, or *quota limit*, to each user.</span></span> <span data-ttu-id="d3ce3-106">Puede usar este objeto para establecer el límite de cuota predeterminado que se asignará automáticamente a todos los usuarios nuevos.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-106">You can use this object to set the default quota limit that will be automatically assigned to all new users.</span></span>

## <a name="members"></a><span data-ttu-id="d3ce3-107">Members</span><span class="sxs-lookup"><span data-stu-id="d3ce3-107">Members</span></span>

<span data-ttu-id="d3ce3-108">El **objeto DiskQuotaControl** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d3ce3-108">The **DiskQuotaControl** object has these types of members:</span></span>

-   [<span data-ttu-id="d3ce3-109">Eventos</span><span class="sxs-lookup"><span data-stu-id="d3ce3-109">Events</span></span>](#events)
-   [<span data-ttu-id="d3ce3-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="d3ce3-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="d3ce3-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d3ce3-111">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="d3ce3-112">Eventos</span><span class="sxs-lookup"><span data-stu-id="d3ce3-112">Events</span></span>

<span data-ttu-id="d3ce3-113">El **objeto DiskQuotaControl** tiene estos eventos.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-113">The **DiskQuotaControl** object has these events.</span></span>



| <span data-ttu-id="d3ce3-114">Evento</span><span class="sxs-lookup"><span data-stu-id="d3ce3-114">Event</span></span>                                                           | <span data-ttu-id="d3ce3-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3ce3-115">Description</span></span>                                                                                                                   |
|:----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3ce3-116">**OnUserNameChanged**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-116">**OnUserNameChanged**</span></span>](diskquotacontrol-onusernamechanged.md) | <span data-ttu-id="d3ce3-117">Se produce cuando se ha resuelto la información de nombre de un objeto [**DIDiskQuotaUser.**](didiskquotauser-object.md)</span><span class="sxs-lookup"><span data-stu-id="d3ce3-117">Occurs when the name information for a [**DIDiskQuotaUser**](didiskquotauser-object.md) object has been resolved.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="d3ce3-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="d3ce3-118">Methods</span></span>

<span data-ttu-id="d3ce3-119">El **objeto DiskQuotaControl** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-119">The **DiskQuotaControl** object has these methods.</span></span>



| <span data-ttu-id="d3ce3-120">Método</span><span class="sxs-lookup"><span data-stu-id="d3ce3-120">Method</span></span>                                                                                    | <span data-ttu-id="d3ce3-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3ce3-121">Description</span></span>                                                                                |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3ce3-122">**AddUser**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-122">**AddUser**</span></span>](diskquotacontrol-adduser.md)                                               | <span data-ttu-id="d3ce3-123">Asigna una cuota de disco no predeterminada a un nuevo usuario.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-123">Assigns a nondefault disk quota to a new user.</span></span><br/>                                  |
| [<span data-ttu-id="d3ce3-124">**DeleteUser**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-124">**DeleteUser**</span></span>](diskquotacontrol-deleteuser.md)                                         | <span data-ttu-id="d3ce3-125">Elimina un usuario del volumen.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-125">Deletes a user from the volume.</span></span><br/>                                                 |
| [<span data-ttu-id="d3ce3-126">**FindUser**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-126">**FindUser**</span></span>](diskquotacontrol-finduser.md)                                             | <span data-ttu-id="d3ce3-127">Busca la entrada de un usuario, por nombre, en el archivo de cuota del volumen.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-127">Finds a user's entry, by name, in the volume's quota file.</span></span><br/>                      |
| [<span data-ttu-id="d3ce3-128">**GiveUserNameResolutionPriority**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-128">**GiveUserNameResolutionPriority**</span></span>](diskquotacontrol-giveusernameresolutionpriority.md) | <span data-ttu-id="d3ce3-129">Coloca el objeto de usuario especificado a continuación en línea para la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-129">Places the specified user object next in line for name resolution.</span></span><br/>              |
| [<span data-ttu-id="d3ce3-130">**Inicialización**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-130">**Initialize**</span></span>](diskquotacontrol-initialize.md)                                         | <span data-ttu-id="d3ce3-131">Abre un volumen especificado e inicializa su objeto de control de cuota.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-131">Opens a specified volume and initializes its quota control object.</span></span><br/>              |
| [<span data-ttu-id="d3ce3-132">**InvalidateSidNameCache**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-132">**InvalidateSidNameCache**</span></span>](diskquotacontrol-invalidatesidnamecache.md)                 | <span data-ttu-id="d3ce3-133">Invalida la caché de nombres de usuario del identificador de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-133">Invalidates the security ID user name cache.</span></span><br/>                                    |
| [<span data-ttu-id="d3ce3-134">**ShutdownNameResolution**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-134">**ShutdownNameResolution**</span></span>](diskquotacontrol-shutdownnameresolution.md)                 | <span data-ttu-id="d3ce3-135">Cierra el subproceso de resolución de nombres de usuario.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-135">Shuts down the user name resolution thread.</span></span><br/>                                     |
| [<span data-ttu-id="d3ce3-136">**TranslateLogonNameToSID**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-136">**TranslateLogonNameToSID**</span></span>](diskquotacontrol-translatelogonnametosid.md)               | <span data-ttu-id="d3ce3-137">Traduce un nombre de inicio de sesión al identificador de seguridad de usuario correspondiente en formato de cadena.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-137">Translates a logon name to the corresponding user security ID in string format.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d3ce3-138">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d3ce3-138">Properties</span></span>

<span data-ttu-id="d3ce3-139">El **objeto DiskQuotaControl** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-139">The **DiskQuotaControl** object has these properties.</span></span>



| <span data-ttu-id="d3ce3-140">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d3ce3-140">Property</span></span>                                                                                   | <span data-ttu-id="d3ce3-141">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="d3ce3-141">Access type</span></span>           | <span data-ttu-id="d3ce3-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3ce3-142">Description</span></span>                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3ce3-143">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-143">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)<br/>                 | <span data-ttu-id="d3ce3-144">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="d3ce3-144">Read/write</span></span><br/> | <span data-ttu-id="d3ce3-145">Establece u obtiene el límite de cuota predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-145">Sets or gets the default quota limit.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="d3ce3-146">**DefaultQuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-146">**DefaultQuotaLimitText**</span></span>](diskquotacontrol-defaultquotalimittext.md)<br/>         | <span data-ttu-id="d3ce3-147">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d3ce3-147">Read-only</span></span><br/>  | <span data-ttu-id="d3ce3-148">Obtiene el límite de cuota predeterminado como una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-148">Gets the default quota limit as a text string.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="d3ce3-149">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-149">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)<br/>         | <span data-ttu-id="d3ce3-150">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="d3ce3-150">Read/write</span></span><br/> | <span data-ttu-id="d3ce3-151">Establece u obtiene el umbral de cuota predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-151">Sets or gets the default quota threshold.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="d3ce3-152">**DefaultQuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-152">**DefaultQuotaThresholdText**</span></span>](diskquotacontrol-defaultquotathresholdtext.md)<br/> | <span data-ttu-id="d3ce3-153">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d3ce3-153">Read-only</span></span><br/>  | <span data-ttu-id="d3ce3-154">Obtiene el umbral de cuota predeterminado como una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-154">Gets the default quota threshold as a text string.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="d3ce3-155">**LogQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-155">**LogQuotaLimit**</span></span>](diskquotacontrol-logquotalimit.md)<br/>                         | <span data-ttu-id="d3ce3-156">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="d3ce3-156">Read/write</span></span><br/> | <span data-ttu-id="d3ce3-157">Establece u obtiene un valor booleano que indica si se realizará una entrada del registro de eventos del sistema cuando un usuario supere su límite de cuota asignado.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-157">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota limit.</span></span><br/>     |
| [<span data-ttu-id="d3ce3-158">**LogQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-158">**LogQuotaThreshold**</span></span>](diskquotacontrol-logquotathreshold.md)<br/>                 | <span data-ttu-id="d3ce3-159">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="d3ce3-159">Read/write</span></span><br/> | <span data-ttu-id="d3ce3-160">Establece u obtiene un valor booleano que indica si se realizará una entrada del registro de eventos del sistema cuando un usuario supere su umbral de cuota asignado.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-160">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota threshold.</span></span><br/> |
| [<span data-ttu-id="d3ce3-161">**QuotaFileIncomplete**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-161">**QuotaFileIncomplete**</span></span>](diskquotacontrol-quotafileincomplete.md)<br/>             | <span data-ttu-id="d3ce3-162">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d3ce3-162">Read-only</span></span><br/>  | <span data-ttu-id="d3ce3-163">Obtiene un valor booleano que indica si el archivo de cuota del volumen está completo.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-163">Gets a Boolean value that indicates whether the quota file for the volume is complete.</span></span><br/>                                                             |
| [<span data-ttu-id="d3ce3-164">**QuotaFileRebuilding**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-164">**QuotaFileRebuilding**</span></span>](diskquotacontrol-quotafilerebuilding.md)<br/>             | <span data-ttu-id="d3ce3-165">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d3ce3-165">Read-only</span></span><br/>  | <span data-ttu-id="d3ce3-166">Obtiene un valor booleano que indica si el archivo de cuota del volumen se está recompilando actualmente.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-166">Gets a Boolean value that indicates whether the quota file for the volume is currently being rebuilt.</span></span><br/>                                              |
| [<span data-ttu-id="d3ce3-167">**QuotaState**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-167">**QuotaState**</span></span>](diskquotacontrol-quotastate.md)<br/>                               | <span data-ttu-id="d3ce3-168">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="d3ce3-168">Read/write</span></span><br/> | <span data-ttu-id="d3ce3-169">Establece u obtiene el estado de las cuotas de disco del volumen.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-169">Sets or gets the state of the volume's disk quotas.</span></span><br/>                                                                                                |
| [<span data-ttu-id="d3ce3-170">**UserNameResolution**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-170">**UserNameResolution**</span></span>](diskquotacontrol-usernameresolution.md)<br/>               | <span data-ttu-id="d3ce3-171">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="d3ce3-171">Read/write</span></span><br/> | <span data-ttu-id="d3ce3-172">Establece u obtiene un valor que controla cómo se resuelve el SID de usuario en los nombres de usuario.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-172">Sets or gets a value that controls how user SID are resolved to user names.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="d3ce3-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3ce3-173">Remarks</span></span>

<span data-ttu-id="d3ce3-174">Un administrador puede usar el **objeto DiskQuotaControl** para realizar una serie de tareas, incluidas las siguientes:</span><span class="sxs-lookup"><span data-stu-id="d3ce3-174">An administrator can use the **DiskQuotaControl** object to do a number of tasks, including the following:</span></span>

-   <span data-ttu-id="d3ce3-175">Habilitación y deshabilitación del sistema de cuota de disco del volumen.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-175">Enabling and disabling the volume's disk quota system.</span></span>
-   <span data-ttu-id="d3ce3-176">Obtener el estado del sistema de cuota en el volumen.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-176">Obtaining the status of the quota system on the volume.</span></span>
-   <span data-ttu-id="d3ce3-177">Denegar espacio en disco a los usuarios que superen su límite de cuota.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-177">Denying disk space to users exceeding their quota limit.</span></span>
-   <span data-ttu-id="d3ce3-178">Especificación del umbral de advertencia predeterminado y los valores de límite de cuota que se asignarán a los nuevos usuarios.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-178">Specifying the default warning threshold and quota limit values that will be assigned to new users.</span></span>
-   <span data-ttu-id="d3ce3-179">Agregar y quitar usuarios.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-179">Adding and removing users.</span></span>

<span data-ttu-id="d3ce3-180">El **objeto DiskQuotaControl** permite establecer valores predeterminados globales para el volumen para propiedades como límites de cuota.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-180">The **DiskQuotaControl** object allows you to set global default values for the volume for properties such as quota limits.</span></span> <span data-ttu-id="d3ce3-181">Sin embargo, cada usuario se representa mediante un [**objeto DIDiskQuotaUser**](didiskquotauser-object.md) que se puede usar para especificar la configuración de cuota individual.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-181">However, each user is represented by a [**DIDiskQuotaUser**](didiskquotauser-object.md) object that can be used to specify individual quota settings.</span></span>

<span data-ttu-id="d3ce3-182">Hay varias maneras de obtener el objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) de un usuario:</span><span class="sxs-lookup"><span data-stu-id="d3ce3-182">There are several ways to obtain a user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object:</span></span>

-   <span data-ttu-id="d3ce3-183">Los [**objetos DIDiskQuotaUser**](didiskquotauser-object.md) para todos los usuarios con cuotas en el volumen se exponen como una colección y se pueden enumerar.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-183">The [**DIDiskQuotaUser**](didiskquotauser-object.md) objects for all users with quotas on the volume are exposed as a collection, and can be enumerated.</span></span> <span data-ttu-id="d3ce3-184">Para obtener una explicación sobre cómo enumerar objetos **DIDiskQuotaUser,** vea **Enumerating Disk Quota Users (Enumeración** de usuarios de cuota de disco) en la sección Comentarios de **DIDiskQuotaUser**.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-184">For a discussion of how to enumerate **DIDiskQuotaUser** objects, see **Enumerating Disk Quota Users** in the Remarks section of **DIDiskQuotaUser**.</span></span>
-   <span data-ttu-id="d3ce3-185">Al agregar un nuevo usuario, el [**método AddUser**](diskquotacontrol-adduser.md) devuelve el objeto [**DIDiskQuotaUser del**](didiskquotauser-object.md) usuario.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-185">When you add a new user, the [**AddUser**](diskquotacontrol-adduser.md) method returns the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>
-   <span data-ttu-id="d3ce3-186">Si tiene el nombre del usuario, el [**método FindUser**](diskquotacontrol-finduser.md) devuelve el objeto [**DIDiskQuotaUser del**](didiskquotauser-object.md) usuario.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-186">If you have the user's name, the [**FindUser**](diskquotacontrol-finduser.md) method returns the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

<span data-ttu-id="d3ce3-187">Este objeto hace que la funcionalidad esencial de la interfaz IDiskQuotaControl esté disponible para scripting y aplicaciones basadas Visual Basic Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-187">This object makes the essential functionality of the IDiskQuotaControl interface available to scripting and Microsoft Visual Basic-based applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3ce3-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3ce3-188">Requirements</span></span>



| <span data-ttu-id="d3ce3-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3ce3-189">Requirement</span></span> | <span data-ttu-id="d3ce3-190">Value</span><span class="sxs-lookup"><span data-stu-id="d3ce3-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ce3-191">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3ce3-191">Minimum supported client</span></span><br/> | <span data-ttu-id="d3ce3-192">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d3ce3-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d3ce3-193">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3ce3-193">Minimum supported server</span></span><br/> | <span data-ttu-id="d3ce3-194">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d3ce3-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d3ce3-195">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d3ce3-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3ce3-196"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d3ce3-196"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3ce3-197">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d3ce3-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3ce3-198">**Objeto shell**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-198">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 




