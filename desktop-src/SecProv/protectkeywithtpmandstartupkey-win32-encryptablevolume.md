---
description: Si el Módulo de plataforma segura (TPM) está disponible, este método protege la clave de cifrado del volumen mejorada por una clave externa.
ms.assetid: 58bc2de7-645f-4049-949c-975062f8c8ce
title: Método ProtectKeyWithTPMAndStartupKey de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndStartupKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 06ab2b9474b3564a567374490d9aeb70448338be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666385"
---
# <a name="protectkeywithtpmandstartupkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="431a7-103">Método ProtectKeyWithTPMAndStartupKey de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="431a7-103">ProtectKeyWithTPMAndStartupKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="431a7-104">El método **ProtectKeyWithTPMAndStartupKey** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) protege la clave de cifrado del volumen mediante el hardware de seguridad de módulo de plataforma segura (TPM) del equipo, si está disponible, mejorado por una clave externa que se debe presentar al equipo en el inicio.</span><span class="sxs-lookup"><span data-stu-id="431a7-104">The **ProtectKeyWithTPMAndStartupKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available, enhanced by an external key that must be presented to the computer at startup.</span></span>

<span data-ttu-id="431a7-105">Tanto la validación por el TPM como la entrada de un dispositivo de memoria USB que contiene la clave externa son necesarias para tener acceso a la clave de cifrado del volumen y desbloquear el contenido del volumen.</span><span class="sxs-lookup"><span data-stu-id="431a7-105">Both validation by the TPM and input of a USB memory device that contains the external key are necessary to access the volume's encryption key and unlock the volume contents.</span></span> <span data-ttu-id="431a7-106">Use el método [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) para guardar esta clave externa en un archivo en un dispositivo de memoria USB para su uso como clave de inicio.</span><span class="sxs-lookup"><span data-stu-id="431a7-106">Use the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method to save this external key to a file on a USB memory device for usage as a startup key.</span></span>

<span data-ttu-id="431a7-107">Este método solo es aplicable para el volumen que contiene el sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="431a7-107">This method is only applicable for the volume that contains the currently running operating system.</span></span>

<span data-ttu-id="431a7-108">Se crea un protector de clave de tipo "TPM y clave de inicio" para el volumen, si todavía no existe uno.</span><span class="sxs-lookup"><span data-stu-id="431a7-108">A key protector of type "TPM And Startup Key" is created for the volume, if one does not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="431a7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="431a7-109">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPMAndStartupKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="431a7-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="431a7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="431a7-111">*FriendlyName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="431a7-111">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="431a7-112">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="431a7-112">Type: **string**</span></span>

<span data-ttu-id="431a7-113">Identificador de cadena asignado por el usuario para este protector de clave.</span><span class="sxs-lookup"><span data-stu-id="431a7-113">A user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="431a7-114">Si no se especifica este parámetro, se utiliza un valor en blanco.</span><span class="sxs-lookup"><span data-stu-id="431a7-114">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="431a7-115">*PlatformValidationProfile* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="431a7-115">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="431a7-116">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="431a7-116">Type: **uint8\[\]**</span></span>

<span data-ttu-id="431a7-117">Matriz de enteros que especifica el modo en que el hardware de seguridad del Módulo de plataforma segura (TPM) del equipo protege la clave de cifrado del volumen de disco.</span><span class="sxs-lookup"><span data-stu-id="431a7-117">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the encryption key of the disk volume.</span></span>

<span data-ttu-id="431a7-118">Un perfil de validación de plataforma consta de un conjunto de índices de registro de configuración de plataforma (PCR) que van de 0 a 23, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="431a7-118">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="431a7-119">Los valores de repetición del parámetro se omiten.</span><span class="sxs-lookup"><span data-stu-id="431a7-119">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="431a7-120">Cada índice de PCR está asociado a los servicios que se ejecutan cuando se inicia el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="431a7-120">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="431a7-121">Cada vez que se inicia el equipo, el TPM comprobará que los servicios especificados en el perfil de validación de plataforma no han cambiado.</span><span class="sxs-lookup"><span data-stu-id="431a7-121">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="431a7-122">Si alguno de estos servicios cambia mientras la protección de Cifrado de unidad BitLocker (BDE) permanece en ON, el TPM no liberará la clave de cifrado para desbloquear el volumen del disco y el equipo entrará en modo de recuperación.</span><span class="sxs-lookup"><span data-stu-id="431a7-122">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume, and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="431a7-123">Si se especifica este parámetro mientras se ha habilitado el valor de la directiva de grupo correspondiente, debe coincidir con la configuración de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="431a7-123">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="431a7-124">Si no se especifica este parámetro, se usa el valor predeterminado de 0, 2, 4, 5, 8, 9, 10 y 11.</span><span class="sxs-lookup"><span data-stu-id="431a7-124">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="431a7-125">El perfil de validación de plataforma predeterminado protege la clave de cifrado frente a los cambios en los elementos siguientes:</span><span class="sxs-lookup"><span data-stu-id="431a7-125">The default platform validation profile secures the encryption key against changes to the following elements:</span></span>

-   <span data-ttu-id="431a7-126">Raíz principal de la confianza de la medida (CRTM)</span><span class="sxs-lookup"><span data-stu-id="431a7-126">Core Root of Trust of Measurement (CRTM)</span></span>
-   <span data-ttu-id="431a7-127">BIOS</span><span class="sxs-lookup"><span data-stu-id="431a7-127">BIOS</span></span>
-   <span data-ttu-id="431a7-128">Extensiones de la plataforma (PCR 0)</span><span class="sxs-lookup"><span data-stu-id="431a7-128">Platform Extensions (PCR 0)</span></span>
-   <span data-ttu-id="431a7-129">Código ROM de opción (PCR 2)</span><span class="sxs-lookup"><span data-stu-id="431a7-129">Option ROM Code (PCR 2)</span></span>
-   <span data-ttu-id="431a7-130">Código de registro de arranque maestro (MBR) (PCR 4)</span><span class="sxs-lookup"><span data-stu-id="431a7-130">Master Boot Record (MBR) Code (PCR 4)</span></span>
-   <span data-ttu-id="431a7-131">Tabla de partición de registro de arranque maestro (MBR) (PCR 5)</span><span class="sxs-lookup"><span data-stu-id="431a7-131">Master Boot Record (MBR) Partition Table (PCR 5)</span></span>
-   <span data-ttu-id="431a7-132">Sector de arranque de NTFS (PCR 8)</span><span class="sxs-lookup"><span data-stu-id="431a7-132">NTFS Boot Sector (PCR 8)</span></span>
-   <span data-ttu-id="431a7-133">Bloque de arranque de NTFS (PCR 9)</span><span class="sxs-lookup"><span data-stu-id="431a7-133">NTFS Boot Block (PCR 9)</span></span>
-   <span data-ttu-id="431a7-134">Administración de arranque (PCR 10)</span><span class="sxs-lookup"><span data-stu-id="431a7-134">Boot Manager (PCR 10)</span></span>
-   <span data-ttu-id="431a7-135">Control de acceso de BitLocker (PCR 11)</span><span class="sxs-lookup"><span data-stu-id="431a7-135">BitLocker Access Control (PCR 11)</span></span>

<span data-ttu-id="431a7-136">Para la seguridad del equipo, se recomienda el perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="431a7-136">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="431a7-137">Para obtener protección adicional frente a los cambios de configuración de inicio temprano, use un perfil de PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="431a7-137">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span> <span data-ttu-id="431a7-138">De forma predeterminada, los equipos basados en Unified Extensible Firmware Interface (UEFI) no usan PCR 5.</span><span class="sxs-lookup"><span data-stu-id="431a7-138">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span>

<span data-ttu-id="431a7-139">Cambiar desde el perfil predeterminado afecta a la seguridad y la capacidad de administración del equipo.</span><span class="sxs-lookup"><span data-stu-id="431a7-139">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="431a7-140">La confidencialidad de las modificaciones de BitLocker a plataforma (malintencionadas o autorizadas) aumenta o disminuye en función de la inclusión o exclusión, respectivamente, de las PCR.</span><span class="sxs-lookup"><span data-stu-id="431a7-140">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="431a7-141">Para habilitar la protección de BitLocker, el perfil de validación de plataforma debe incluir PCR 11.</span><span class="sxs-lookup"><span data-stu-id="431a7-141">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="431a7-142">Value</span><span class="sxs-lookup"><span data-stu-id="431a7-142">Value</span></span>                                                                         | <span data-ttu-id="431a7-143">Significado</span><span class="sxs-lookup"><span data-stu-id="431a7-143">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="431a7-144"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-144"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="431a7-145">Raíz principal de la confianza de medición (CRTM), BIOS y extensiones de plataforma</span><span class="sxs-lookup"><span data-stu-id="431a7-145">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="431a7-146"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-146"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="431a7-147">Configuración y datos de la plataforma y la placa base</span><span class="sxs-lookup"><span data-stu-id="431a7-147">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="431a7-148"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-148"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="431a7-149">Código ROM de opción</span><span class="sxs-lookup"><span data-stu-id="431a7-149">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="431a7-150"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-150"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="431a7-151">Configuración y datos de ROM de opción</span><span class="sxs-lookup"><span data-stu-id="431a7-151">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="431a7-152"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-152"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="431a7-153">Código de registro de arranque maestro (MBR)</span><span class="sxs-lookup"><span data-stu-id="431a7-153">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="431a7-154"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-154"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="431a7-155">Tabla de partición de registro de arranque maestro (MBR)</span><span class="sxs-lookup"><span data-stu-id="431a7-155">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="431a7-156"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-156"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="431a7-157">Transición de estado y eventos de activación</span><span class="sxs-lookup"><span data-stu-id="431a7-157">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="431a7-158"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-158"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="431a7-159">Manufacturer-Specific de equipo</span><span class="sxs-lookup"><span data-stu-id="431a7-159">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="431a7-160"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-160"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="431a7-161">Sector de arranque de NTFS</span><span class="sxs-lookup"><span data-stu-id="431a7-161">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="431a7-162"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-162"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="431a7-163">Bloque de arranque de NTFS</span><span class="sxs-lookup"><span data-stu-id="431a7-163">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="431a7-164"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-164"><dt>10</dt></span></span> </dl> | <span data-ttu-id="431a7-165">Administrador de arranque</span><span class="sxs-lookup"><span data-stu-id="431a7-165">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="431a7-166"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-166"><dt>11</dt></span></span> </dl> | <span data-ttu-id="431a7-167">Access Control de BitLocker</span><span class="sxs-lookup"><span data-stu-id="431a7-167">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="431a7-168"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-168"><dt>12</dt></span></span> </dl> | <span data-ttu-id="431a7-169">Definido para que lo use el sistema operativo estático</span><span class="sxs-lookup"><span data-stu-id="431a7-169">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="431a7-170"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-170"><dt>13</dt></span></span> </dl> | <span data-ttu-id="431a7-171">Definido para que lo use el sistema operativo estático</span><span class="sxs-lookup"><span data-stu-id="431a7-171">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="431a7-172"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-172"><dt>14</dt></span></span> </dl> | <span data-ttu-id="431a7-173">Definido para que lo use el sistema operativo estático</span><span class="sxs-lookup"><span data-stu-id="431a7-173">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="431a7-174"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-174"><dt>15</dt></span></span> </dl> | <span data-ttu-id="431a7-175">Definido para que lo use el sistema operativo estático</span><span class="sxs-lookup"><span data-stu-id="431a7-175">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="431a7-176"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-176"><dt>16</dt></span></span> </dl> | <span data-ttu-id="431a7-177">Se usa para la depuración</span><span class="sxs-lookup"><span data-stu-id="431a7-177">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="431a7-178"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-178"><dt>17</dt></span></span> </dl> | <span data-ttu-id="431a7-179">CRTM dinámico</span><span class="sxs-lookup"><span data-stu-id="431a7-179">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="431a7-180"><dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-180"><dt>18</dt></span></span> </dl> | <span data-ttu-id="431a7-181">Plataforma definida</span><span class="sxs-lookup"><span data-stu-id="431a7-181">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="431a7-182"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-182"><dt>19</dt></span></span> </dl> | <span data-ttu-id="431a7-183">Usado por un sistema operativo de confianza</span><span class="sxs-lookup"><span data-stu-id="431a7-183">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="431a7-184"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-184"><dt>20</dt></span></span> </dl> | <span data-ttu-id="431a7-185">Usado por un sistema operativo de confianza</span><span class="sxs-lookup"><span data-stu-id="431a7-185">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="431a7-186"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-186"><dt>21</dt></span></span> </dl> | <span data-ttu-id="431a7-187">Usado por un sistema operativo de confianza</span><span class="sxs-lookup"><span data-stu-id="431a7-187">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="431a7-188"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-188"><dt>22</dt></span></span> </dl> | <span data-ttu-id="431a7-189">Usado por un sistema operativo de confianza</span><span class="sxs-lookup"><span data-stu-id="431a7-189">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="431a7-190"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-190"><dt>23</dt></span></span> </dl> | <span data-ttu-id="431a7-191">Compatibilidad con aplicaciones</span><span class="sxs-lookup"><span data-stu-id="431a7-191">Application support</span></span><br/>                                                     |



 

</dd> <dt>

<span data-ttu-id="431a7-192">*ExternalKey* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="431a7-192">*ExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="431a7-193">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="431a7-193">Type: **uint8\[\]**</span></span>

<span data-ttu-id="431a7-194">Matriz de bytes que especifica la clave externa de 256 bits usada para desbloquear el volumen cuando se inicia el equipo.</span><span class="sxs-lookup"><span data-stu-id="431a7-194">An array of bytes that specifies the 256-bit external key used to unlock the volume when the computer starts.</span></span>

<span data-ttu-id="431a7-195">Si no se especifica ninguna clave externa, se genera una de forma aleatoria.</span><span class="sxs-lookup"><span data-stu-id="431a7-195">If no external key is specified, one is randomly generated.</span></span> <span data-ttu-id="431a7-196">Use el método [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) para obtener la clave generada de forma aleatoria.</span><span class="sxs-lookup"><span data-stu-id="431a7-196">Use the [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) method to obtain the randomly generated key.</span></span>

</dd> <dt>

<span data-ttu-id="431a7-197">*VolumeKeyProtectorID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="431a7-197">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="431a7-198">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="431a7-198">Type: **string**</span></span>

<span data-ttu-id="431a7-199">Una cadena que es el identificador único asociado al protector de clave creado que se puede usar para administrar el protector de clave.</span><span class="sxs-lookup"><span data-stu-id="431a7-199">A string that is the unique identifier associated with the created key protector that can be used to manage the key protector.</span></span>

<span data-ttu-id="431a7-200">Si la unidad admite el cifrado de hardware y BitLocker no ha tomado propiedad de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos de cada banda.</span><span class="sxs-lookup"><span data-stu-id="431a7-200">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="431a7-201">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="431a7-201">Return value</span></span>

<span data-ttu-id="431a7-202">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="431a7-202">Type: **uint32**</span></span>

<span data-ttu-id="431a7-203">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="431a7-203">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="431a7-204">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="431a7-204">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="431a7-205">Descripción</span><span class="sxs-lookup"><span data-stu-id="431a7-205">Description</span></span>                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="431a7-206"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-206"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="431a7-207">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="431a7-207">The method was successful.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="431a7-208"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-208"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>        | <span data-ttu-id="431a7-209">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="431a7-209">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="431a7-210"><dt>**TBS \_ El \_ servicio E \_ no se \_ está ejecutando**</dt> <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-210"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl> | <span data-ttu-id="431a7-211">No se encuentra ningún TPM compatible en este equipo.</span><span class="sxs-lookup"><span data-stu-id="431a7-211">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="431a7-212"><dt>**FVE \_ \_ \_ Volumen externo E**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-212"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>       | <span data-ttu-id="431a7-213">El TPM no puede proteger la clave de cifrado del volumen porque el volumen no contiene el sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="431a7-213">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                                                                                                               |
| <dl> <span data-ttu-id="431a7-214"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-214"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="431a7-215">Se proporciona el parámetro *PlatformValidationProfile* , pero sus valores no están dentro del intervalo conocido o no coinciden con la configuración de directiva de grupo actualmente en vigor.</span><span class="sxs-lookup"><span data-stu-id="431a7-215">The *PlatformValidationProfile* parameter is provided, but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> <span data-ttu-id="431a7-216">Se proporciona el parámetro *ExternalKey* , pero no es una matriz de tamaño 32.</span><span class="sxs-lookup"><span data-stu-id="431a7-216">The *ExternalKey* parameter is provided but is not an array of size 32.</span></span><br/> |
| <dl> <span data-ttu-id="431a7-217"><dt>**FVE \_ E \_ \_ CDDVD de arranque**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-217"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>       | <span data-ttu-id="431a7-218">En este equipo se encuentra un CD/DVD de arranque.</span><span class="sxs-lookup"><span data-stu-id="431a7-218">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="431a7-219">Quite el CD o el DVD y reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="431a7-219">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="431a7-220"><dt>**FVE \_ El \_ protector E \_ existe**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-220"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>     | <span data-ttu-id="431a7-221">Ya existe un protector de clave de este tipo.</span><span class="sxs-lookup"><span data-stu-id="431a7-221">A key protector of this type already exists.</span></span><br/>                                                                                                                                                                                                                |



 

## <a name="security-considerations"></a><span data-ttu-id="431a7-222">Consideraciones sobre la seguridad</span><span class="sxs-lookup"><span data-stu-id="431a7-222">Security Considerations</span></span>

<span data-ttu-id="431a7-223">Para la seguridad del equipo, se recomienda el perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="431a7-223">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="431a7-224">Para obtener una protección adicional frente a los cambios en el código de inicio temprano, use un perfil de PCRs 0, 2, 4, 5, 8, 9, 10 y 11.</span><span class="sxs-lookup"><span data-stu-id="431a7-224">For additional protection against early startup code changes, use a profile of PCRs 0, 2, 4, 5, 8, 9, 10, and 11.</span></span> <span data-ttu-id="431a7-225">Para obtener protección adicional frente a los cambios de configuración de inicio temprano, use un perfil de PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="431a7-225">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="431a7-226">Cambiar desde el perfil predeterminado afecta a la seguridad o la facilidad de uso del equipo.</span><span class="sxs-lookup"><span data-stu-id="431a7-226">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="431a7-227">Observaciones</span><span class="sxs-lookup"><span data-stu-id="431a7-227">Remarks</span></span>

<span data-ttu-id="431a7-228">Como máximo, un protector de clave del tipo "TPM y clave de inicio" puede existir para un volumen en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="431a7-228">At most one key protector of type "TPM And Startup Key" can exist for a volume at any time.</span></span> <span data-ttu-id="431a7-229">Si desea cambiar el nombre para mostrar o el perfil de validación de plataforma usado por un protector de clave "TPM Plus key" existente, primero debe quitar el protector de clave existente y, a continuación, llamar a **ProtectKeyWithTPMAndStartupKey** para crear uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="431a7-229">If you want to change the display name or the platform validation profile used by an existing "TPM plus Startup Key" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPMAndStartupKey** to create a new one.</span></span> <span data-ttu-id="431a7-230">Se deben especificar protectores de clave adicionales para desbloquear el volumen en escenarios de recuperación en los que no se puede obtener acceso a la clave de cifrado del volumen. por ejemplo, cuando el TPM no se puede validar correctamente con el perfil de validación de plataforma o cuando se pierde la memoria USB que contiene la clave externa.</span><span class="sxs-lookup"><span data-stu-id="431a7-230">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile or when USB memory that contains the external key is lost.</span></span>

<span data-ttu-id="431a7-231">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) o [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) para crear uno o varios protectores de clave para recuperar un volumen bloqueado de otro modo.</span><span class="sxs-lookup"><span data-stu-id="431a7-231">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="431a7-232">Aunque es posible tener un protector de clave del tipo "TPM" y otro del tipo "TPM y clave de inicio", la presencia del tipo de protector de clave "TPM" niega los efectos de otros protectores de clave basados en TPM.</span><span class="sxs-lookup"><span data-stu-id="431a7-232">While it is possible to have both a key protector of the type "TPM" and another of the type "TPM And Startup Key", the presence of the "TPM" key protector type negates the effects of other TPM-based key protectors.</span></span>

<span data-ttu-id="431a7-233">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="431a7-233">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="431a7-234">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="431a7-234">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="431a7-235">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="431a7-235">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="431a7-236">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="431a7-236">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="431a7-237">Requisitos</span><span class="sxs-lookup"><span data-stu-id="431a7-237">Requirements</span></span>



| <span data-ttu-id="431a7-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="431a7-238">Requirement</span></span> | <span data-ttu-id="431a7-239">Value</span><span class="sxs-lookup"><span data-stu-id="431a7-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="431a7-240">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="431a7-240">Minimum supported client</span></span><br/> | <span data-ttu-id="431a7-241">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="431a7-241">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="431a7-242">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="431a7-242">Minimum supported server</span></span><br/> | <span data-ttu-id="431a7-243">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="431a7-243">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="431a7-244">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="431a7-244">Namespace</span></span><br/>                | <span data-ttu-id="431a7-245">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="431a7-245">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="431a7-246">MOF</span><span class="sxs-lookup"><span data-stu-id="431a7-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="431a7-247"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="431a7-247"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="431a7-248">Vea también</span><span class="sxs-lookup"><span data-stu-id="431a7-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="431a7-249">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="431a7-249">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="431a7-250">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="431a7-250">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
