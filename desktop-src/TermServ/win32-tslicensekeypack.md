---
title: Clase Win32_TSLicenseKeyPack
description: Proporciona métodos y propiedades para ver e instalar los paquetes de claves de licencia de Servicios de Escritorio remoto.
ms.assetid: 27450646-c51f-4911-bb42-410794e32003
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseKeyPack clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSLicenseKeyPack de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack.KeyPackId
- Win32_TSLicenseKeyPack.Description
- Win32_TSLicenseKeyPack.KeyPackType
- Win32_TSLicenseKeyPack.ProductType
- Win32_TSLicenseKeyPack.ProductVersion
- Win32_TSLicenseKeyPack.ProductVersionID
- Win32_TSLicenseKeyPack.TotalLicenses
- Win32_TSLicenseKeyPack.IssuedLicenses
- Win32_TSLicenseKeyPack.AvailableLicenses
- Win32_TSLicenseKeyPack.ExpirationDate
- Win32_TSLicenseKeyPack.AccessRights
- Win32_TSLicenseKeyPack.TypeAndModel
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d78af398ebf7c137be5b31c9db427691a66a7a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533789"
---
# <a name="win32_tslicensekeypack-class"></a><span data-ttu-id="aa54e-105">\_Clase Win32 TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="aa54e-105">Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="aa54e-106">Proporciona métodos y propiedades para ver e instalar los paquetes de claves de licencia de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="aa54e-106">Provides methods and properties for viewing and installing Remote Desktop Services license key packs.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa54e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa54e-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseKeyPack
{
  uint32   KeyPackId;
  string   Description;
  uint32   KeyPackType;
  uint32   ProductType;
  string   ProductVersion;
  uint32   ProductVersionID;
  uint32   TotalLicenses;
  uint32   IssuedLicenses;
  uint32   AvailableLicenses;
  DATETIME ExpirationDate;
  uint32   AccessRights;
  string   TypeAndModel;
};
```

## <a name="members"></a><span data-ttu-id="aa54e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="aa54e-108">Members</span></span>

<span data-ttu-id="aa54e-109">La **clase \_ TSLicenseKeyPack de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="aa54e-109">The **Win32\_TSLicenseKeyPack** class has these types of members:</span></span>

-   [<span data-ttu-id="aa54e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="aa54e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="aa54e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aa54e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="aa54e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="aa54e-112">Methods</span></span>

<span data-ttu-id="aa54e-113">La clase **Win32 \_ TSLicenseKeyPack** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="aa54e-113">The **Win32\_TSLicenseKeyPack** class has these methods.</span></span>



| <span data-ttu-id="aa54e-114">Método</span><span class="sxs-lookup"><span data-stu-id="aa54e-114">Method</span></span>                                                                                                        | <span data-ttu-id="aa54e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa54e-115">Description</span></span>                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa54e-116">**ConvertLicenses**</span><span class="sxs-lookup"><span data-stu-id="aa54e-116">**ConvertLicenses**</span></span>](convertlicenses-win32-tslicensekeypack.md)                                             | <span data-ttu-id="aa54e-117">Convierte las licencias en el paquete de claves actual.</span><span class="sxs-lookup"><span data-stu-id="aa54e-117">Converts the licenses in the current key pack.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="aa54e-118">**ImportAgreementLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="aa54e-118">**ImportAgreementLicenseKeyPack**</span></span>](win32-tslicensekeypack-importagreementlicensekeypack.md)                 | <span data-ttu-id="aa54e-119">Importa, desde otro servidor de licencias de Escritorio remoto, un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un contrato de licencia y se conecta automáticamente a través de Internet para validar la licencia del paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="aa54e-119">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span><br/> |
| [<span data-ttu-id="aa54e-120">**ImportLicenseKeyPackOffline**</span><span class="sxs-lookup"><span data-stu-id="aa54e-120">**ImportLicenseKeyPackOffline**</span></span>](win32-tslicensekeypack-importlicensekeypackoffline.md)                     | <span data-ttu-id="aa54e-121">Importa, desde otro servidor de licencias de Escritorio remoto, un paquete de claves de licencia de Servicios de Escritorio remoto que utiliza un identificador de licencia recibido a través de Internet o del teléfono.</span><span class="sxs-lookup"><span data-stu-id="aa54e-121">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that uses a license identifier that was received over the Internet or the phone.</span></span><br/>                                               |
| [<span data-ttu-id="aa54e-122">**ImportOpenPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="aa54e-122">**ImportOpenPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-importopenpurchaselicensekeypack.md)           | <span data-ttu-id="aa54e-123">Importa, desde otro servidor de licencias de Escritorio remoto, un paquete de claves de licencia Open Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="aa54e-123">Imports, from another Remote Desktop license server, an Open License Remote Desktop Services license key pack.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="aa54e-124">**ImportRetailPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="aa54e-124">**ImportRetailPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-importretailpurchaselicensekeypack.md)       | <span data-ttu-id="aa54e-125">Importa, desde otro servidor de licencias de Escritorio remoto, un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un canal minorista.</span><span class="sxs-lookup"><span data-stu-id="aa54e-125">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span><br/>                                                                                   |
| [<span data-ttu-id="aa54e-126">**InstallAgreementLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="aa54e-126">**InstallAgreementLicenseKeyPack**</span></span>](installagreementlicensekeypack-win32-tslicensekeypack.md)               | <span data-ttu-id="aa54e-127">Instala un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de una licencia de contrato.</span><span class="sxs-lookup"><span data-stu-id="aa54e-127">Installs a Remote Desktop Services license key pack that was purchased through an agreement license.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="aa54e-128">**InstallLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="aa54e-128">**InstallLicenseKeyPack**</span></span>](installlicensekeypack-win32-tslicensekeypack.md)                                 | <span data-ttu-id="aa54e-129">Instala un paquete de claves de licencia Servicios de Escritorio remoto que utiliza un identificador de paquete de claves de licencia recibido a través de Internet o del teléfono.</span><span class="sxs-lookup"><span data-stu-id="aa54e-129">Installs a Remote Desktop Services license key pack that uses a license key pack ID that was received over the Internet or the phone.</span></span><br/>                                                                                          |
| [<span data-ttu-id="aa54e-130">**InstallOpenLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="aa54e-130">**InstallOpenLicenseKeyPack**</span></span>](installopenlicensekeypack-win32-tslicensekeypack.md)                         | <span data-ttu-id="aa54e-131">Instala un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un contrato de licencia abierto.</span><span class="sxs-lookup"><span data-stu-id="aa54e-131">Installs a Remote Desktop Services license key pack that was purchased through an open license agreement.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="aa54e-132">**InstallRetailPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="aa54e-132">**InstallRetailPurchaseLicenseKeyPack**</span></span>](installretailpurchaselicensekeypack-win32-tslicensekeypack.md)     | <span data-ttu-id="aa54e-133">Instala un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de una tienda de venta directa.</span><span class="sxs-lookup"><span data-stu-id="aa54e-133">Installs a Remote Desktop Services license key pack that was purchased through a retail store.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="aa54e-134">**ReinstallAgreementLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="aa54e-134">**ReinstallAgreementLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallagreementlicensekeypack.md)           | <span data-ttu-id="aa54e-135">Vuelve a instalar un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un contrato de licencia y se conecta automáticamente a través de Internet para validar la licencia del paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="aa54e-135">Reinstalls a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span><br/>                                           |
| [<span data-ttu-id="aa54e-136">**ReinstallLicenseKeyPackOffline**</span><span class="sxs-lookup"><span data-stu-id="aa54e-136">**ReinstallLicenseKeyPackOffline**</span></span>](win32-tslicensekeypack-reinstalllicensekeypackoffline.md)               | <span data-ttu-id="aa54e-137">Vuelve a instalar un paquete de claves de licencia Servicios de Escritorio remoto que usa el identificador de licencia que se recibió a través de Internet o el teléfono.</span><span class="sxs-lookup"><span data-stu-id="aa54e-137">Reinstalls a Remote Desktop Services license key pack that uses the license identifier that was received over the Internet or the phone.</span></span><br/>                                                                                       |
| [<span data-ttu-id="aa54e-138">**ReinstallOpenPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="aa54e-138">**ReinstallOpenPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallopenpurchaselicensekeypack.md)     | <span data-ttu-id="aa54e-139">Vuelve a instalar una licencia abierta Servicios de Escritorio remoto paquete de claves de licencia.</span><span class="sxs-lookup"><span data-stu-id="aa54e-139">Reinstalls an Open License Remote Desktop Services license key pack.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="aa54e-140">**ReinstallRetailPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="aa54e-140">**ReinstallRetailPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallretailpurchaselicensekeypack.md) | <span data-ttu-id="aa54e-141">Vuelve a instalar un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un canal de venta directa.</span><span class="sxs-lookup"><span data-stu-id="aa54e-141">Reinstalls a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="aa54e-142">**RemoveLicensesWithIdCount**</span><span class="sxs-lookup"><span data-stu-id="aa54e-142">**RemoveLicensesWithIdCount**</span></span>](win32-tslicensekeypack-removelicenseswithidcount.md)                         | <span data-ttu-id="aa54e-143">Quita el número especificado de licencias de Servicios de Escritorio remoto del paquete de claves especificado.</span><span class="sxs-lookup"><span data-stu-id="aa54e-143">Removes the specified number of Remote Desktop Services licenses from the specified key pack.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="aa54e-144">**UninstallLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="aa54e-144">**UninstallLicenseKeyPack**</span></span>](win32-tslicensekeypack-uninstalllicensekeypack.md)                             | <span data-ttu-id="aa54e-145">Desinstala un paquete de claves de licencia de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="aa54e-145">Uninstalls a Remote Desktop Services license key pack.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="aa54e-146">**UninstallLicenseKeyPackWithId**</span><span class="sxs-lookup"><span data-stu-id="aa54e-146">**UninstallLicenseKeyPackWithId**</span></span>](win32-tslicensekeypack-uninstalllicensekeypackwithid.md)                 | <span data-ttu-id="aa54e-147">Desinstala el paquete de claves de licencia de Servicios de Escritorio remoto con el identificador de paquete de claves especificado.</span><span class="sxs-lookup"><span data-stu-id="aa54e-147">Uninstalls the Remote Desktop Services license key pack with the specified key pack identifier.</span></span><br/>                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="aa54e-148">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aa54e-148">Properties</span></span>

<span data-ttu-id="aa54e-149">La **clase \_ TSLicenseKeyPack de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="aa54e-149">The **Win32\_TSLicenseKeyPack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aa54e-150">**AccessRights**</span><span class="sxs-lookup"><span data-stu-id="aa54e-150">**AccessRights**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa54e-151">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa54e-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa54e-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa54e-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa54e-153">Calificadores: [**mapa de bits**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "3"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("sesión de RD", "sesión de VDI", "Calista", "asociados de VDI")</span><span class="sxs-lookup"><span data-stu-id="aa54e-153">Qualifiers: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "3"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("RD Session", "VDI Session", "Calista", "VDI Partners")</span></span>
</dt> </dl>

<span data-ttu-id="aa54e-154">Calificador para derechos de acceso de paquete de claves de licencias TS</span><span class="sxs-lookup"><span data-stu-id="aa54e-154">Qualifier for TS Licensing key pack access rights</span></span>

</dd> <dt>

<span data-ttu-id="aa54e-155">**AvailableLicenses**</span><span class="sxs-lookup"><span data-stu-id="aa54e-155">**AvailableLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa54e-156">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa54e-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa54e-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa54e-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa54e-158">Número total de licencias disponibles en el paquete de claves de licencia de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="aa54e-158">Total number of available licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="aa54e-159">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aa54e-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa54e-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa54e-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa54e-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa54e-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa54e-162">Descripción del paquete de claves de licencia de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="aa54e-162">Description of the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="aa54e-163">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="aa54e-163">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa54e-164">Tipo de datos: **[DateTime](/windows/desktop/WmiSdk/datetime)**</span><span class="sxs-lookup"><span data-stu-id="aa54e-164">Data type: **[DATETIME](/windows/desktop/WmiSdk/datetime)**</span></span>
</dt> <dt>

<span data-ttu-id="aa54e-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa54e-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa54e-166">Fecha de expiración de la Servicios de Escritorio remoto paquete de claves de licencia.</span><span class="sxs-lookup"><span data-stu-id="aa54e-166">The expiration date of the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="aa54e-167">**IssuedLicenses**</span><span class="sxs-lookup"><span data-stu-id="aa54e-167">**IssuedLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa54e-168">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa54e-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa54e-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa54e-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa54e-170">Número total de licencias emitidas en el paquete de claves de licencia de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="aa54e-170">Total number of issued licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="aa54e-171">**KeyPackId**</span><span class="sxs-lookup"><span data-stu-id="aa54e-171">**KeyPackId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa54e-172">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa54e-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa54e-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa54e-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa54e-174">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aa54e-174">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="aa54e-175">Identificador del paquete de claves de licencia de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="aa54e-175">Identifier for the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="aa54e-176">**KeyPackType**</span><span class="sxs-lookup"><span data-stu-id="aa54e-176">**KeyPackType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa54e-177">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa54e-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa54e-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa54e-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa54e-179">Tipo de paquete de claves para el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="aa54e-179">Type of key pack for the Remote Desktop license server.</span></span>

| <span data-ttu-id="aa54e-180">Value</span><span class="sxs-lookup"><span data-stu-id="aa54e-180">Value</span></span> | <span data-ttu-id="aa54e-181">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa54e-181">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="aa54e-182">0</span><span class="sxs-lookup"><span data-stu-id="aa54e-182">0</span></span> | <span data-ttu-id="aa54e-183">No se conoce el tipo de paquete de claves de licencia Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="aa54e-183">The Remote Desktop Services license key pack type is unknown.</span></span> |
| <span data-ttu-id="aa54e-184">1</span><span class="sxs-lookup"><span data-stu-id="aa54e-184">1</span></span> | <span data-ttu-id="aa54e-185">El tipo de paquete de claves de licencia Servicios de Escritorio remoto es una compra comercial.</span><span class="sxs-lookup"><span data-stu-id="aa54e-185">The Remote Desktop Services license key pack type is a retail purchase.</span></span> |
| <span data-ttu-id="aa54e-186">2</span><span class="sxs-lookup"><span data-stu-id="aa54e-186">2</span></span> | <span data-ttu-id="aa54e-187">El tipo de paquete de claves de licencia Servicios de Escritorio remoto es una compra por volumen.</span><span class="sxs-lookup"><span data-stu-id="aa54e-187">The Remote Desktop Services license key pack type is a volume purchase.</span></span> |
| <span data-ttu-id="aa54e-188">3</span><span class="sxs-lookup"><span data-stu-id="aa54e-188">3</span></span> | <span data-ttu-id="aa54e-189">El tipo de paquete de claves de licencia Servicios de Escritorio remoto es una licencia simultánea.</span><span class="sxs-lookup"><span data-stu-id="aa54e-189">The Remote Desktop Services license key pack type is a concurrent license.</span></span> |
| <span data-ttu-id="aa54e-190">4</span><span class="sxs-lookup"><span data-stu-id="aa54e-190">4</span></span> | <span data-ttu-id="aa54e-191">El tipo de paquete de claves de licencia Servicios de Escritorio remoto es temporal.</span><span class="sxs-lookup"><span data-stu-id="aa54e-191">The Remote Desktop Services license key pack type is temporary.</span></span> |
| <span data-ttu-id="aa54e-192">5</span><span class="sxs-lookup"><span data-stu-id="aa54e-192">5</span></span> | <span data-ttu-id="aa54e-193">El tipo de paquete de claves de licencia Servicios de Escritorio remoto es una licencia abierta.</span><span class="sxs-lookup"><span data-stu-id="aa54e-193">The Remote Desktop Services license key pack type is an open license.</span></span> |
| <span data-ttu-id="aa54e-194">6</span><span class="sxs-lookup"><span data-stu-id="aa54e-194">6</span></span> | <span data-ttu-id="aa54e-195">No se admite.</span><span class="sxs-lookup"><span data-stu-id="aa54e-195">Not supported.</span></span> |

<span data-ttu-id="aa54e-196">**ProductType**</span><span class="sxs-lookup"><span data-stu-id="aa54e-196">**ProductType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa54e-197">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa54e-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa54e-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa54e-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa54e-199">Tipo de producto del paquete de claves de licencia de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="aa54e-199">Product type of the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="aa54e-200">Value</span><span class="sxs-lookup"><span data-stu-id="aa54e-200">Value</span></span> | <span data-ttu-id="aa54e-201">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa54e-201">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="aa54e-202">0</span><span class="sxs-lookup"><span data-stu-id="aa54e-202">0</span></span> | <span data-ttu-id="aa54e-203">El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa54e-203">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="aa54e-204">Por lo tanto, cada dispositivo que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia.</span><span class="sxs-lookup"><span data-stu-id="aa54e-204">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="aa54e-205">1</span><span class="sxs-lookup"><span data-stu-id="aa54e-205">1</span></span> | <span data-ttu-id="aa54e-206">El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por usuario.</span><span class="sxs-lookup"><span data-stu-id="aa54e-206">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="aa54e-207">Por lo tanto, cada usuario que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia.</span><span class="sxs-lookup"><span data-stu-id="aa54e-207">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="aa54e-208">2</span><span class="sxs-lookup"><span data-stu-id="aa54e-208">2</span></span> | <span data-ttu-id="aa54e-209">Este tipo de producto no es válido.</span><span class="sxs-lookup"><span data-stu-id="aa54e-209">This product type is not valid.</span></span> |

<span data-ttu-id="aa54e-210">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="aa54e-210">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa54e-211">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa54e-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa54e-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa54e-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa54e-213">Versión del producto para el paquete de claves de licencia de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="aa54e-213">Product version for the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="aa54e-214">Value</span><span class="sxs-lookup"><span data-stu-id="aa54e-214">Value</span></span> | <span data-ttu-id="aa54e-215">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa54e-215">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="aa54e-216">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="aa54e-216">"Windows Server 2012"</span></span> | <span data-ttu-id="aa54e-217">En esta licencia solo se admiten servidores que ejecuten Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="aa54e-217">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span> |
| <span data-ttu-id="aa54e-218">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="aa54e-218">"Windows Server 7"</span></span> | <span data-ttu-id="aa54e-219">Con esta licencia solo se admiten servidores que ejecuten Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="aa54e-219">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span> |
| <span data-ttu-id="aa54e-220">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="aa54e-220">"Windows Server 2008"</span></span> | <span data-ttu-id="aa54e-221">Este paquete de claves solo admite servidores que ejecuten Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="aa54e-221">Only servers running Windows Server 2008 are supported by this key pack.</span></span> |

<span data-ttu-id="aa54e-222">**ProductVersionID**</span><span class="sxs-lookup"><span data-stu-id="aa54e-222">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa54e-223">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa54e-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa54e-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa54e-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa54e-225">Identificador de la versión del producto para el paquete de claves de licencia de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="aa54e-225">Product version identifier for the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="aa54e-226">Value</span><span class="sxs-lookup"><span data-stu-id="aa54e-226">Value</span></span> | <span data-ttu-id="aa54e-227">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa54e-227">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="aa54e-228">0</span><span class="sxs-lookup"><span data-stu-id="aa54e-228">0</span></span> | <span data-ttu-id="aa54e-229">No compatible</span><span class="sxs-lookup"><span data-stu-id="aa54e-229">Not supported</span></span> |
| <span data-ttu-id="aa54e-230">1</span><span class="sxs-lookup"><span data-stu-id="aa54e-230">1</span></span> | <span data-ttu-id="aa54e-231">No compatible</span><span class="sxs-lookup"><span data-stu-id="aa54e-231">Not supported</span></span> |
| <span data-ttu-id="aa54e-232">2</span><span class="sxs-lookup"><span data-stu-id="aa54e-232">2</span></span> | <span data-ttu-id="aa54e-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa54e-233">Windows Server 2008</span></span> |
| <span data-ttu-id="aa54e-234">3</span><span class="sxs-lookup"><span data-stu-id="aa54e-234">3</span></span> | <span data-ttu-id="aa54e-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aa54e-235">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="aa54e-236">4</span><span class="sxs-lookup"><span data-stu-id="aa54e-236">4</span></span> | <span data-ttu-id="aa54e-237">Windows Server 2012 o Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="aa54e-237">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="aa54e-238">5</span><span class="sxs-lookup"><span data-stu-id="aa54e-238">5</span></span> | <span data-ttu-id="aa54e-239">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="aa54e-239">Windows Server 2016</span></span> |
| <span data-ttu-id="aa54e-240">6</span><span class="sxs-lookup"><span data-stu-id="aa54e-240">6</span></span> | <span data-ttu-id="aa54e-241">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="aa54e-241">Windows Server 2019</span></span> |

<span data-ttu-id="aa54e-242">**TotalLicenses**</span><span class="sxs-lookup"><span data-stu-id="aa54e-242">**TotalLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa54e-243">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa54e-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa54e-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa54e-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa54e-245">Número total de licencias en el paquete de claves de licencia de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="aa54e-245">Total number of licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="aa54e-246">**TypeAndModel**</span><span class="sxs-lookup"><span data-stu-id="aa54e-246">**TypeAndModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa54e-247">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa54e-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa54e-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa54e-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa54e-249">Calificador para el modelo y el tipo de paquete de claves de licencias de TS.</span><span class="sxs-lookup"><span data-stu-id="aa54e-249">Qualifier for TS Licensing key pack type and model.</span></span> <span data-ttu-id="aa54e-250">Ejemplos: licencias por suscripción de VDI por dispositivo, CAL por usuario de TS</span><span class="sxs-lookup"><span data-stu-id="aa54e-250">Examples: VDI Per Device subscription license, TS Per User CAL</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa54e-251">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa54e-251">Remarks</span></span>

<span data-ttu-id="aa54e-252">Para usar esta clase, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="aa54e-252">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="aa54e-253">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="aa54e-253">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="aa54e-254">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="aa54e-254">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="aa54e-255">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="aa54e-255">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="aa54e-256">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="aa54e-256">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa54e-257">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa54e-257">Requirements</span></span>



| <span data-ttu-id="aa54e-258">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa54e-258">Requirement</span></span> | <span data-ttu-id="aa54e-259">Value</span><span class="sxs-lookup"><span data-stu-id="aa54e-259">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa54e-260">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa54e-260">Minimum supported client</span></span><br/> | <span data-ttu-id="aa54e-261">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="aa54e-261">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="aa54e-262">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa54e-262">Minimum supported server</span></span><br/> | <span data-ttu-id="aa54e-263">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa54e-263">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="aa54e-264">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aa54e-264">Namespace</span></span><br/>                | <span data-ttu-id="aa54e-265">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="aa54e-265">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="aa54e-266">MOF</span><span class="sxs-lookup"><span data-stu-id="aa54e-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa54e-267"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa54e-267"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa54e-268">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aa54e-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa54e-269"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa54e-269"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa54e-270">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa54e-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa54e-271">**Win32 \_ TSIssuedLicense**</span><span class="sxs-lookup"><span data-stu-id="aa54e-271">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="aa54e-272">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="aa54e-272">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="aa54e-273">**Win32 \_ TSLicenseReportEntry**</span><span class="sxs-lookup"><span data-stu-id="aa54e-273">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="aa54e-274">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="aa54e-274">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

