---
description: Si el Módulo de plataforma segura (TPM) está disponible, este método protege la clave de cifrado del volumen.
ms.assetid: 79bee9ca-c86a-482b-a06f-1cfb887e7fae
title: Método ProtectKeyWithTPM de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPM
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0369e44d96a4f1dcacf33dbf1b1da6ad6d37eed2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668008"
---
# <a name="protectkeywithtpm-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="e1595-103">Método ProtectKeyWithTPM de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="e1595-103">ProtectKeyWithTPM method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="e1595-104">El método **ProtectKeyWithTPM** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) protege la clave de cifrado del volumen mediante el hardware de seguridad de módulo de plataforma segura (TPM) del equipo, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="e1595-104">The **ProtectKeyWithTPM** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available.</span></span>

<span data-ttu-id="e1595-105">Se crea un protector de clave de tipo "TPM" para el volumen, si aún no existe ninguno.</span><span class="sxs-lookup"><span data-stu-id="e1595-105">A key protector of type "TPM" is created for the volume, if one does not already exist.</span></span>

<span data-ttu-id="e1595-106">Este método solo es aplicable para el volumen que contiene el sistema operativo que se está ejecutando actualmente y si aún no existe un protector de claves en el volumen.</span><span class="sxs-lookup"><span data-stu-id="e1595-106">This method is only applicable for the volume that contains the currently running operating system, and if a key protector does not already exist on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1595-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1595-107">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPM(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="e1595-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1595-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1595-109">*FriendlyName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e1595-109">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e1595-110">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="e1595-110">Type: **string**</span></span>

<span data-ttu-id="e1595-111">Cadena que especifica un identificador de cadena asignado por el usuario para este protector de clave.</span><span class="sxs-lookup"><span data-stu-id="e1595-111">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="e1595-112">Si no se especifica este parámetro, se utiliza un valor en blanco.</span><span class="sxs-lookup"><span data-stu-id="e1595-112">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="e1595-113">*PlatformValidationProfile* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e1595-113">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e1595-114">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="e1595-114">Type: **uint8\[\]**</span></span>

<span data-ttu-id="e1595-115">Matriz de enteros que especifica el modo en que el hardware de seguridad del Módulo de plataforma segura (TPM) del equipo protege la clave de cifrado del volumen de disco.</span><span class="sxs-lookup"><span data-stu-id="e1595-115">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the disk volume's encryption key.</span></span>

<span data-ttu-id="e1595-116">Un perfil de validación de plataforma consta de un conjunto de índices de registro de configuración de plataforma (PCR) que van de 0 a 23, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="e1595-116">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="e1595-117">Los valores de repetición del parámetro se omiten.</span><span class="sxs-lookup"><span data-stu-id="e1595-117">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="e1595-118">Cada índice de PCR está asociado a los servicios que se ejecutan cuando se inicia el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e1595-118">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="e1595-119">Cada vez que se inicia el equipo, el TPM comprobará que los servicios especificados en el perfil de validación de plataforma no han cambiado.</span><span class="sxs-lookup"><span data-stu-id="e1595-119">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="e1595-120">Si alguno de estos servicios cambia mientras la protección de Cifrado de unidad BitLocker (BDE) permanece en ON, el TPM no liberará la clave de cifrado para desbloquear el volumen del disco y el equipo entrará en modo de recuperación.</span><span class="sxs-lookup"><span data-stu-id="e1595-120">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="e1595-121">Si se especifica este parámetro mientras se ha habilitado el valor de la directiva de grupo correspondiente, debe coincidir con la configuración de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="e1595-121">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="e1595-122">Si no se especifica este parámetro, se usa el valor predeterminado de 0, 2, 4, 5, 8, 9, 10 y 11.</span><span class="sxs-lookup"><span data-stu-id="e1595-122">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="e1595-123">El perfil de validación de plataforma predeterminado protege la clave de cifrado frente a los cambios en la raíz principal de la confianza de medición (CRTM). BIOS, y extensiones de plataforma (PCR 0), código ROM de opción (PCR 2), el código de registro de arranque maestro (MBR) (PCR 4), la tabla de particiones de registro de arranque maestro (PCR 5), el sector de arranque NTFS (PCR 8), el código de arranque NTFS (PCR 9), el administrador de arranque (PCR 10) y el Access Control de Cifrado de unidad BitLocker (PCR 11).</span><span class="sxs-lookup"><span data-stu-id="e1595-123">The default platform validation profile secures the encryption key against changes to the Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions (PCR 0), Option ROM Code (PCR 2), the Master Boot Record (MBR) Code (PCR 4), the Master Boot Record (MBR) Partition Table (PCR 5), the NTFS Boot Sector (PCR 8), the NTFS Boot Code (PCR 9), the Boot Manager (PCR 10), and the BitLocker Drive Encryption Access Control (PCR 11).</span></span> <span data-ttu-id="e1595-124">Para la seguridad del equipo, se recomienda el perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e1595-124">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="e1595-125">De forma predeterminada, los equipos basados en Unified Extensible Firmware Interface (UEFI) no usan PCR 5.</span><span class="sxs-lookup"><span data-stu-id="e1595-125">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span> <span data-ttu-id="e1595-126">Para obtener protección adicional frente a los cambios de configuración de inicio temprano, use un perfil de PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="e1595-126">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="e1595-127">Cambiar desde el perfil predeterminado afecta a la seguridad y la capacidad de administración del equipo.</span><span class="sxs-lookup"><span data-stu-id="e1595-127">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="e1595-128">La confidencialidad de las modificaciones de BitLocker a plataforma (malintencionadas o autorizadas) aumenta o disminuye en función de la inclusión o exclusión, respectivamente, de las PCR.</span><span class="sxs-lookup"><span data-stu-id="e1595-128">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="e1595-129">Para habilitar la protección de BitLocker, el perfil de validación de plataforma debe incluir PCR 11.</span><span class="sxs-lookup"><span data-stu-id="e1595-129">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="e1595-130">Value</span><span class="sxs-lookup"><span data-stu-id="e1595-130">Value</span></span>                                                                         | <span data-ttu-id="e1595-131">Significado</span><span class="sxs-lookup"><span data-stu-id="e1595-131">Meaning</span></span>                                                                             |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e1595-132"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-132"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="e1595-133">Raíz principal de la confianza de medición (CRTM), BIOS y extensiones de plataforma.</span><span class="sxs-lookup"><span data-stu-id="e1595-133">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions.</span></span><br/> |
| <dl> <span data-ttu-id="e1595-134"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-134"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="e1595-135">Configuración y datos de la plataforma y la placa base</span><span class="sxs-lookup"><span data-stu-id="e1595-135">Platform and Motherboard Configuration and Data</span></span><br/>                          |
| <dl> <span data-ttu-id="e1595-136"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-136"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="e1595-137">Código ROM de opción</span><span class="sxs-lookup"><span data-stu-id="e1595-137">Option ROM Code</span></span><br/>                                                          |
| <dl> <span data-ttu-id="e1595-138"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-138"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="e1595-139">Configuración y datos de ROM de opción</span><span class="sxs-lookup"><span data-stu-id="e1595-139">Option ROM Configuration and Data</span></span><br/>                                        |
| <dl> <span data-ttu-id="e1595-140"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-140"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="e1595-141">Código de registro de arranque maestro (MBR)</span><span class="sxs-lookup"><span data-stu-id="e1595-141">Master Boot Record (MBR) Code</span></span><br/>                                            |
| <dl> <span data-ttu-id="e1595-142"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-142"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="e1595-143">Tabla de partición de registro de arranque maestro (MBR)</span><span class="sxs-lookup"><span data-stu-id="e1595-143">Master Boot Record (MBR) Partition Table</span></span><br/>                                 |
| <dl> <span data-ttu-id="e1595-144"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-144"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="e1595-145">Transición de estado y eventos de activación</span><span class="sxs-lookup"><span data-stu-id="e1595-145">State Transition and Wake Events</span></span><br/>                                         |
| <dl> <span data-ttu-id="e1595-146"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-146"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="e1595-147">Manufacturer-Specific de equipo</span><span class="sxs-lookup"><span data-stu-id="e1595-147">Computer Manufacturer-Specific</span></span><br/>                                           |
| <dl> <span data-ttu-id="e1595-148"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-148"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="e1595-149">Sector de arranque de NTFS</span><span class="sxs-lookup"><span data-stu-id="e1595-149">NTFS Boot Sector</span></span><br/>                                                         |
| <dl> <span data-ttu-id="e1595-150"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-150"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="e1595-151">Código de arranque NTFS</span><span class="sxs-lookup"><span data-stu-id="e1595-151">NTFS Boot Code</span></span><br/>                                                           |
| <dl> <span data-ttu-id="e1595-152"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-152"><dt>10</dt></span></span> </dl> | <span data-ttu-id="e1595-153">Administrador de arranque</span><span class="sxs-lookup"><span data-stu-id="e1595-153">Boot Manager</span></span><br/>                                                             |
| <dl> <span data-ttu-id="e1595-154"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-154"><dt>11</dt></span></span> </dl> | <span data-ttu-id="e1595-155">Cifrado de unidad BitLocker Access Control</span><span class="sxs-lookup"><span data-stu-id="e1595-155">BitLocker Drive Encryption Access Control</span></span><br/>                                |
| <dl> <span data-ttu-id="e1595-156"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-156"><dt>12</dt></span></span> </dl> | <span data-ttu-id="e1595-157">Definido para que lo use el sistema operativo estático</span><span class="sxs-lookup"><span data-stu-id="e1595-157">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="e1595-158"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-158"><dt>13</dt></span></span> </dl> | <span data-ttu-id="e1595-159">Definido para que lo use el sistema operativo estático</span><span class="sxs-lookup"><span data-stu-id="e1595-159">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="e1595-160"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-160"><dt>14</dt></span></span> </dl> | <span data-ttu-id="e1595-161">Definido para que lo use el sistema operativo estático</span><span class="sxs-lookup"><span data-stu-id="e1595-161">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="e1595-162"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-162"><dt>15</dt></span></span> </dl> | <span data-ttu-id="e1595-163">Definido para que lo use el sistema operativo estático</span><span class="sxs-lookup"><span data-stu-id="e1595-163">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="e1595-164"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-164"><dt>16</dt></span></span> </dl> | <span data-ttu-id="e1595-165">Se usa para la depuración</span><span class="sxs-lookup"><span data-stu-id="e1595-165">Used for debugging</span></span><br/>                                                       |
| <dl> <span data-ttu-id="e1595-166"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-166"><dt>17</dt></span></span> </dl> | <span data-ttu-id="e1595-167">CRTM dinámico</span><span class="sxs-lookup"><span data-stu-id="e1595-167">Dynamic CRTM</span></span><br/>                                                             |
| <dl> <span data-ttu-id="e1595-168"><dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-168"><dt>18</dt></span></span> </dl> | <span data-ttu-id="e1595-169">Plataforma definida</span><span class="sxs-lookup"><span data-stu-id="e1595-169">Platform defined</span></span><br/>                                                         |
| <dl> <span data-ttu-id="e1595-170"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-170"><dt>19</dt></span></span> </dl> | <span data-ttu-id="e1595-171">Usado por el sistema operativo de confianza</span><span class="sxs-lookup"><span data-stu-id="e1595-171">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="e1595-172"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-172"><dt>20</dt></span></span> </dl> | <span data-ttu-id="e1595-173">Usado por el sistema operativo de confianza</span><span class="sxs-lookup"><span data-stu-id="e1595-173">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="e1595-174"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-174"><dt>21</dt></span></span> </dl> | <span data-ttu-id="e1595-175">Usado por el sistema operativo de confianza</span><span class="sxs-lookup"><span data-stu-id="e1595-175">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="e1595-176"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-176"><dt>22</dt></span></span> </dl> | <span data-ttu-id="e1595-177">Usado por el sistema operativo de confianza</span><span class="sxs-lookup"><span data-stu-id="e1595-177">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="e1595-178"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-178"><dt>23</dt></span></span> </dl> | <span data-ttu-id="e1595-179">Compatibilidad con aplicaciones</span><span class="sxs-lookup"><span data-stu-id="e1595-179">Application support</span></span><br/>                                                      |



 

</dd> <dt>

<span data-ttu-id="e1595-180">*VolumeKeyProtectorID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e1595-180">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1595-181">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="e1595-181">Type: **string**</span></span>

<span data-ttu-id="e1595-182">Una cadena que identifica de forma única el protector creado y que se puede usar para administrar el protector de clave.</span><span class="sxs-lookup"><span data-stu-id="e1595-182">A string that uniquely identifies the created protector and which can be used to manage the key protector.</span></span>

<span data-ttu-id="e1595-183">Si la unidad admite el cifrado de hardware y BitLocker no ha tomado propiedad de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos de cada banda.</span><span class="sxs-lookup"><span data-stu-id="e1595-183">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1595-184">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1595-184">Return value</span></span>

<span data-ttu-id="e1595-185">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e1595-185">Type: **uint32**</span></span>

<span data-ttu-id="e1595-186">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="e1595-186">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="e1595-187">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1595-187">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="e1595-188">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1595-188">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e1595-189"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-189"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="e1595-190">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e1595-190">The method was successful.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="e1595-191"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-191"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>        | <span data-ttu-id="e1595-192">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="e1595-192">The volume is locked.</span></span><br/>                                                                                                                                                   |
| <dl> <span data-ttu-id="e1595-193"><dt>**TBS \_ El \_ servicio E \_ no se \_ está ejecutando**</dt> <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-193"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl> | <span data-ttu-id="e1595-194">No se encuentra ningún TPM compatible en este equipo.</span><span class="sxs-lookup"><span data-stu-id="e1595-194">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="e1595-195"><dt>**FVE \_ \_ \_ Volumen externo E**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-195"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>       | <span data-ttu-id="e1595-196">El TPM no puede proteger la clave de cifrado del volumen porque el volumen no contiene el sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="e1595-196">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                           |
| <dl> <span data-ttu-id="e1595-197"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-197"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="e1595-198">Se proporciona el parámetro *PlatformValidationProfile* , pero sus valores no están dentro del intervalo conocido o no coinciden con la configuración de directiva de grupo actualmente en vigor.</span><span class="sxs-lookup"><span data-stu-id="e1595-198">The *PlatformValidationProfile* parameter is provided but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> |
| <dl> <span data-ttu-id="e1595-199"><dt>**FVE \_ El \_ protector E \_ existe**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-199"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>            | <span data-ttu-id="e1595-200">Ya existe un protector de clave de este tipo.</span><span class="sxs-lookup"><span data-stu-id="e1595-200">A key protector of this type already exists.</span></span><br/>                                                                                                                             |



 

## <a name="security-considerations"></a><span data-ttu-id="e1595-201">Consideraciones sobre la seguridad</span><span class="sxs-lookup"><span data-stu-id="e1595-201">Security Considerations</span></span>

<span data-ttu-id="e1595-202">Para la seguridad del equipo, se recomienda el perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e1595-202">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="e1595-203">Para obtener protección adicional frente a los cambios de configuración de inicio temprano, use un perfil de PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="e1595-203">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="e1595-204">Cambiar desde el perfil predeterminado afecta a la seguridad o la facilidad de uso del equipo.</span><span class="sxs-lookup"><span data-stu-id="e1595-204">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1595-205">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1595-205">Remarks</span></span>

<span data-ttu-id="e1595-206">Como máximo, puede existir un protector de clave de tipo "TPM" para un volumen en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="e1595-206">At most one key protector of type "TPM" can exist for a volume at any time.</span></span> <span data-ttu-id="e1595-207">Si desea cambiar el nombre para mostrar o el perfil de validación de plataforma usado por un protector de clave "TPM" existente, primero debe quitar el protector de clave existente y, a continuación, llamar a **ProtectKeyWithTPM** para crear uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="e1595-207">If you want to change the display name or the platform validation profile used by an existing "TPM" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPM** to create a new one.</span></span>

<span data-ttu-id="e1595-208">En el caso de los índices de PCR de 0 a 5, las medidas actuales de los registros se utilizan para proteger la clave de cifrado.</span><span class="sxs-lookup"><span data-stu-id="e1595-208">For PCR indices 0 through 5, the current measurements in the registers are used to protect the encryption key.</span></span> <span data-ttu-id="e1595-209">En el caso de los valores de PCR del 8 al 11, las medidas usadas son las que se espera que existan en el siguiente ciclo de inicio.</span><span class="sxs-lookup"><span data-stu-id="e1595-209">For PCR values 8 through 11, the measurements used are the ones expected to exist on the next start cycle.</span></span>

<span data-ttu-id="e1595-210">Se deben especificar protectores de clave adicionales para desbloquear el volumen en escenarios de recuperación en los que no se puede obtener acceso a la clave de cifrado del volumen. por ejemplo, cuando el TPM no puede validar correctamente el perfil de validación de plataforma.</span><span class="sxs-lookup"><span data-stu-id="e1595-210">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile.</span></span> <span data-ttu-id="e1595-211">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) o [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) para crear uno o varios protectores de clave para recuperar un volumen bloqueado de otro modo.</span><span class="sxs-lookup"><span data-stu-id="e1595-211">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="e1595-212">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e1595-212">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e1595-213">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e1595-213">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="e1595-214">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="e1595-214">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e1595-215">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="e1595-215">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1595-216">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1595-216">Requirements</span></span>



| <span data-ttu-id="e1595-217">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1595-217">Requirement</span></span> | <span data-ttu-id="e1595-218">Value</span><span class="sxs-lookup"><span data-stu-id="e1595-218">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1595-219">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1595-219">Minimum supported client</span></span><br/> | <span data-ttu-id="e1595-220">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="e1595-220">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e1595-221">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1595-221">Minimum supported server</span></span><br/> | <span data-ttu-id="e1595-222">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e1595-222">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e1595-223">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e1595-223">Namespace</span></span><br/>                | <span data-ttu-id="e1595-224">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="e1595-224">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="e1595-225">MOF</span><span class="sxs-lookup"><span data-stu-id="e1595-225">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1595-226"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1595-226"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1595-227">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1595-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1595-228">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="e1595-228">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="e1595-229">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="e1595-229">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
