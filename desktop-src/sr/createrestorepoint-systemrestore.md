---
title: Método CreateRestorePoint de la clase SystemRestore
description: Crea un punto de restauración.
ms.assetid: 30e1ff03-816c-463f-9f80-6d84149f0e0b
keywords:
- Método CreateRestorePoint Restaurar sistema
- Método CreateRestorePoint Restaurar sistema, clase SystemRestore
- SystemRestore Class System Restore, CreateRestorePoint método
topic_type:
- apiref
api_name:
- SystemRestore.CreateRestorePoint
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1cae9e78d1845f628d62dc46362f1bc2bd8a37e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491038"
---
# <a name="createrestorepoint-method-of-the-systemrestore-class"></a><span data-ttu-id="8c725-106">Método CreateRestorePoint de la clase SystemRestore</span><span class="sxs-lookup"><span data-stu-id="8c725-106">CreateRestorePoint method of the SystemRestore class</span></span>

<span data-ttu-id="8c725-107">Crea un punto de restauración.</span><span class="sxs-lookup"><span data-stu-id="8c725-107">Creates a restore point.</span></span>

<span data-ttu-id="8c725-108">Este método es el equivalente que admite scripts de la función [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) .</span><span class="sxs-lookup"><span data-stu-id="8c725-108">This method is the scriptable equivalent of the [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c725-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c725-109">Syntax</span></span>


```mof
uint32 CreateRestorePoint(
  [in] String Description,
  [in] uint32 RestorePointType,
  [in] uint32 EventType
);
```



## <a name="parameters"></a><span data-ttu-id="8c725-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c725-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c725-111">*Descripción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8c725-111">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c725-112">La descripción que se va a mostrar para que el usuario pueda identificar fácilmente un punto de restauración.</span><span class="sxs-lookup"><span data-stu-id="8c725-112">The description to be displayed so the user can easily identify a restore point.</span></span> <span data-ttu-id="8c725-113">La longitud máxima de una cadena ANSI es MAX \_ desc.</span><span class="sxs-lookup"><span data-stu-id="8c725-113">The maximum length of an ANSI string is MAX\_DESC.</span></span> <span data-ttu-id="8c725-114">La longitud máxima de una cadena Unicode es MAX \_ DESC \_ W.</span><span class="sxs-lookup"><span data-stu-id="8c725-114">The maximum length of a Unicode string is MAX\_DESC\_W.</span></span> <span data-ttu-id="8c725-115">Para obtener más información, vea [texto de descripción de punto de restauración](restore-point-description-text.md).</span><span class="sxs-lookup"><span data-stu-id="8c725-115">For more information, see [Restore Point Description Text](restore-point-description-text.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c725-116">*RestorePointType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c725-116">*RestorePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c725-117">El tipo de punto de restauración.</span><span class="sxs-lookup"><span data-stu-id="8c725-117">The type of restore point.</span></span> <span data-ttu-id="8c725-118">Este miembro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8c725-118">This member can be one of the following values.</span></span>



| <span data-ttu-id="8c725-119">Tipo de punto de restauración</span><span class="sxs-lookup"><span data-stu-id="8c725-119">Restore point type</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="8c725-120">Significado</span><span class="sxs-lookup"><span data-stu-id="8c725-120">Meaning</span></span>                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <span data-ttu-id="8c725-121"><dt>**Aplicación \_ de INSTALAR**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8c725-121"><dt>**APPLICATION\_INSTALL**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="8c725-122">Se ha instalado una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8c725-122">An application has been installed.</span></span><br/>                                                                                                                |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <span data-ttu-id="8c725-123"><dt>**Aplicación \_ de Desinstalar**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8c725-123"><dt>**APPLICATION\_UNINSTALL**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="8c725-124">Se ha desinstalado una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8c725-124">An application has been uninstalled.</span></span><br/>                                                                                                              |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <span data-ttu-id="8c725-125"><dt>**Dispositivo \_ de \_Instalación del controlador**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="8c725-125"><dt>**DEVICE\_DRIVER\_INSTALL**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="8c725-126">Se ha instalado un controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c725-126">A device driver has been installed.</span></span><br/>                                                                                                               |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <span data-ttu-id="8c725-127"><dt>**Modificar \_ CONFIGURACIÓN**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="8c725-127"><dt>**MODIFY\_SETTINGS**</dt> <dt>12</dt></span></span> </dl>                    | <span data-ttu-id="8c725-128">Una aplicación tiene características agregadas o eliminadas.</span><span class="sxs-lookup"><span data-stu-id="8c725-128">An application has had features added or removed.</span></span><br/>                                                                                                 |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <span data-ttu-id="8c725-129"><dt>**Cancelado \_ OPERACIÓN**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="8c725-129"><dt>**CANCELLED\_OPERATION**</dt> <dt>13</dt></span></span> </dl>        | <span data-ttu-id="8c725-130">Una aplicación debe eliminar el punto de restauración que creó.</span><span class="sxs-lookup"><span data-stu-id="8c725-130">An application needs to delete the restore point it created.</span></span> <span data-ttu-id="8c725-131">Por ejemplo, una aplicación usaría esta marca cuando un usuario cancela una instalación.</span><span class="sxs-lookup"><span data-stu-id="8c725-131">For example, an application would use this flag when a user cancels an installation.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8c725-132">*EventType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c725-132">*EventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c725-133">Tipo del evento.</span><span class="sxs-lookup"><span data-stu-id="8c725-133">The type of event.</span></span> <span data-ttu-id="8c725-134">Este miembro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8c725-134">This member can be one of the following values.</span></span>



| <span data-ttu-id="8c725-135">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="8c725-135">Event type</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="8c725-136">Significado</span><span class="sxs-lookup"><span data-stu-id="8c725-136">Meaning</span></span>                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <span data-ttu-id="8c725-137"><dt>**Inicio \_ de Cambio de \_ sistema \_ anidado**</dt> <dt>102</dt></span><span class="sxs-lookup"><span data-stu-id="8c725-137"><dt>**BEGIN\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>102</dt></span></span> </dl> | <span data-ttu-id="8c725-138">Ha empezado un cambio en el sistema.</span><span class="sxs-lookup"><span data-stu-id="8c725-138">A system change has begun.</span></span> <span data-ttu-id="8c725-139">Una llamada subsiguiente anidada no crea un nuevo punto de restauración.</span><span class="sxs-lookup"><span data-stu-id="8c725-139">A subsequent nested call does not create a new restore point.</span></span> <br/> <span data-ttu-id="8c725-140">Las llamadas subsiguientes deben usar END \_ Nested \_ System \_ Change, no end \_ System \_ Change.</span><span class="sxs-lookup"><span data-stu-id="8c725-140">Subsequent calls must use END\_NESTED\_SYSTEM\_CHANGE, not END\_SYSTEM\_CHANGE.</span></span><br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <span data-ttu-id="8c725-141"><dt>**Inicio \_ de \_Cambio del sistema**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="8c725-141"><dt>**BEGIN\_SYSTEM\_CHANGE**</dt> <dt>100</dt></span></span> </dl>                       | <span data-ttu-id="8c725-142">Ha empezado un cambio en el sistema.</span><span class="sxs-lookup"><span data-stu-id="8c725-142">A system change has begun.</span></span> <br/> <span data-ttu-id="8c725-143">Una llamada subsiguiente debe usar el \_ cambio del sistema final \_ , no el \_ \_ cambio del sistema anidado \_ .</span><span class="sxs-lookup"><span data-stu-id="8c725-143">A subsequent call must use END\_SYSTEM\_CHANGE, not END\_NESTED\_SYSTEM\_CHANGE.</span></span><br/>                                                              |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <span data-ttu-id="8c725-144"><dt>**Fin \_ de Cambio de \_ sistema \_ anidado**</dt> <dt>103</dt></span><span class="sxs-lookup"><span data-stu-id="8c725-144"><dt>**END\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>103</dt></span></span> </dl>       | <span data-ttu-id="8c725-145">Ha finalizado un cambio de sistema.</span><span class="sxs-lookup"><span data-stu-id="8c725-145">A system change has ended.</span></span><br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <span data-ttu-id="8c725-146"><dt>**Fin \_ de \_Cambio del sistema**</dt> <dt>101</dt></span><span class="sxs-lookup"><span data-stu-id="8c725-146"><dt>**END\_SYSTEM\_CHANGE**</dt> <dt>101</dt></span></span> </dl>                             | <span data-ttu-id="8c725-147">Ha finalizado un cambio de sistema.</span><span class="sxs-lookup"><span data-stu-id="8c725-147">A system change has ended.</span></span><br/>                                                                                                                                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c725-148">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c725-148">Return value</span></span>

<span data-ttu-id="8c725-149">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8c725-149">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8c725-150">De lo contrario, el método devuelve uno de los códigos de error COM definidos en WinError. h.</span><span class="sxs-lookup"><span data-stu-id="8c725-150">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c725-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c725-151">Remarks</span></span>

<span data-ttu-id="8c725-152">\* \* Windows 8: \* \*</span><span class="sxs-lookup"><span data-stu-id="8c725-152">\*\*Windows 8:  \*\*</span></span>

<span data-ttu-id="8c725-153">Una nueva clave del registro permite a los desarrolladores de aplicaciones cambiar la frecuencia de creación de puntos de restauración.</span><span class="sxs-lookup"><span data-stu-id="8c725-153">A new registry key enables application developers to change the frequency of restore-point creation.</span></span>

<span data-ttu-id="8c725-154">Las aplicaciones deben crear esta clave para usarla, ya que no existirá en el sistema.</span><span class="sxs-lookup"><span data-stu-id="8c725-154">Applications should create this key to use it because it will not preexist in the system.</span></span> <span data-ttu-id="8c725-155">De forma predeterminada, se aplicará lo siguiente si la clave no existe.</span><span class="sxs-lookup"><span data-stu-id="8c725-155">The following will apply by default if the key does not exist.</span></span> <span data-ttu-id="8c725-156">Si una aplicación llama al método **CreateRestorePoint** para crear un punto de restauración, Windows omite la creación de este nuevo punto de restauración si se ha creado algún punto de restauración en las últimas 24 horas.</span><span class="sxs-lookup"><span data-stu-id="8c725-156">If an application calls the **CreateRestorePoint** method to create a restore point, Windows skips creating this new restore point if any restore points have been created in the last 24 hours.</span></span> <span data-ttu-id="8c725-157">El método **CreateRestorePoint** devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8c725-157">The **CreateRestorePoint** method returns **S\_OK**.</span></span>

<span data-ttu-id="8c725-158">Los desarrolladores pueden escribir aplicaciones que creen el valor **DWORD** **SystemRestorePointCreationFrequency** en la clave del registro **HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore**.</span><span class="sxs-lookup"><span data-stu-id="8c725-158">Developers can write applications that create the **DWORD** value **SystemRestorePointCreationFrequency** under the registry key **HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\SystemRestore**.</span></span> <span data-ttu-id="8c725-159">El valor de esta clave del registro puede cambiar la frecuencia de creación de puntos de restauración.</span><span class="sxs-lookup"><span data-stu-id="8c725-159">The value of this registry key can change the frequency of restore point creation.</span></span> <span data-ttu-id="8c725-160">El valor de esta clave del registro puede cambiar la frecuencia de creación de puntos de restauración.</span><span class="sxs-lookup"><span data-stu-id="8c725-160">The value of this registry key can change the frequency of restore point creation.</span></span>

<span data-ttu-id="8c725-161">Si la aplicación llama a **CreateRestorePoint** para crear un punto de restauración y el valor de la clave del registro es 0, Restaurar sistema no omite la creación del nuevo punto de restauración.</span><span class="sxs-lookup"><span data-stu-id="8c725-161">If the application calls **CreateRestorePoint** to create a restore point, and the registry key value is 0, system restore does not skip creating the new restore point.</span></span>

<span data-ttu-id="8c725-162">Si la aplicación llama a **CreateRestorePoint** para crear un punto de restauración y el valor de la clave del registro es el entero n, Restaurar sistema omite la creación de un nuevo punto de restauración si se crearon puntos de restauración en los N minutos anteriores.</span><span class="sxs-lookup"><span data-stu-id="8c725-162">If the application calls **CreateRestorePoint** to create a restore point, and the registry key value is the integer N, system restore skips creating a new restore point if any restore points were created in the previous N minutes.</span></span>

## <a name="examples"></a><span data-ttu-id="8c725-163">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8c725-163">Examples</span></span>


```VB
'CreateRestorePoint Method of the SystemRestore Class
'Creates a restore point. Specifies the beginning and 
'the ending of a set of changes so that System Restore 
'can create a restore point.This method is the 
'scriptable equivalent of the SRSetRestorePoint function.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    RpName = Args.item(0)
Else 
    RpName = "Vbscript"
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.CreateRestorePoint(RpName, 0, 100)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="8c725-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c725-164">Requirements</span></span>



| <span data-ttu-id="8c725-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c725-165">Requirement</span></span> | <span data-ttu-id="8c725-166">Value</span><span class="sxs-lookup"><span data-stu-id="8c725-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8c725-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c725-167">Minimum supported client</span></span><br/> | <span data-ttu-id="8c725-168">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8c725-168">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8c725-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c725-169">Minimum supported server</span></span><br/> | <span data-ttu-id="8c725-170">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8c725-170">None supported</span></span><br/>                                                         |
| <span data-ttu-id="8c725-171">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8c725-171">Namespace</span></span><br/>                | <span data-ttu-id="8c725-172">Raíz \\ predeterminada</span><span class="sxs-lookup"><span data-stu-id="8c725-172">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="8c725-173">MOF</span><span class="sxs-lookup"><span data-stu-id="8c725-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c725-174"><dt>MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8c725-174"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c725-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c725-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c725-176">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="8c725-176">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





