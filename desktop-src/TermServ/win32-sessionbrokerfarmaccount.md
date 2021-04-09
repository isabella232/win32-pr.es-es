---
title: Win32_SessionBrokerFarmAccount (clase)
description: La \_ clase Win32 SessionBrokerFarmAccount ya no está disponible para su uso a partir de Windows Server 2012. | Win32_SessionBrokerFarmAccount (clase)
ms.assetid: a76ade0f-cd94-438c-bc07-30dc4b4ee6c8
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerFarmAccount clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_SessionBrokerFarmAccount de clase, se describe
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount
- Win32_SessionBrokerFarmAccount.FarmName
- Win32_SessionBrokerFarmAccount.Manual
- Win32_SessionBrokerFarmAccount.AccountName
- Win32_SessionBrokerFarmAccount.AccountDomain
- Win32_SessionBrokerFarmAccount.AccountPassword
- Win32_SessionBrokerFarmAccount.AccountSPN1
- Win32_SessionBrokerFarmAccount.AccountSPN2
- Win32_SessionBrokerFarmAccount.ComputerDNSName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a31f076ddc6f9361be12a57dc60ada24ed75e4bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820823"
---
# <a name="win32_sessionbrokerfarmaccount-class"></a><span data-ttu-id="5f9ca-106">\_Clase Win32 SessionBrokerFarmAccount</span><span class="sxs-lookup"><span data-stu-id="5f9ca-106">Win32\_SessionBrokerFarmAccount class</span></span>

<span data-ttu-id="5f9ca-107">\[La clase **Win32 \_ SessionBrokerFarmAccount** ya no está disponible para su uso a partir de Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="5f9ca-107">\[The **Win32\_SessionBrokerFarmAccount** class is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="5f9ca-108">Define una cuenta de granja de agentes de sesiones.</span><span class="sxs-lookup"><span data-stu-id="5f9ca-108">Defines a session broker farm account.</span></span>

<span data-ttu-id="5f9ca-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5f9ca-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f9ca-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f9ca-110">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARMACCOUNT_Prov"), AMENDMENT]
class Win32_SessionBrokerFarmAccount
{
  string  FarmName;
  boolean Manual;
  string  AccountName;
  string  AccountDomain;
  string  AccountPassword;
  string  AccountSPN1;
  string  AccountSPN2;
  string  ComputerDNSName;
};
```

## <a name="members"></a><span data-ttu-id="5f9ca-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="5f9ca-111">Members</span></span>

<span data-ttu-id="5f9ca-112">La **clase \_ SessionBrokerFarmAccount de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5f9ca-112">The **Win32\_SessionBrokerFarmAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="5f9ca-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="5f9ca-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="5f9ca-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5f9ca-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5f9ca-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="5f9ca-115">Methods</span></span>

<span data-ttu-id="5f9ca-116">La clase **Win32 \_ SessionBrokerFarmAccount** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5f9ca-116">The **Win32\_SessionBrokerFarmAccount** class has these methods.</span></span>



| <span data-ttu-id="5f9ca-117">Método</span><span class="sxs-lookup"><span data-stu-id="5f9ca-117">Method</span></span>                                                      | <span data-ttu-id="5f9ca-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f9ca-118">Description</span></span>                          |
|:------------------------------------------------------------|:-------------------------------------|
| [<span data-ttu-id="5f9ca-119">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="5f9ca-119">**DeleteEx**</span></span>](deleteex-win32-sessionbrokerfarmaccount.md) | <span data-ttu-id="5f9ca-120">Elimina la cuenta de la granja.</span><span class="sxs-lookup"><span data-stu-id="5f9ca-120">Deletes the farm account.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5f9ca-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5f9ca-121">Properties</span></span>

<span data-ttu-id="5f9ca-122">La **clase \_ SessionBrokerFarmAccount de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5f9ca-122">The **Win32\_SessionBrokerFarmAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5f9ca-123">**AccountDomain**</span><span class="sxs-lookup"><span data-stu-id="5f9ca-123">**AccountDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f9ca-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5f9ca-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f9ca-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5f9ca-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5f9ca-126">Nombre del dominio al que pertenece la cuenta de la granja de servidores.</span><span class="sxs-lookup"><span data-stu-id="5f9ca-126">The name of the domain the farm account belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="5f9ca-127">**AccountName**</span><span class="sxs-lookup"><span data-stu-id="5f9ca-127">**AccountName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f9ca-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5f9ca-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f9ca-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5f9ca-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5f9ca-130">El nombre de la cuenta de la granja.</span><span class="sxs-lookup"><span data-stu-id="5f9ca-130">The name of the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="5f9ca-131">**AccountPassword**</span><span class="sxs-lookup"><span data-stu-id="5f9ca-131">**AccountPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f9ca-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5f9ca-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f9ca-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5f9ca-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5f9ca-134">La contraseña de la cuenta de la granja.</span><span class="sxs-lookup"><span data-stu-id="5f9ca-134">The password of the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="5f9ca-135">**AccountSPN1**</span><span class="sxs-lookup"><span data-stu-id="5f9ca-135">**AccountSPN1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f9ca-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5f9ca-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f9ca-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5f9ca-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f9ca-138">Primer nombre de entidad de seguridad de servicio (SPN) asociado a la cuenta de la granja.</span><span class="sxs-lookup"><span data-stu-id="5f9ca-138">The first service principal name (SPN) associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="5f9ca-139">**AccountSPN2**</span><span class="sxs-lookup"><span data-stu-id="5f9ca-139">**AccountSPN2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f9ca-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5f9ca-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f9ca-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5f9ca-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f9ca-142">El segundo SPN asociado a la cuenta de la granja.</span><span class="sxs-lookup"><span data-stu-id="5f9ca-142">The second SPN associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="5f9ca-143">**ComputerDNSName**</span><span class="sxs-lookup"><span data-stu-id="5f9ca-143">**ComputerDNSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f9ca-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5f9ca-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f9ca-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5f9ca-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5f9ca-146">Nombre DNS del equipo asociado a la cuenta de la granja.</span><span class="sxs-lookup"><span data-stu-id="5f9ca-146">The DNS name of the computer associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="5f9ca-147">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="5f9ca-147">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f9ca-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5f9ca-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f9ca-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5f9ca-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f9ca-150">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5f9ca-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5f9ca-151">El nombre de la granja de agentes de sesiones.</span><span class="sxs-lookup"><span data-stu-id="5f9ca-151">The name of the session broker farm.</span></span>

</dd> <dt>

<span data-ttu-id="5f9ca-152">**Manual**</span><span class="sxs-lookup"><span data-stu-id="5f9ca-152">**Manual**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f9ca-153">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5f9ca-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5f9ca-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5f9ca-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5f9ca-155">Indica si la contraseña de la cuenta se ha actualizado manualmente.</span><span class="sxs-lookup"><span data-stu-id="5f9ca-155">Indicates if the password for the account is updated manually.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f9ca-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f9ca-156">Requirements</span></span>



| <span data-ttu-id="5f9ca-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f9ca-157">Requirement</span></span> | <span data-ttu-id="5f9ca-158">Value</span><span class="sxs-lookup"><span data-stu-id="5f9ca-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f9ca-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f9ca-159">Minimum supported client</span></span><br/> | <span data-ttu-id="5f9ca-160">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5f9ca-160">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5f9ca-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f9ca-161">Minimum supported server</span></span><br/> | <span data-ttu-id="5f9ca-162">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5f9ca-162">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="5f9ca-163">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="5f9ca-163">End of client support</span></span><br/>    | <span data-ttu-id="5f9ca-164">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5f9ca-164">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5f9ca-165">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="5f9ca-165">End of server support</span></span><br/>    | <span data-ttu-id="5f9ca-166">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5f9ca-166">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="5f9ca-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5f9ca-167">Namespace</span></span><br/>                | <span data-ttu-id="5f9ca-168">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5f9ca-168">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="5f9ca-169">MOF</span><span class="sxs-lookup"><span data-stu-id="5f9ca-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f9ca-170"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f9ca-170"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f9ca-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5f9ca-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f9ca-172"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f9ca-172"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

