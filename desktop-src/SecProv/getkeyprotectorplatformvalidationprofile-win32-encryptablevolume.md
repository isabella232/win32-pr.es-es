---
description: Recupera el perfil de validación de plataforma para un protector de clave determinado del tipo adecuado.
ms.assetid: 45fa6ba7-169c-4753-8586-0029a7650acc
title: Método GetKeyProtectorPlatformValidationProfile de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorPlatformValidationProfile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b9b951d3ce9eab52687730831f7052942fcbec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688154"
---
# <a name="getkeyprotectorplatformvalidationprofile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="20563-103">Método GetKeyProtectorPlatformValidationProfile de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="20563-103">GetKeyProtectorPlatformValidationProfile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="20563-104">El método **GetKeyProtectorPlatformValidationProfile** recupera el perfil de validación de plataforma para un protector de clave determinado del tipo adecuado.</span><span class="sxs-lookup"><span data-stu-id="20563-104">The **GetKeyProtectorPlatformValidationProfile** method retrieves the platform validation profile for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="20563-105">El identificador de protector de clave debe hacer referencia a un protector de clave de tipo "TPM", "TPM y PIN", "TPM y PIN y clave de inicio", o "TPM y clave de inicio".</span><span class="sxs-lookup"><span data-stu-id="20563-105">The key protector identifier must refer to a key protector of type "TPM", "TPM And PIN", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="20563-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20563-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorPlatformValidationProfile(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PlatformValidationProfile[]
);
```



## <a name="parameters"></a><span data-ttu-id="20563-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20563-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20563-108">*VolumeKeyProtectorID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="20563-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20563-109">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="20563-109">Type: **string**</span></span>

<span data-ttu-id="20563-110">Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="20563-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="20563-111">*PlatformValidationProfile* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="20563-111">*PlatformValidationProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20563-112">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="20563-112">Type: **uint8\[\]**</span></span>

<span data-ttu-id="20563-113">Matriz de enteros que especifica cómo el hardware de seguridad del Módulo de plataforma segura (TPM) del equipo protege la clave de cifrado del volumen de disco.</span><span class="sxs-lookup"><span data-stu-id="20563-113">An array of integers that specifies how the Trusted Platform Module (TPM) Security Hardware of the computer secures the encryption key of the disk volume.</span></span>



| <span data-ttu-id="20563-114">Value</span><span class="sxs-lookup"><span data-stu-id="20563-114">Value</span></span>                                                                         | <span data-ttu-id="20563-115">Significado</span><span class="sxs-lookup"><span data-stu-id="20563-115">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="20563-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="20563-116"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="20563-117">Raíz principal de la confianza de medición (CRTM), BIOS y extensiones de plataforma</span><span class="sxs-lookup"><span data-stu-id="20563-117">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="20563-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="20563-118"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="20563-119">Configuración y datos de la plataforma y la placa base</span><span class="sxs-lookup"><span data-stu-id="20563-119">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="20563-120"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="20563-120"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="20563-121">Código ROM de opción</span><span class="sxs-lookup"><span data-stu-id="20563-121">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="20563-122"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="20563-122"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="20563-123">Configuración y datos de ROM de opción</span><span class="sxs-lookup"><span data-stu-id="20563-123">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="20563-124"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="20563-124"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="20563-125">Código de registro de arranque maestro (MBR)</span><span class="sxs-lookup"><span data-stu-id="20563-125">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="20563-126"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="20563-126"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="20563-127">Tabla de partición de registro de arranque maestro (MBR)</span><span class="sxs-lookup"><span data-stu-id="20563-127">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="20563-128"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="20563-128"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="20563-129">Transición de estado y eventos de activación</span><span class="sxs-lookup"><span data-stu-id="20563-129">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="20563-130"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="20563-130"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="20563-131">Manufacturer-Specific de equipo</span><span class="sxs-lookup"><span data-stu-id="20563-131">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="20563-132"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="20563-132"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="20563-133">Sector de arranque de NTFS</span><span class="sxs-lookup"><span data-stu-id="20563-133">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="20563-134"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="20563-134"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="20563-135">Bloque de arranque de NTFS</span><span class="sxs-lookup"><span data-stu-id="20563-135">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="20563-136"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="20563-136"><dt>10</dt></span></span> </dl> | <span data-ttu-id="20563-137">Administrador de arranque</span><span class="sxs-lookup"><span data-stu-id="20563-137">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="20563-138"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="20563-138"><dt>11</dt></span></span> </dl> | <span data-ttu-id="20563-139">Access Control de BitLocker</span><span class="sxs-lookup"><span data-stu-id="20563-139">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="20563-140"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="20563-140"><dt>12</dt></span></span> </dl> | <span data-ttu-id="20563-141">Definido para que lo use el sistema operativo estático</span><span class="sxs-lookup"><span data-stu-id="20563-141">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="20563-142"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="20563-142"><dt>13</dt></span></span> </dl> | <span data-ttu-id="20563-143">Definido para que lo use el sistema operativo estático</span><span class="sxs-lookup"><span data-stu-id="20563-143">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="20563-144"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="20563-144"><dt>14</dt></span></span> </dl> | <span data-ttu-id="20563-145">Definido para que lo use el sistema operativo estático</span><span class="sxs-lookup"><span data-stu-id="20563-145">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="20563-146"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="20563-146"><dt>15</dt></span></span> </dl> | <span data-ttu-id="20563-147">Definido para que lo use el sistema operativo estático</span><span class="sxs-lookup"><span data-stu-id="20563-147">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="20563-148"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="20563-148"><dt>16</dt></span></span> </dl> | <span data-ttu-id="20563-149">Se usa para la depuración</span><span class="sxs-lookup"><span data-stu-id="20563-149">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="20563-150"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="20563-150"><dt>17</dt></span></span> </dl> | <span data-ttu-id="20563-151">CRTM dinámico</span><span class="sxs-lookup"><span data-stu-id="20563-151">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="20563-152"><dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="20563-152"><dt>18</dt></span></span> </dl> | <span data-ttu-id="20563-153">Plataforma definida</span><span class="sxs-lookup"><span data-stu-id="20563-153">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="20563-154"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="20563-154"><dt>19</dt></span></span> </dl> | <span data-ttu-id="20563-155">Usado por un sistema operativo de confianza</span><span class="sxs-lookup"><span data-stu-id="20563-155">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="20563-156"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="20563-156"><dt>20</dt></span></span> </dl> | <span data-ttu-id="20563-157">Usado por un sistema operativo de confianza</span><span class="sxs-lookup"><span data-stu-id="20563-157">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="20563-158"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="20563-158"><dt>21</dt></span></span> </dl> | <span data-ttu-id="20563-159">Usado por un sistema operativo de confianza</span><span class="sxs-lookup"><span data-stu-id="20563-159">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="20563-160"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="20563-160"><dt>22</dt></span></span> </dl> | <span data-ttu-id="20563-161">Usado por un sistema operativo de confianza</span><span class="sxs-lookup"><span data-stu-id="20563-161">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="20563-162"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="20563-162"><dt>23</dt></span></span> </dl> | <span data-ttu-id="20563-163">Compatibilidad con aplicaciones</span><span class="sxs-lookup"><span data-stu-id="20563-163">Application support</span></span><br/>                                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20563-164">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20563-164">Return value</span></span>

<span data-ttu-id="20563-165">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20563-165">Type: **uint32**</span></span>

<span data-ttu-id="20563-166">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="20563-166">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="20563-167">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20563-167">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="20563-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="20563-168">Description</span></span>                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="20563-169"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="20563-169"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="20563-170">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="20563-170">The method was successful.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="20563-171"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="20563-171"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="20563-172">El parámetro *VolumeKeyProtectorID* no hace referencia a un protector de clave del tipo "TPM", "TPM y PIN", "TPM y PIN y clave de inicio", o "TPM y clave de inicio".</span><span class="sxs-lookup"><span data-stu-id="20563-172">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "TPM", "TPM And PIN", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span><br/> |
| <dl> <span data-ttu-id="20563-173"><dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="20563-173"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="20563-174">BitLocker no está habilitado en el volumen.</span><span class="sxs-lookup"><span data-stu-id="20563-174">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="20563-175">Agregue un protector de clave para habilitar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="20563-175">Add a key protector to enable BitLocker.</span></span><br/>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="20563-176">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20563-176">Remarks</span></span>

<span data-ttu-id="20563-177">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="20563-177">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="20563-178">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="20563-178">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="20563-179">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="20563-179">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="20563-180">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="20563-180">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20563-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20563-181">Requirements</span></span>



| <span data-ttu-id="20563-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="20563-182">Requirement</span></span> | <span data-ttu-id="20563-183">Value</span><span class="sxs-lookup"><span data-stu-id="20563-183">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20563-184">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20563-184">Minimum supported client</span></span><br/> | <span data-ttu-id="20563-185">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="20563-185">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="20563-186">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20563-186">Minimum supported server</span></span><br/> | <span data-ttu-id="20563-187">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="20563-187">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="20563-188">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="20563-188">Namespace</span></span><br/>                | <span data-ttu-id="20563-189">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="20563-189">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="20563-190">MOF</span><span class="sxs-lookup"><span data-stu-id="20563-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20563-191"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20563-191"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20563-192">Vea también</span><span class="sxs-lookup"><span data-stu-id="20563-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20563-193">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="20563-193">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
