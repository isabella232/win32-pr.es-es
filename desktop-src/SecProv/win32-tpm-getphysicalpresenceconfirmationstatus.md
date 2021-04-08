---
description: Indica si se requiere la confirmación de un usuario presente físicamente para una operación de presencia física determinada.
ms.assetid: 1CE558B7-EB6F-42CB-B52B-2A0101E90BD5
title: 'Win32_Tpm:: GetPhysicalPresenceConfirmationStatus (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceConfirmationStatus
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 61dc2798973a82cfc75c803f2bf8307c8a43b3c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002336"
---
# <a name="win32_tpmgetphysicalpresenceconfirmationstatus-method"></a><span data-ttu-id="5e5a4-103">Win32 \_ TPM:: GetPhysicalPresenceConfirmationStatus (método)</span><span class="sxs-lookup"><span data-stu-id="5e5a4-103">Win32\_Tpm::GetPhysicalPresenceConfirmationStatus method</span></span>

<span data-ttu-id="5e5a4-104">Indica si se requiere la confirmación de un usuario presente físicamente para una operación de presencia física determinada.</span><span class="sxs-lookup"><span data-stu-id="5e5a4-104">Indicates if confirmation from a physically present user is required for a given physical presence operation.</span></span>

<span data-ttu-id="5e5a4-105">Este método solo es accesible para los administradores locales.</span><span class="sxs-lookup"><span data-stu-id="5e5a4-105">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e5a4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e5a4-106">Syntax</span></span>


```C++
uint32 GetPhysicalPresenceConfirmationStatus(
  [in]  uint32 Operation,
  [out] uint32 ConfirmationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="5e5a4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e5a4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e5a4-108">*Operación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5e5a4-108">*Operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e5a4-109">Valor entero que especifica la operación de TPM solicitada que requiere presencia física.</span><span class="sxs-lookup"><span data-stu-id="5e5a4-109">An integer value that specifies the requested TPM operation that requires physical presence.</span></span> <span data-ttu-id="5e5a4-110">También se admiten comandos específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="5e5a4-110">Vendor specific commands are supported as well.</span></span>

<span data-ttu-id="5e5a4-111">El parámetro de *operación* puede constar de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="5e5a4-111">The *Operation* parameter may consist of the following values.</span></span>



| <span data-ttu-id="5e5a4-112">Value</span><span class="sxs-lookup"><span data-stu-id="5e5a4-112">Value</span></span>                                                                                                                               | <span data-ttu-id="5e5a4-113">Significado</span><span class="sxs-lookup"><span data-stu-id="5e5a4-113">Meaning</span></span>                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="5e5a4-114"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-114"><dt>1</dt></span></span> </dl>                                                        | <span data-ttu-id="5e5a4-115">Habilitar</span><span class="sxs-lookup"><span data-stu-id="5e5a4-115">Enable</span></span><br/>                                        |
| <dl> <span data-ttu-id="5e5a4-116"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-116"><dt>2</dt></span></span> </dl>                                                        | <span data-ttu-id="5e5a4-117">Disable</span><span class="sxs-lookup"><span data-stu-id="5e5a4-117">Disable</span></span><br/>                                       |
| <dl> <span data-ttu-id="5e5a4-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-118"><dt>3</dt></span></span> </dl>                                                        | <span data-ttu-id="5e5a4-119">Activar</span><span class="sxs-lookup"><span data-stu-id="5e5a4-119">Activate</span></span><br/>                                      |
| <dl> <span data-ttu-id="5e5a4-120"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-120"><dt>4</dt></span></span> </dl>                                                        | <span data-ttu-id="5e5a4-121">Desactivación</span><span class="sxs-lookup"><span data-stu-id="5e5a4-121">Deactivate</span></span><br/>                                    |
| <dl> <span data-ttu-id="5e5a4-122"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-122"><dt>5</dt></span></span> </dl>                                                        | <span data-ttu-id="5e5a4-123">Borrar</span><span class="sxs-lookup"><span data-stu-id="5e5a4-123">Clear</span></span><br/>                                         |
| <dl> <span data-ttu-id="5e5a4-124"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-124"><dt>6</dt></span></span> </dl>                                                        | <span data-ttu-id="5e5a4-125">Habilitar + activar</span><span class="sxs-lookup"><span data-stu-id="5e5a4-125">Enable + Activate</span></span><br/>                             |
| <dl> <span data-ttu-id="5e5a4-126"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-126"><dt>7</dt></span></span> </dl>                                                        | <span data-ttu-id="5e5a4-127">Desactivación y deshabilitación</span><span class="sxs-lookup"><span data-stu-id="5e5a4-127">Deactivate + Disable</span></span><br/>                          |
| <dl> <span data-ttu-id="5e5a4-128"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-128"><dt>8</dt></span></span> </dl>                                                        | <span data-ttu-id="5e5a4-129">SetOwnerInstall \_ true</span><span class="sxs-lookup"><span data-stu-id="5e5a4-129">SetOwnerInstall\_True</span></span><br/>                         |
| <dl> <span data-ttu-id="5e5a4-130"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-130"><dt>9</dt></span></span> </dl>                                                        | <span data-ttu-id="5e5a4-131">SetOwnerInstall \_ false</span><span class="sxs-lookup"><span data-stu-id="5e5a4-131">SetOwnerInstall\_False</span></span><br/>                        |
| <dl> <span data-ttu-id="5e5a4-132"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-132"><dt>10</dt></span></span> </dl>                                                       | <span data-ttu-id="5e5a4-133">Habilitar + Activar + SetOwnerInstall \_ true</span><span class="sxs-lookup"><span data-stu-id="5e5a4-133">Enable + Activate + SetOwnerInstall\_True</span></span><br/>     |
| <dl> <span data-ttu-id="5e5a4-134"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-134"><dt>11</dt></span></span> </dl>                                                       | <span data-ttu-id="5e5a4-135">SetOwnerInstall \_ false + desactivar + deshabilitar</span><span class="sxs-lookup"><span data-stu-id="5e5a4-135">SetOwnerInstall\_False + Deactivate + Disable</span></span><br/> |
| <dl> <span data-ttu-id="5e5a4-136"><dt></dt><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-136"><dt></dt> <dt>12</dt></span></span> </dl> | <span data-ttu-id="5e5a4-137">PresenceunownedFieldUpgrade físico diferida</span><span class="sxs-lookup"><span data-stu-id="5e5a4-137">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> |
| <dl> <span data-ttu-id="5e5a4-138"><dt></dt><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-138"><dt></dt> <dt>14</dt></span></span> </dl> | <span data-ttu-id="5e5a4-139">Clear + enable + Activate</span><span class="sxs-lookup"><span data-stu-id="5e5a4-139">Clear + Enable + Activate</span></span><br/>                     |
| <dl> <span data-ttu-id="5e5a4-140"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-140"><dt>15</dt></span></span> </dl>                                                       | <span data-ttu-id="5e5a4-141">SetNoPPIProvision \_ false</span><span class="sxs-lookup"><span data-stu-id="5e5a4-141">SetNoPPIProvision\_False</span></span><br/>                      |
| <dl> <span data-ttu-id="5e5a4-142"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-142"><dt>16</dt></span></span> </dl>                                                       | <span data-ttu-id="5e5a4-143">SetNoPPIProvision \_ true</span><span class="sxs-lookup"><span data-stu-id="5e5a4-143">SetNoPPIProvision\_True</span></span><br/>                       |
| <dl> <span data-ttu-id="5e5a4-144"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-144"><dt>17</dt></span></span> </dl>                                                       | <span data-ttu-id="5e5a4-145">SetNoPPIClear \_ false</span><span class="sxs-lookup"><span data-stu-id="5e5a4-145">SetNoPPIClear\_False</span></span><br/>                          |
| <dl> <span data-ttu-id="5e5a4-146"><dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-146"><dt>18</dt></span></span> </dl>                                                       | <span data-ttu-id="5e5a4-147">SetNoPPIClear \_ true</span><span class="sxs-lookup"><span data-stu-id="5e5a4-147">SetNoPPIClear\_True</span></span><br/>                           |
| <dl> <span data-ttu-id="5e5a4-148"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-148"><dt>19</dt></span></span> </dl>                                                       | <span data-ttu-id="5e5a4-149">SetNoPPIMaintenance \_ false</span><span class="sxs-lookup"><span data-stu-id="5e5a4-149">SetNoPPIMaintenance\_False</span></span><br/>                    |
| <dl> <span data-ttu-id="5e5a4-150"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-150"><dt>20</dt></span></span> </dl>                                                       | <span data-ttu-id="5e5a4-151">SetNoPPIMaintenance \_ true</span><span class="sxs-lookup"><span data-stu-id="5e5a4-151">SetNoPPIMaintenance\_True</span></span><br/>                     |
| <dl> <span data-ttu-id="5e5a4-152"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-152"><dt>21</dt></span></span> </dl>                                                       | <span data-ttu-id="5e5a4-153">Habilitar + Activar + borrar</span><span class="sxs-lookup"><span data-stu-id="5e5a4-153">Enable + Activate + Clear</span></span><br/>                     |
| <dl> <span data-ttu-id="5e5a4-154"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-154"><dt>22</dt></span></span> </dl>                                                       | <span data-ttu-id="5e5a4-155">Habilitar + Activar + desactivar + habilitar + activar</span><span class="sxs-lookup"><span data-stu-id="5e5a4-155">Enable + Activate + Clear + Enable + Activate</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5e5a4-156">*ConfirmationStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5e5a4-156">*ConfirmationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e5a4-157">Devuelve el estado de confirmación para el comando de presencia física.</span><span class="sxs-lookup"><span data-stu-id="5e5a4-157">Returns the confirmation status for physical presence command.</span></span>

<span data-ttu-id="5e5a4-158">El parámetro *ConfirmationStatus* puede constar de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="5e5a4-158">The *ConfirmationStatus* parameter may consist of the following values.</span></span>



| <span data-ttu-id="5e5a4-159">Value</span><span class="sxs-lookup"><span data-stu-id="5e5a4-159">Value</span></span>                                                                        | <span data-ttu-id="5e5a4-160">Significado</span><span class="sxs-lookup"><span data-stu-id="5e5a4-160">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5e5a4-161"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-161"><dt>0</dt></span></span> </dl> | <span data-ttu-id="5e5a4-162">No implementado</span><span class="sxs-lookup"><span data-stu-id="5e5a4-162">Not implemented</span></span><br/>                                             |
| <dl> <span data-ttu-id="5e5a4-163"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-163"><dt>1</dt></span></span> </dl> | <span data-ttu-id="5e5a4-164">Solo BIOS.</span><span class="sxs-lookup"><span data-stu-id="5e5a4-164">BIOS only.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="5e5a4-165"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-165"><dt>2</dt></span></span> </dl> | <span data-ttu-id="5e5a4-166">Bloqueada para el sistema operativo mediante la configuración del BIOS.</span><span class="sxs-lookup"><span data-stu-id="5e5a4-166">Blocked for the operating system by the BIOS configuration.</span></span><br/> |
| <dl> <span data-ttu-id="5e5a4-167"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-167"><dt>3</dt></span></span> </dl> | <span data-ttu-id="5e5a4-168">Permitido y presente físicamente el usuario requerido.</span><span class="sxs-lookup"><span data-stu-id="5e5a4-168">Allowed and physically present user required.</span></span><br/>               |
| <dl> <span data-ttu-id="5e5a4-169"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-169"><dt>4</dt></span></span> </dl> | <span data-ttu-id="5e5a4-170">No se requiere el usuario presente y presente físicamente</span><span class="sxs-lookup"><span data-stu-id="5e5a4-170">Allowed and physically present user not required</span></span><br/>            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e5a4-171">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e5a4-171">Return value</span></span>

<span data-ttu-id="5e5a4-172">Se pueden devolver todos los errores de TPM, así como los errores específicos de los [servicios base de TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="5e5a4-172">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="5e5a4-173">A continuación se enumeran los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="5e5a4-173">Common return codes are listed below.</span></span>



| <span data-ttu-id="5e5a4-174">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e5a4-174">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="5e5a4-175">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e5a4-175">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="5e5a4-176"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-176"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="5e5a4-177">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5e5a4-177">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5e5a4-178">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e5a4-178">Remarks</span></span>

<span data-ttu-id="5e5a4-179">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5e5a4-179">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5e5a4-180">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="5e5a4-180">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5e5a4-181">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="5e5a4-181">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5e5a4-182">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5e5a4-182">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e5a4-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e5a4-183">Requirements</span></span>



| <span data-ttu-id="5e5a4-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e5a4-184">Requirement</span></span> | <span data-ttu-id="5e5a4-185">Value</span><span class="sxs-lookup"><span data-stu-id="5e5a4-185">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e5a4-186">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e5a4-186">Minimum supported client</span></span><br/> | <span data-ttu-id="5e5a4-187">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e5a4-187">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5e5a4-188">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e5a4-188">Minimum supported server</span></span><br/> | <span data-ttu-id="5e5a4-189">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e5a4-189">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5e5a4-190">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5e5a4-190">Namespace</span></span><br/>                | <span data-ttu-id="5e5a4-191">\\\\.\\ \\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="5e5a4-191">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="5e5a4-192">MOF</span><span class="sxs-lookup"><span data-stu-id="5e5a4-192">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e5a4-193"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-193"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e5a4-194">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e5a4-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e5a4-195"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a4-195"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e5a4-196">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e5a4-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e5a4-197">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="5e5a4-197">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
