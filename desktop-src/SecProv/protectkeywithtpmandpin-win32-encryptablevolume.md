---
description: Si el Módulo de plataforma segura (TPM) está disponible, este método protege la clave de cifrado del volumen mejorada por un número de identificación personal especificado por el usuario.
ms.assetid: 8c4c434a-dd60-491a-a983-b3fa78c91c0d
title: Método ProtectKeyWithTPMAndPIN de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndPIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e5a0a7a253723bec84df7a86fa94ab182bd192dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907805"
---
# <a name="protectkeywithtpmandpin-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="a7bf9-103">Método ProtectKeyWithTPMAndPIN de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="a7bf9-103">ProtectKeyWithTPMAndPIN method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="a7bf9-104">El método **ProtectKeyWithTPMAndPIN** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) protege la clave de cifrado del volumen mediante el hardware de seguridad de módulo de plataforma segura (TPM) del equipo, si está disponible, mejorado por un número de identificación personal (PIN) especificado por el usuario que se debe proporcionar al equipo en el inicio.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-104">The **ProtectKeyWithTPMAndPIN** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available, enhanced by a user-specified personal identification number (PIN) that must be provided to the computer at startup.</span></span>

<span data-ttu-id="a7bf9-105">Tanto la validación por TPM como la entrada de la cadena de identificación personal son necesarias para tener acceso a la clave de cifrado del volumen y desbloquear el contenido del volumen.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-105">Both validation by the TPM and input of the personal identification string are necessary to access the volume's encryption key and unlock volume contents.</span></span>

<span data-ttu-id="a7bf9-106">Este método solo es aplicable para el volumen que contiene el sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-106">This method is only applicable for the volume that contains the currently running operating system.</span></span>

<span data-ttu-id="a7bf9-107">Se crea un protector de clave de tipo "TPM y PIN" para el volumen, si aún no existe ninguno.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-107">A key protector of type "TPM And PIN" is created for the volume, if one does not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7bf9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7bf9-108">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPMAndPIN(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [in]           string PIN,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="a7bf9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7bf9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7bf9-110">*FriendlyName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a7bf9-110">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a7bf9-111">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="a7bf9-111">Type: **string**</span></span>

<span data-ttu-id="a7bf9-112">Identificador de cadena asignado por el usuario para este protector de clave.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-112">A user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="a7bf9-113">Si no se especifica este parámetro, se utiliza un valor en blanco.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-113">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="a7bf9-114">*PlatformValidationProfile* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a7bf9-114">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a7bf9-115">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="a7bf9-115">Type: **uint8\[\]**</span></span>

<span data-ttu-id="a7bf9-116">Matriz de enteros que especifica el modo en que el hardware de seguridad del Módulo de plataforma segura (TPM) del equipo protege la clave de cifrado del volumen de disco.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-116">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the disk volume's encryption key.</span></span>

<span data-ttu-id="a7bf9-117">Un perfil de validación de plataforma consta de un conjunto de índices de registro de configuración de plataforma (PCR) que van de 0 a 23, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-117">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="a7bf9-118">Los valores de repetición del parámetro se omiten.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-118">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="a7bf9-119">Cada índice de PCR está asociado a los servicios que se ejecutan cuando se inicia el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-119">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="a7bf9-120">Cada vez que se inicia el equipo, el TPM comprobará que los servicios especificados en el perfil de validación de plataforma no han cambiado.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-120">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="a7bf9-121">Si alguno de estos servicios cambia mientras la protección de Cifrado de unidad BitLocker (BDE) permanece en ON, el TPM no liberará la clave de cifrado para desbloquear el volumen del disco y el equipo entrará en modo de recuperación.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-121">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume, and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="a7bf9-122">Si se especifica este parámetro mientras se ha habilitado el valor de la directiva de grupo correspondiente, debe coincidir con la configuración de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-122">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="a7bf9-123">Si no se especifica este parámetro, se usa el valor predeterminado de 0, 2, 4, 5, 8, 9, 10 y 11.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-123">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="a7bf9-124">El perfil de validación de plataforma predeterminado protege la clave de cifrado frente a los cambios en los elementos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a7bf9-124">The default platform validation profile secures the encryption key against changes to the following elements:</span></span>

-   <span data-ttu-id="a7bf9-125">Raíz principal de la confianza de la medida (CRTM)</span><span class="sxs-lookup"><span data-stu-id="a7bf9-125">Core Root of Trust of Measurement (CRTM)</span></span>
-   <span data-ttu-id="a7bf9-126">BIOS</span><span class="sxs-lookup"><span data-stu-id="a7bf9-126">BIOS</span></span>
-   <span data-ttu-id="a7bf9-127">Extensiones de la plataforma (PCR 0)</span><span class="sxs-lookup"><span data-stu-id="a7bf9-127">Platform Extensions (PCR 0)</span></span>
-   <span data-ttu-id="a7bf9-128">Código ROM de opción (PCR 2)</span><span class="sxs-lookup"><span data-stu-id="a7bf9-128">Option ROM Code (PCR 2)</span></span>
-   <span data-ttu-id="a7bf9-129">Código de registro de arranque maestro (MBR) (PCR 4)</span><span class="sxs-lookup"><span data-stu-id="a7bf9-129">Master Boot Record (MBR) Code (PCR 4)</span></span>
-   <span data-ttu-id="a7bf9-130">Tabla de partición de registro de arranque maestro (MBR) (PCR 5)</span><span class="sxs-lookup"><span data-stu-id="a7bf9-130">Master Boot Record (MBR) Partition Table (PCR 5)</span></span>
-   <span data-ttu-id="a7bf9-131">Sector de arranque de NTFS (PCR 8)</span><span class="sxs-lookup"><span data-stu-id="a7bf9-131">NTFS Boot Sector (PCR 8)</span></span>
-   <span data-ttu-id="a7bf9-132">Bloque de arranque de NTFS (PCR 9)</span><span class="sxs-lookup"><span data-stu-id="a7bf9-132">NTFS Boot Block (PCR 9)</span></span>
-   <span data-ttu-id="a7bf9-133">Administración de arranque (PCR 10)</span><span class="sxs-lookup"><span data-stu-id="a7bf9-133">Boot Manager (PCR 10)</span></span>
-   <span data-ttu-id="a7bf9-134">Control de acceso de BitLocker (PCR 11)</span><span class="sxs-lookup"><span data-stu-id="a7bf9-134">BitLocker Access Control (PCR 11)</span></span>

<span data-ttu-id="a7bf9-135">Para la seguridad del equipo, se recomienda el perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-135">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="a7bf9-136">Para obtener protección adicional frente a los cambios de configuración de inicio temprano, use un perfil de PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-136">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span> <span data-ttu-id="a7bf9-137">De forma predeterminada, los equipos basados en Unified Extensible Firmware Interface (UEFI) no usan PCR 5.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-137">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span>

<span data-ttu-id="a7bf9-138">Cambiar desde el perfil predeterminado afecta a la seguridad y la capacidad de administración del equipo.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-138">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="a7bf9-139">La confidencialidad de las modificaciones de BitLocker a plataforma (malintencionadas o autorizadas) aumenta o disminuye en función de la inclusión o exclusión, respectivamente, de las PCR.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-139">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="a7bf9-140">Para habilitar la protección de BitLocker, el perfil de validación de plataforma debe incluir PCR 11.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-140">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="a7bf9-141">Value</span><span class="sxs-lookup"><span data-stu-id="a7bf9-141">Value</span></span>                                                                         | <span data-ttu-id="a7bf9-142">Significado</span><span class="sxs-lookup"><span data-stu-id="a7bf9-142">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a7bf9-143"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-143"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="a7bf9-144">Raíz principal de la confianza de medición (CRTM), BIOS y extensiones de plataforma</span><span class="sxs-lookup"><span data-stu-id="a7bf9-144">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="a7bf9-145"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-145"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="a7bf9-146">Configuración y datos de la plataforma y la placa base</span><span class="sxs-lookup"><span data-stu-id="a7bf9-146">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="a7bf9-147"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-147"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="a7bf9-148">Código ROM de opción</span><span class="sxs-lookup"><span data-stu-id="a7bf9-148">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="a7bf9-149"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-149"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="a7bf9-150">Configuración y datos de ROM de opción</span><span class="sxs-lookup"><span data-stu-id="a7bf9-150">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="a7bf9-151"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-151"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="a7bf9-152">Código de registro de arranque maestro (MBR)</span><span class="sxs-lookup"><span data-stu-id="a7bf9-152">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="a7bf9-153"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-153"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="a7bf9-154">Tabla de partición de registro de arranque maestro (MBR)</span><span class="sxs-lookup"><span data-stu-id="a7bf9-154">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="a7bf9-155"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-155"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="a7bf9-156">Transición de estado y eventos de activación</span><span class="sxs-lookup"><span data-stu-id="a7bf9-156">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="a7bf9-157"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-157"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="a7bf9-158">Manufacturer-Specific de equipo</span><span class="sxs-lookup"><span data-stu-id="a7bf9-158">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="a7bf9-159"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-159"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="a7bf9-160">Sector de arranque de NTFS</span><span class="sxs-lookup"><span data-stu-id="a7bf9-160">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="a7bf9-161"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-161"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="a7bf9-162">Bloque de arranque de NTFS</span><span class="sxs-lookup"><span data-stu-id="a7bf9-162">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="a7bf9-163"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-163"><dt>10</dt></span></span> </dl> | <span data-ttu-id="a7bf9-164">Administrador de arranque</span><span class="sxs-lookup"><span data-stu-id="a7bf9-164">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="a7bf9-165"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-165"><dt>11</dt></span></span> </dl> | <span data-ttu-id="a7bf9-166">Access Control de BitLocker</span><span class="sxs-lookup"><span data-stu-id="a7bf9-166">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="a7bf9-167"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-167"><dt>12</dt></span></span> </dl> | <span data-ttu-id="a7bf9-168">Definido para que lo use el sistema operativo estático</span><span class="sxs-lookup"><span data-stu-id="a7bf9-168">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="a7bf9-169"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-169"><dt>13</dt></span></span> </dl> | <span data-ttu-id="a7bf9-170">Definido para que lo use el sistema operativo estático</span><span class="sxs-lookup"><span data-stu-id="a7bf9-170">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="a7bf9-171"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-171"><dt>14</dt></span></span> </dl> | <span data-ttu-id="a7bf9-172">Definido para que lo use el sistema operativo estático</span><span class="sxs-lookup"><span data-stu-id="a7bf9-172">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="a7bf9-173"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-173"><dt>15</dt></span></span> </dl> | <span data-ttu-id="a7bf9-174">Definido para que lo use el sistema operativo estático</span><span class="sxs-lookup"><span data-stu-id="a7bf9-174">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="a7bf9-175"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-175"><dt>16</dt></span></span> </dl> | <span data-ttu-id="a7bf9-176">Se usa para la depuración</span><span class="sxs-lookup"><span data-stu-id="a7bf9-176">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="a7bf9-177"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-177"><dt>17</dt></span></span> </dl> | <span data-ttu-id="a7bf9-178">CRTM dinámico</span><span class="sxs-lookup"><span data-stu-id="a7bf9-178">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="a7bf9-179"><dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-179"><dt>18</dt></span></span> </dl> | <span data-ttu-id="a7bf9-180">Plataforma definida</span><span class="sxs-lookup"><span data-stu-id="a7bf9-180">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="a7bf9-181"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-181"><dt>19</dt></span></span> </dl> | <span data-ttu-id="a7bf9-182">Usado por un sistema operativo de confianza</span><span class="sxs-lookup"><span data-stu-id="a7bf9-182">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="a7bf9-183"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-183"><dt>20</dt></span></span> </dl> | <span data-ttu-id="a7bf9-184">Usado por un sistema operativo de confianza</span><span class="sxs-lookup"><span data-stu-id="a7bf9-184">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="a7bf9-185"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-185"><dt>21</dt></span></span> </dl> | <span data-ttu-id="a7bf9-186">Usado por un sistema operativo de confianza</span><span class="sxs-lookup"><span data-stu-id="a7bf9-186">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="a7bf9-187"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-187"><dt>22</dt></span></span> </dl> | <span data-ttu-id="a7bf9-188">Usado por un sistema operativo de confianza</span><span class="sxs-lookup"><span data-stu-id="a7bf9-188">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="a7bf9-189"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-189"><dt>23</dt></span></span> </dl> | <span data-ttu-id="a7bf9-190">Compatibilidad con aplicaciones</span><span class="sxs-lookup"><span data-stu-id="a7bf9-190">Application support</span></span><br/>                                                     |



 

</dd> <dt>

<span data-ttu-id="a7bf9-191">*Código PIN* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a7bf9-191">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7bf9-192">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="a7bf9-192">Type: **string**</span></span>

<span data-ttu-id="a7bf9-193">Cadena de identificación personal especificada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-193">A user-specified personal identification string.</span></span> <span data-ttu-id="a7bf9-194">Esta cadena debe estar formada por una secuencia de 6 a 20 dígitos o, si la Directiva de grupo "permitir PIN mejorados para el inicio" está habilitada, de 6 a 20 letras, símbolos, espacios o números.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-194">This string must consist of a sequence of 6 to 20 digits or, if the "Allow enhanced PINs for startup" group policy is enabled, 6 to 20 letters, symbols, spaces, or numbers.</span></span>

</dd> <dt>

<span data-ttu-id="a7bf9-195">*VolumeKeyProtectorID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a7bf9-195">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7bf9-196">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="a7bf9-196">Type: **string**</span></span>

<span data-ttu-id="a7bf9-197">Identificador de cadena único actualizado que se usa para administrar un protector de clave de volumen cifrado.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-197">The updated unique string identifier used to manage an encrypted volume key protector.</span></span>

<span data-ttu-id="a7bf9-198">Si la unidad admite el cifrado de hardware y BitLocker no ha tomado propiedad de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos de cada banda.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-198">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7bf9-199">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7bf9-199">Return value</span></span>

<span data-ttu-id="a7bf9-200">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7bf9-200">Type: **uint32**</span></span>

<span data-ttu-id="a7bf9-201">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-201">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="a7bf9-202">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7bf9-202">Return code/value</span></span>                                                                                                                                                                                | <span data-ttu-id="a7bf9-203">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7bf9-203">Description</span></span>                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a7bf9-204"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-204"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                | <span data-ttu-id="a7bf9-205">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-205">The method was successful.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="a7bf9-206"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-206"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                        | <span data-ttu-id="a7bf9-207">Se proporciona el parámetro *PlatformValidationProfile* , pero sus valores no están dentro del intervalo conocido o no coinciden con la configuración de directiva de grupo actualmente en vigor.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-207">The *PlatformValidationProfile* parameter is provided, but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> |
| <dl> <span data-ttu-id="a7bf9-208"><dt>**FVE \_ E \_ \_ CDDVD de arranque**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-208"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>              | <span data-ttu-id="a7bf9-209">En este equipo se encuentra un CD/DVD de arranque.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-209">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="a7bf9-210">Quite el CD o el DVD y reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-210">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="a7bf9-211"><dt>**FVE \_ \_ \_ Volumen externo E**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-211"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>              | <span data-ttu-id="a7bf9-212">El TPM no puede proteger la clave de cifrado del volumen porque el volumen no contiene el sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-212">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                            |
| <dl> <span data-ttu-id="a7bf9-213"><dt>**FVE \_ E \_ \_ \_ caracteres de PIN no válidos**</dt> <dt>2150695066 (0x8031009A)</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-213"><dt>**FVE\_E\_INVALID\_PIN\_CHARS**</dt> <dt>2150695066 (0x8031009A)</dt></span></span> </dl>          | <span data-ttu-id="a7bf9-214">El parámetro *NewPIN* contiene caracteres que no son válidos.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-214">The *NewPIN* parameter contains characters that are not valid.</span></span> <span data-ttu-id="a7bf9-215">Cuando el directiva de grupo "permitir PIN mejorados para el inicio" está deshabilitado, solo se admiten los números.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-215">When the "Allow enhanced PINs for startup" Group Policy is disabled, only numbers are supported.</span></span><br/>          |
| <dl> <span data-ttu-id="a7bf9-216"><dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-216"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>               | <span data-ttu-id="a7bf9-217">El volumen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-217">The volume is locked.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="a7bf9-218"><dt>**FVE \_ \_Longitud de \_ \_ PIN no \_ válida de la Directiva E**</dt> <dt>2150695016 (0x80310068)</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-218"><dt>**FVE\_E\_POLICY\_INVALID\_PIN\_LENGTH**</dt> <dt>2150695016 (0x80310068)</dt></span></span> </dl> | <span data-ttu-id="a7bf9-219">El parámetro *NewPIN* proporcionado tiene más de 20 caracteres, menos de 6 caracteres, o menor que la longitud mínima especificada por directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-219">The *NewPIN* parameter supplied is either longer than 20 characters, shorter than 6 characters, or shorter than the minimum length specified by Group Policy.</span></span><br/>            |
| <dl> <span data-ttu-id="a7bf9-220"><dt>**FVE \_ El \_ protector E \_ existe**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-220"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>            | <span data-ttu-id="a7bf9-221">Ya existe un protector de clave de este tipo.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-221">A key protector of this type already exists.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="a7bf9-222"><dt>**TBS \_ El \_ servicio E \_ no se \_ está ejecutando**</dt> <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-222"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl>        | <span data-ttu-id="a7bf9-223">No se encuentra ningún TPM compatible en este equipo.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-223">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                             |



 

## <a name="security-considerations"></a><span data-ttu-id="a7bf9-224">Consideraciones sobre la seguridad</span><span class="sxs-lookup"><span data-stu-id="a7bf9-224">Security Considerations</span></span>

<span data-ttu-id="a7bf9-225">Para la seguridad del equipo, se recomienda el perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-225">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="a7bf9-226">Para obtener una protección adicional frente a los cambios en el código de inicio temprano, use un perfil de PCRs 0, 2, 4, 5, 8, 9, 10 y 11.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-226">For additional protection against early startup code changes, use a profile of PCRs 0, 2, 4, 5, 8, 9, 10, and 11.</span></span> <span data-ttu-id="a7bf9-227">Para obtener protección adicional frente a los cambios de configuración de inicio temprano, use un perfil de PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-227">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="a7bf9-228">Cambiar desde el perfil predeterminado afecta a la seguridad o la facilidad de uso del equipo.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-228">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7bf9-229">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7bf9-229">Remarks</span></span>

<span data-ttu-id="a7bf9-230">Como máximo, puede existir un protector de clave de tipo "TPM y PIN" para un volumen en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-230">At most one key protector of type "TPM And PIN" can exist for a volume at any time.</span></span> <span data-ttu-id="a7bf9-231">Si desea cambiar el nombre para mostrar o el perfil de validación de plataforma usado por un protector de clave "TPM y PIN" existente, primero debe quitar el protector de clave existente y, a continuación, llamar a **ProtectKeyWithTPMAndPIN** para crear uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-231">If you want to change the display name or the platform validation profile used by an existing "TPM And PIN" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPMAndPIN** to create a new one.</span></span>

<span data-ttu-id="a7bf9-232">Se deben especificar protectores de clave adicionales para desbloquear el volumen en escenarios de recuperación en los que no se puede obtener acceso a la clave de cifrado del volumen. por ejemplo, cuando el TPM no se puede validar correctamente con el perfil de validación de plataforma o cuando se pierde el PIN.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-232">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile or when the PIN is lost.</span></span>

<span data-ttu-id="a7bf9-233">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) o [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) para crear uno o varios protectores de clave para recuperar un volumen bloqueado de otro modo.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-233">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="a7bf9-234">Aunque es posible tener tanto un protector de clave del tipo "TPM" como otro del tipo "TPM y el PIN", la presencia del tipo de protector de clave "TPM" niega los efectos de otros protectores de clave basados en TPM.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-234">While it is possible to have both a key protector of the type "TPM" and another of the type "TPM And PIN", the presence of the "TPM" key protector type negates the effects of other TPM-based key protectors.</span></span>

<span data-ttu-id="a7bf9-235">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a7bf9-235">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a7bf9-236">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-236">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="a7bf9-237">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="a7bf9-237">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a7bf9-238">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="a7bf9-238">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7bf9-239">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7bf9-239">Requirements</span></span>



| <span data-ttu-id="a7bf9-240">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7bf9-240">Requirement</span></span> | <span data-ttu-id="a7bf9-241">Value</span><span class="sxs-lookup"><span data-stu-id="a7bf9-241">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7bf9-242">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7bf9-242">Minimum supported client</span></span><br/> | <span data-ttu-id="a7bf9-243">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="a7bf9-243">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a7bf9-244">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7bf9-244">Minimum supported server</span></span><br/> | <span data-ttu-id="a7bf9-245">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a7bf9-245">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a7bf9-246">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a7bf9-246">Namespace</span></span><br/>                | <span data-ttu-id="a7bf9-247">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="a7bf9-247">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="a7bf9-248">MOF</span><span class="sxs-lookup"><span data-stu-id="a7bf9-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7bf9-249"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7bf9-249"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7bf9-250">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7bf9-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7bf9-251">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="a7bf9-251">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="a7bf9-252">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="a7bf9-252">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
