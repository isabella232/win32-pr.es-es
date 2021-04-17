---
description: Representa el Módulo de plataforma segura (TPM), un chip de seguridad de hardware que proporciona una raíz de confianza para un sistema informático.
ms.assetid: da4ba366-49af-420e-a2ad-80bba34b3b00
title: Win32_Tpm (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm
- Win32_Tpm.IsActivated_InitialValue
- Win32_Tpm.IsEnabled_InitialValue
- Win32_Tpm.IsOwned_InitialValue
- Win32_Tpm.SpecVersion
- Win32_Tpm.ManufacturerVersion
- Win32_Tpm.ManufacturerVersionInfo
- Win32_Tpm.ManufacturerId
- Win32_Tpm.PhysicalPresenceVersionInfo
api_type:
- DllExport
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d8d6eac9fba875484ba2f08e149608c9994a1087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668309"
---
# <a name="win32_tpm-class"></a><span data-ttu-id="dfe56-103">\_Clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="dfe56-103">Win32\_Tpm class</span></span>

<span data-ttu-id="dfe56-104">La **clase \_ TPM de Win32** representa el módulo de plataforma segura (TPM), un chip de seguridad de hardware que proporciona una raíz de confianza para un sistema informático.</span><span class="sxs-lookup"><span data-stu-id="dfe56-104">The **Win32\_Tpm** class represents the Trusted Platform Module (TPM), a hardware security chip that provides a root of trust for a computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfe56-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dfe56-105">Syntax</span></span>

``` syntax
class Win32_Tpm
{
  boolean IsActivated_InitialValue;
  boolean IsEnabled_InitialValue;
  boolean IsOwned_InitialValue;
  string  SpecVersion;
  string  ManufacturerVersion;
  string  ManufacturerVersionInfo;
  uint32  ManufacturerId;
  string  PhysicalPresenceVersionInfo;
};
```

## <a name="members"></a><span data-ttu-id="dfe56-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="dfe56-106">Members</span></span>

<span data-ttu-id="dfe56-107">La clase **Win32 \_ TPM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dfe56-107">The **Win32\_Tpm** class has these types of members:</span></span>

-   [<span data-ttu-id="dfe56-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="dfe56-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="dfe56-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dfe56-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dfe56-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="dfe56-110">Methods</span></span>

<span data-ttu-id="dfe56-111">La clase **Win32 \_ TPM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="dfe56-111">The **Win32\_Tpm** class has these methods.</span></span>



| <span data-ttu-id="dfe56-112">Método</span><span class="sxs-lookup"><span data-stu-id="dfe56-112">Method</span></span>                                                                                   | <span data-ttu-id="dfe56-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfe56-113">Description</span></span>                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dfe56-114">**AddBlockedCommand**</span><span class="sxs-lookup"><span data-stu-id="dfe56-114">**AddBlockedCommand**</span></span>](addblockedcommand-win32-tpm.md)                                 | <span data-ttu-id="dfe56-115">Agrega un comando de TPM a la lista local de comandos bloqueados en Windows.</span><span class="sxs-lookup"><span data-stu-id="dfe56-115">Adds a TPM command to the local list of commands blocked on Windows.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="dfe56-116">**ChangeOwnerAuth**</span><span class="sxs-lookup"><span data-stu-id="dfe56-116">**ChangeOwnerAuth**</span></span>](changeownerauth-win32-tpm.md)                                     | <span data-ttu-id="dfe56-117">Cambia el valor de autorización de propietario de TPM.</span><span class="sxs-lookup"><span data-stu-id="dfe56-117">Changes the TPM owner authorization value.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="dfe56-118">**Claridad**</span><span class="sxs-lookup"><span data-stu-id="dfe56-118">**Clear**</span></span>](clear-win32-tpm.md)                                                         | <span data-ttu-id="dfe56-119">Restablece el TPM a su estado predeterminado de fábrica.</span><span class="sxs-lookup"><span data-stu-id="dfe56-119">Resets the TPM to its factory-default state.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="dfe56-120">**ConvertToOwnerAuth**</span><span class="sxs-lookup"><span data-stu-id="dfe56-120">**ConvertToOwnerAuth**</span></span>](converttoownerauth-win32-tpm.md)                               | <span data-ttu-id="dfe56-121">Convierte una frase de contraseña proporcionada por el usuario en un valor de autorización de propietario de 20 bytes que se puede usar para interactuar con el TPM.</span><span class="sxs-lookup"><span data-stu-id="dfe56-121">Converts a user-provided passphrase to a 20-byte owner authorization value that can be used to interact with the TPM.</span></span><br/>                                                            |
| [<span data-ttu-id="dfe56-122">**CreateEndorsementKeyPair**</span><span class="sxs-lookup"><span data-stu-id="dfe56-122">**CreateEndorsementKeyPair**</span></span>](createendorsementkeypair-win32-tpm.md)                   | <span data-ttu-id="dfe56-123">Crea un par de claves de aprobación de 2048 bits en el TPM.</span><span class="sxs-lookup"><span data-stu-id="dfe56-123">Creates a 2048-bit endorsement key pair on the TPM.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="dfe56-124">**Disable**</span><span class="sxs-lookup"><span data-stu-id="dfe56-124">**Disable**</span></span>](disable-win32-tpm.md)                                                     | <span data-ttu-id="dfe56-125">Permite al propietario del TPM deshabilitar TPM.</span><span class="sxs-lookup"><span data-stu-id="dfe56-125">Allows the TPM owner to disable the TPM.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="dfe56-126">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="dfe56-126">**Enable**</span></span>](enable-win32-tpm.md)                                                       | <span data-ttu-id="dfe56-127">Permite al propietario del TPM habilitar TPM.</span><span class="sxs-lookup"><span data-stu-id="dfe56-127">Allows the TPM owner to enable the TPM.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="dfe56-128">**GetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="dfe56-128">**GetPhysicalPresenceRequest**</span></span>](getphysicalpresencerequest-win32-tpm.md)               | <span data-ttu-id="dfe56-129">Obtiene y devuelve la operación de presencia física de TPM pendiente.</span><span class="sxs-lookup"><span data-stu-id="dfe56-129">Gets and returns the pending TPM physical presence operation.</span></span> <span data-ttu-id="dfe56-130">Use el método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) para solicitar una operación.</span><span class="sxs-lookup"><span data-stu-id="dfe56-130">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span><br/> |
| [<span data-ttu-id="dfe56-131">**GetPhysicalPresenceResponse**</span><span class="sxs-lookup"><span data-stu-id="dfe56-131">**GetPhysicalPresenceResponse**</span></span>](getphysicalpresenceresponse-win32-tpm.md)             | <span data-ttu-id="dfe56-132">Obtiene y devuelve los resultados de una operación de presencia física de TPM realizada.</span><span class="sxs-lookup"><span data-stu-id="dfe56-132">Gets and returns the results from a TPM physical presence operation that was performed.</span></span><br/>                                                                                          |
| [<span data-ttu-id="dfe56-133">**GetPhysicalPresenceTransition**</span><span class="sxs-lookup"><span data-stu-id="dfe56-133">**GetPhysicalPresenceTransition**</span></span>](getphysicalpresencetransition-win32-tpm.md)         | <span data-ttu-id="dfe56-134">Indica la acción del usuario que se necesita para realizar una operación de presencia física de TPM.</span><span class="sxs-lookup"><span data-stu-id="dfe56-134">Indicates the user action that is needed to perform a TPM physical presence operation.</span></span><br/>                                                                                           |
| [<span data-ttu-id="dfe56-135">**IsActivated**</span><span class="sxs-lookup"><span data-stu-id="dfe56-135">**IsActivated**</span></span>](isactivated-win32-tpm.md)                                             | <span data-ttu-id="dfe56-136">Indica si el TPM está activado.</span><span class="sxs-lookup"><span data-stu-id="dfe56-136">Indicates whether the TPM is activated.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="dfe56-137">**IsCommandBlocked**</span><span class="sxs-lookup"><span data-stu-id="dfe56-137">**IsCommandBlocked**</span></span>](iscommandblocked-win32-tpm.md)                                   | <span data-ttu-id="dfe56-138">Indica si el comando TPM puede ejecutarse en este sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dfe56-138">Indicates whether the TPM command can run on this operating system.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="dfe56-139">**IsCommandPresent**</span><span class="sxs-lookup"><span data-stu-id="dfe56-139">**IsCommandPresent**</span></span>](iscommandpresent-win32-tpm.md)                                   | <span data-ttu-id="dfe56-140">Indica si este equipo admite un comando de TPM.</span><span class="sxs-lookup"><span data-stu-id="dfe56-140">Indicates whether a TPM command is supported by this computer.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="dfe56-141">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="dfe56-141">**IsEnabled**</span></span>](isenabled-win32-tpm.md)                                                 | <span data-ttu-id="dfe56-142">Indica si el TPM está habilitado.</span><span class="sxs-lookup"><span data-stu-id="dfe56-142">Indicates whether the TPM is enabled.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="dfe56-143">**IsEndorsementKeyPairPresent**</span><span class="sxs-lookup"><span data-stu-id="dfe56-143">**IsEndorsementKeyPairPresent**</span></span>](isendorsementkeypairpresent-win32-tpm.md)             | <span data-ttu-id="dfe56-144">Indica si el TPM tiene un par de claves de aprobación.</span><span class="sxs-lookup"><span data-stu-id="dfe56-144">Indicates whether the TPM has an endorsement key pair.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="dfe56-145">**IsOwned**</span><span class="sxs-lookup"><span data-stu-id="dfe56-145">**IsOwned**</span></span>](isowned-win32-tpm.md)                                                     | <span data-ttu-id="dfe56-146">Indica si el TPM tiene un propietario.</span><span class="sxs-lookup"><span data-stu-id="dfe56-146">Indicates whether the TPM has an owner.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="dfe56-147">**IsOwnerClearDisabled**</span><span class="sxs-lookup"><span data-stu-id="dfe56-147">**IsOwnerClearDisabled**</span></span>](isownercleardisabled-win32-tpm.md)                           | <span data-ttu-id="dfe56-148">Indica si el propietario de TPM puede borrar el TPM.</span><span class="sxs-lookup"><span data-stu-id="dfe56-148">Indicates whether the TPM owner can clear the TPM.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="dfe56-149">**IsOwnershipAllowed**</span><span class="sxs-lookup"><span data-stu-id="dfe56-149">**IsOwnershipAllowed**</span></span>](isownershipallowed-win32-tpm.md)                               | <span data-ttu-id="dfe56-150">Indica si se puede instalar un propietario de TPM.</span><span class="sxs-lookup"><span data-stu-id="dfe56-150">Indicates whether a TPM owner can be installed.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="dfe56-151">**IsPhysicalClearDisabled**</span><span class="sxs-lookup"><span data-stu-id="dfe56-151">**IsPhysicalClearDisabled**</span></span>](isphysicalcleardisabled-win32-tpm.md)                     | <span data-ttu-id="dfe56-152">Indica si una operación de presencia física de TPM puede borrar el TPM.</span><span class="sxs-lookup"><span data-stu-id="dfe56-152">Indicates whether a TPM physical presence operation can clear the TPM.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="dfe56-153">**IsPhysicalPresenceHardwareEnabled**</span><span class="sxs-lookup"><span data-stu-id="dfe56-153">**IsPhysicalPresenceHardwareEnabled**</span></span>](isphysicalpresencehardwareenabled-win32-tpm.md) | <span data-ttu-id="dfe56-154">Indica si este equipo admite una ruta de hardware dedicada para indicar la presencia física.</span><span class="sxs-lookup"><span data-stu-id="dfe56-154">Indicates whether this computer supports a dedicated hardware path to signal physical presence.</span></span><br/>                                                                                  |
| [<span data-ttu-id="dfe56-155">**IsSrkAuthCompatible**</span><span class="sxs-lookup"><span data-stu-id="dfe56-155">**IsSrkAuthCompatible**</span></span>](issrkauthcompatible-win32-tpm.md)                             | <span data-ttu-id="dfe56-156">Indica si la autorización de la clave raíz de almacenamiento (SRK) es compatible con Windows.</span><span class="sxs-lookup"><span data-stu-id="dfe56-156">Indicates whether the Storage Root Key (SRK) authorization is compatible with Windows.</span></span><br/>                                                                                           |
| [<span data-ttu-id="dfe56-157">**RemoveBlockedCommand**</span><span class="sxs-lookup"><span data-stu-id="dfe56-157">**RemoveBlockedCommand**</span></span>](removeblockedcommand-win32-tpm.md)                           | <span data-ttu-id="dfe56-158">Quita un comando de TPM de la lista local de comandos bloqueados por Windows.</span><span class="sxs-lookup"><span data-stu-id="dfe56-158">Removes a TPM command from the local list of commands blocked by Windows.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="dfe56-159">**ResetAuthLockOut**</span><span class="sxs-lookup"><span data-stu-id="dfe56-159">**ResetAuthLockOut**</span></span>](resetauthlockout-win32-tpm.md)                                   | <span data-ttu-id="dfe56-160">Restablece el período de tiempo de espera u otro mecanismo que los fabricantes de TPM implementan para protegerse de los ataques de diccionario en el TPM.</span><span class="sxs-lookup"><span data-stu-id="dfe56-160">Resets the time-out period or other mechanism that TPM manufacturers implement to protect against dictionary attacks on the TPM.</span></span><br/>                                                 |
| [<span data-ttu-id="dfe56-161">**ResetSrkAuth**</span><span class="sxs-lookup"><span data-stu-id="dfe56-161">**ResetSrkAuth**</span></span>](resetsrkauth-win32-tpm.md)                                           | <span data-ttu-id="dfe56-162">Restablece el valor de autorización de la clave raíz de almacenamiento (SRK) para que sea compatible con Windows.</span><span class="sxs-lookup"><span data-stu-id="dfe56-162">Resets the Storage Root Key (SRK) authorization value to be compatible with Windows.</span></span><br/>                                                                                             |
| [<span data-ttu-id="dfe56-163">**SelfTest**</span><span class="sxs-lookup"><span data-stu-id="dfe56-163">**SelfTest**</span></span>](selftest-win32-tpm.md)                                                   | <span data-ttu-id="dfe56-164">Realiza una prueba automática del TPM y devuelve el resultado.</span><span class="sxs-lookup"><span data-stu-id="dfe56-164">Performs a self-test of the TPM and returns the result.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="dfe56-165">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="dfe56-165">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)               | <span data-ttu-id="dfe56-166">Solicita que se ejecute una operación de presencia física de TPM.</span><span class="sxs-lookup"><span data-stu-id="dfe56-166">Requests a TPM physical presence operation to run.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="dfe56-167">**TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="dfe56-167">**TakeOwnership**</span></span>](takeownership-win32-tpm.md)                                         | <span data-ttu-id="dfe56-168">Instala un propietario para el TPM.</span><span class="sxs-lookup"><span data-stu-id="dfe56-168">Installs an owner for the TPM.</span></span><br/>                                                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="dfe56-169">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dfe56-169">Properties</span></span>

<span data-ttu-id="dfe56-170">La **clase \_ TPM de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dfe56-170">The **Win32\_Tpm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dfe56-171">**IsActivated \_ InitialValue**</span><span class="sxs-lookup"><span data-stu-id="dfe56-171">**IsActivated\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfe56-172">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dfe56-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dfe56-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dfe56-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfe56-174">Indica si el TPM está activado.</span><span class="sxs-lookup"><span data-stu-id="dfe56-174">Indicates whether the TPM is activated.</span></span>

<span data-ttu-id="dfe56-175">**true** si el dispositivo está activado (es decir, si **IsActivated \_ InitialValue** es true); en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="dfe56-175">**true** if the device is activated (that is, if **IsActivated\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="dfe56-176">Este valor se almacena cuando se crea una instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="dfe56-176">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="dfe56-177">Es posible que el TPM cambie el estado entre la creación de instancias y al comprobar este valor.</span><span class="sxs-lookup"><span data-stu-id="dfe56-177">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="dfe56-178">Para comprobar si el TPM está activado en tiempo real, use el método [**IsActivated**](isactivated-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="dfe56-178">To check whether the TPM is activated in real time, use the [**IsActivated**](isactivated-win32-tpm.md) method.</span></span>

<span data-ttu-id="dfe56-179">**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="dfe56-179">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="dfe56-180">**IsEnabled \_ InitialValue**</span><span class="sxs-lookup"><span data-stu-id="dfe56-180">**IsEnabled\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfe56-181">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dfe56-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dfe56-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dfe56-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfe56-183">Indica si el TPM está habilitado.</span><span class="sxs-lookup"><span data-stu-id="dfe56-183">Indicates whether the TPM is enabled.</span></span>

<span data-ttu-id="dfe56-184">**true** si el dispositivo está habilitado (es decir, si **IsEnabled \_ InitialValue** es true); en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="dfe56-184">**true** if the device is enabled (that is, if **IsEnabled\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="dfe56-185">Este valor se almacena cuando se crea una instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="dfe56-185">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="dfe56-186">Es posible que el TPM cambie el estado entre la creación de instancias y al comprobar este valor.</span><span class="sxs-lookup"><span data-stu-id="dfe56-186">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="dfe56-187">Para comprobar si el TPM está habilitado en tiempo real, use el método [**IsEnabled**](isenabled-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="dfe56-187">To check whether the TPM is enabled in real time, use the [**IsEnabled**](isenabled-win32-tpm.md) method.</span></span>

<span data-ttu-id="dfe56-188">**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="dfe56-188">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="dfe56-189">**IsOwned \_ InitialValue**</span><span class="sxs-lookup"><span data-stu-id="dfe56-189">**IsOwned\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfe56-190">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dfe56-190">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dfe56-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dfe56-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfe56-192">Indica si el TPM tiene un propietario.</span><span class="sxs-lookup"><span data-stu-id="dfe56-192">Indicates whether the TPM has an owner.</span></span>

<span data-ttu-id="dfe56-193">**true** si el dispositivo tiene un propietario (es decir, si **IsOwned \_ InitialValue** es true); en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="dfe56-193">**true** if the device has an owner (that is, if **IsOwned\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="dfe56-194">Este valor se almacena cuando se crea una instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="dfe56-194">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="dfe56-195">Es posible que el TPM cambie el estado entre la creación de instancias y al comprobar este valor.</span><span class="sxs-lookup"><span data-stu-id="dfe56-195">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="dfe56-196">Para comprobar si el TPM es propiedad de tiempo real, use el método [**IsOwned**](isowned-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="dfe56-196">To check whether the TPM is owned in real time, use the [**IsOwned**](isowned-win32-tpm.md) method.</span></span>

<span data-ttu-id="dfe56-197">**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="dfe56-197">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="dfe56-198">**ManufacturerId**</span><span class="sxs-lookup"><span data-stu-id="dfe56-198">**ManufacturerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfe56-199">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dfe56-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfe56-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dfe56-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfe56-201">La información de identificación que nombra de forma única al fabricante de TPM.</span><span class="sxs-lookup"><span data-stu-id="dfe56-201">The identifying information that uniquely names the TPM manufacturer.</span></span>

<span data-ttu-id="dfe56-202">Cuando los datos no están disponibles, se devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="dfe56-202">When the data is unavailable, zero is returned.</span></span>

<span data-ttu-id="dfe56-203">Este valor entero se puede traducir en un valor de cadena interpretando cada byte como un carácter ASCII.</span><span class="sxs-lookup"><span data-stu-id="dfe56-203">This integer value can be translated to a string value by interpreting each byte as an ASCII character.</span></span> <span data-ttu-id="dfe56-204">Por ejemplo, un valor entero de 1414548736 se puede dividir en estos 4 bytes: 0x54, 0x50, 0x4D y 0x00.</span><span class="sxs-lookup"><span data-stu-id="dfe56-204">For example, an integer value of 1414548736 can be divided into these 4 bytes: 0x54, 0x50, 0x4D, and 0x00.</span></span> <span data-ttu-id="dfe56-205">Suponiendo que la cadena se interpreta de izquierda a derecha, este valor entero se traduce en un valor de cadena de "TPM".</span><span class="sxs-lookup"><span data-stu-id="dfe56-205">Assuming the string is interpreted from left to right, this integer value translated to a string value of "TPM".</span></span>

</dd> <dt>

<span data-ttu-id="dfe56-206">**ManufacturerVersion**</span><span class="sxs-lookup"><span data-stu-id="dfe56-206">**ManufacturerVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfe56-207">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dfe56-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfe56-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dfe56-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfe56-209">La versión de TPM, tal como la especifica el fabricante.</span><span class="sxs-lookup"><span data-stu-id="dfe56-209">The version of the TPM, as specified by the manufacturer.</span></span>

<span data-ttu-id="dfe56-210">Cuando los datos no están disponibles, se devuelve "no compatible".</span><span class="sxs-lookup"><span data-stu-id="dfe56-210">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="dfe56-211">**ManufacturerVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="dfe56-211">**ManufacturerVersionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfe56-212">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dfe56-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfe56-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dfe56-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfe56-214">Otra información de versión específica del fabricante para el TPM.</span><span class="sxs-lookup"><span data-stu-id="dfe56-214">Other manufacturer-specific version information for the TPM.</span></span>

<span data-ttu-id="dfe56-215">Cuando los datos no están disponibles, se devuelve "no compatible".</span><span class="sxs-lookup"><span data-stu-id="dfe56-215">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="dfe56-216">**PhysicalPresenceVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="dfe56-216">**PhysicalPresenceVersionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfe56-217">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dfe56-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfe56-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dfe56-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfe56-219">La versión de la interfaz de presencia física, un mecanismo de comunicación que se usa para ejecutar operaciones de dispositivo que requieren presencia física, que el equipo admite.</span><span class="sxs-lookup"><span data-stu-id="dfe56-219">The version of the Physical Presence Interface, a communication mechanism used to run device operations that require physical presence, that the computer supports.</span></span>

<span data-ttu-id="dfe56-220">Esta interfaz debe estar disponible para ejecutar operaciones de presencia física de TPM.</span><span class="sxs-lookup"><span data-stu-id="dfe56-220">This interface must be available to run TPM physical presence operations.</span></span> <span data-ttu-id="dfe56-221">Los métodos de **\_ TPM de Win32** [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md)y [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) exponen las capacidades de la interfaz de presencia física.</span><span class="sxs-lookup"><span data-stu-id="dfe56-221">The **Win32\_Tpm** methods [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md), and [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) expose the capabilities of the Physical Presence Interface.</span></span>

<span data-ttu-id="dfe56-222">Cuando los datos no están disponibles, se devuelve "no compatible".</span><span class="sxs-lookup"><span data-stu-id="dfe56-222">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="dfe56-223">**SpecVersion**</span><span class="sxs-lookup"><span data-stu-id="dfe56-223">**SpecVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfe56-224">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dfe56-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfe56-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dfe56-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfe56-226">La versión de la especificación Trusted Computing Group (TCG) que admite el TPM.</span><span class="sxs-lookup"><span data-stu-id="dfe56-226">The version of the Trusted Computing Group (TCG) specification that the TPM supports.</span></span> <span data-ttu-id="dfe56-227">Este valor incluye la versión principal y secundaria de la especificación de TCG, el nivel de revisión de especificación y el nivel de revisión de erratas.</span><span class="sxs-lookup"><span data-stu-id="dfe56-227">This value includes the major and minor TCG specification version, the specification revision level, and the errata revision level.</span></span> <span data-ttu-id="dfe56-228">Todos los valores están en hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="dfe56-228">All values are in hexadecimal.</span></span> <span data-ttu-id="dfe56-229">Por ejemplo, una información de versión de "1,2, 2, 0" indica que el dispositivo se ha implementado para la especificación de TCG versión 1,2, revisión de nivel 2 y sin erratas.</span><span class="sxs-lookup"><span data-stu-id="dfe56-229">For example, a version information of "1.2, 2, 0" indicates that the device was implemented to TCG specification version 1.2, revision level 2, and with no errata.</span></span>

<span data-ttu-id="dfe56-230">Cuando los datos no están disponibles, se devuelve "no compatible".</span><span class="sxs-lookup"><span data-stu-id="dfe56-230">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dfe56-231">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dfe56-231">Remarks</span></span>

<span data-ttu-id="dfe56-232">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="dfe56-232">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="dfe56-233">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="dfe56-233">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="dfe56-234">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="dfe56-234">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="dfe56-235">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="dfe56-235">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dfe56-236">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfe56-236">Requirements</span></span>



| <span data-ttu-id="dfe56-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfe56-237">Requirement</span></span> | <span data-ttu-id="dfe56-238">Value</span><span class="sxs-lookup"><span data-stu-id="dfe56-238">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfe56-239">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dfe56-239">Minimum supported client</span></span><br/> | <span data-ttu-id="dfe56-240">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dfe56-240">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="dfe56-241">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dfe56-241">Minimum supported server</span></span><br/> | <span data-ttu-id="dfe56-242">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dfe56-242">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="dfe56-243">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dfe56-243">Namespace</span></span><br/>                | <span data-ttu-id="dfe56-244">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="dfe56-244">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="dfe56-245">MOF</span><span class="sxs-lookup"><span data-stu-id="dfe56-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dfe56-246"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dfe56-246"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="dfe56-247">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dfe56-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfe56-248"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="dfe56-248"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



 

 
