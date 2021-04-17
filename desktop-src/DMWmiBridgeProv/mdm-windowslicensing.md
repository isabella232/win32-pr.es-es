---
title: MDM_WindowsLicensing (clase)
description: La \_ clase WindowsLicensing de MDM está diseñada para escenarios de administración relacionados con licencias.
ms.assetid: 9b26d8dc-aab6-4c67-9dbc-4b53525b9354
keywords:
- MDM_WindowsLicensing (clase)
- MDM_WindowsLicensing clase, descrita
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing
- MDM_WindowsLicensing.InstanceID
- MDM_WindowsLicensing.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd77bbdb1a7e5c708ebcd955a0c8854c7c7404b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656521"
---
# <a name="mdm_windowslicensing-class"></a><span data-ttu-id="67759-105">\_Clase WindowsLicensing de MDM</span><span class="sxs-lookup"><span data-stu-id="67759-105">MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="67759-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="67759-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="67759-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="67759-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="67759-108">La **clase \_ WindowsLicensing de MDM** está diseñada para escenarios de administración relacionados con licencias.</span><span class="sxs-lookup"><span data-stu-id="67759-108">The **MDM\_WindowsLicensing** class is designed for licensing related management scenarios.</span></span> <span data-ttu-id="67759-109">Actualmente, el ámbito se limita a las actualizaciones de edición de dispositivos móviles y de escritorio de Windows 10, como Windows 10 Pro a Windows 10 Enterprise.</span><span class="sxs-lookup"><span data-stu-id="67759-109">Currently the scope is limited to edition upgrades of Windows 10 desktop and mobile devices, such as Windows 10 Pro to Windows 10 Enterprise.</span></span> <span data-ttu-id="67759-110">Además, este CSP proporciona la capacidad de activar o cambiar la clave de producto de los dispositivos de escritorio de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="67759-110">In addition, this CSP provides the capability to activate or change the product key of Windows 10 desktop devices.</span></span>

<span data-ttu-id="67759-111">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="67759-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="67759-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67759-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing
{
  string InstanceID;
  string ParentID;
  sint32 Edition;
  sint32 Status;
  string LicenseKeyType;
};
```

## <a name="members"></a><span data-ttu-id="67759-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="67759-113">Members</span></span>

<span data-ttu-id="67759-114">La **clase \_ WindowsLicensing de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="67759-114">The **MDM\_WindowsLicensing** class has these types of members:</span></span>

-   [<span data-ttu-id="67759-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="67759-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="67759-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="67759-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="67759-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="67759-117">Methods</span></span>

<span data-ttu-id="67759-118">La **clase \_ WindowsLicensing de MDM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="67759-118">The **MDM\_WindowsLicensing** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="67759-119">Método</span><span class="sxs-lookup"><span data-stu-id="67759-119">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="67759-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="67759-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="67759-121"><a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="67759-121"><a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="67759-122">Instala una clave de producto para dispositivos de escritorio de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="67759-122">Installs a product key for Windows 10 desktop devices.</span></span> <span data-ttu-id="67759-123">No se reinicia.</span><span class="sxs-lookup"><span data-stu-id="67759-123">Does not reboot.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="67759-124"><a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="67759-124"><a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="67759-125">Método para comprobar si se puede usar la clave de producto especificada para una actualización de edición, activación o cambio de una clave de producto de Windows 10 para dispositivos de escritorio.</span><span class="sxs-lookup"><span data-stu-id="67759-125">Method to check if the entered product key can be used for an edition upgrade, activation or changing a product key of Windows 10 for desktop devices.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="67759-126"><a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="67759-126"><a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="67759-127">Proporcione una licencia para una actualización de edición de dispositivos Windows 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="67759-127">Provide a license for an edition upgrade of Windows 10 mobile devices.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="67759-128">Este proceso de actualización no requiere un reinicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="67759-128">This upgrade process does not require a system restart.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="67759-129">El tipo de fecha es XML.</span><span class="sxs-lookup"><span data-stu-id="67759-129">The date type is XML.</span></span><br/> <span data-ttu-id="67759-130">La operación admitida es Execute.</span><span class="sxs-lookup"><span data-stu-id="67759-130">The supported operation is Execute.</span></span><br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="67759-131">El contenido del archivo de licencia XML debe tener un carácter de escape correcto (es decir, no debe ser simplemente un XML copiado), de lo contrario se producirá un error en la actualización de edición en dispositivos Windows 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="67759-131">The XML license file contents must be properly escaped (that is, it should not simply be a copied XML), otherwise the edition upgrade on Windows 10 mobile devices will fail.</span></span> <span data-ttu-id="67759-132">Para obtener más información sobre el escape correcto del archivo de licencia XML, vea la sección 2,4 de la <a href="https://www.w3.org/TR/xml/">especificación XML del consorcio W3C</a>. El archivo de licencia XML se adquiere del centro de servicios de licencias por volumen de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="67759-132">For more information on proper escaping of the XML license file, see Section 2.4 of the <a href="https://www.w3.org/TR/xml/">W3C XML spec</a>. The XML license file is acquired from the Microsoft Volume Licensing Service Center.</span></span> <span data-ttu-id="67759-133">Su organización debe tener un contrato de licencias por volumen con Microsoft para tener acceso al portal.</span><span class="sxs-lookup"><span data-stu-id="67759-133">Your organization must have a Volume Licensing contract with Microsoft to access the portal.</span></span>
</blockquote>
<br/> <span data-ttu-id="67759-134">A continuación se indican las rutas de actualización de la edición válidas al usar este nodo a través de un paquete MDM o de aprovisionamiento:</span><span class="sxs-lookup"><span data-stu-id="67759-134">The following are valid edition upgrade paths when using this node through an MDM or provisioning package:</span></span>
<ul>
<li><span data-ttu-id="67759-135">Windows 10 Mobile para Windows 10 Mobile Enterprise</span><span class="sxs-lookup"><span data-stu-id="67759-135">Windows 10 Mobileto Windows 10 Mobile Enterprise</span></span><br/></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="67759-136"><a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="67759-136"><a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="67759-137">Desencadena que el dispositivo tome la clave de producto y actualice la edición del cliente.</span><span class="sxs-lookup"><span data-stu-id="67759-137">Triggers the device to take the product key and upgrade the edition of the client.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="67759-138">Este proceso de actualización requiere un reinicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="67759-138">This upgrade process requires a system restart.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="67759-139">La operación admitida es Execute.</span><span class="sxs-lookup"><span data-stu-id="67759-139">The supported operation is Execute.</span></span><br/> <span data-ttu-id="67759-140">Cuando se inserta una clave de producto de un servidor MDM en el dispositivo de un usuario, <strong>changepk.exe</strong> se ejecuta con la clave de producto.</span><span class="sxs-lookup"><span data-stu-id="67759-140">When a product key is pushed from an MDM server to a user's device, <strong>changepk.exe</strong> runs using the product key.</span></span> <span data-ttu-id="67759-141">Una vez que se completa, se muestra una notificación al usuario que indica que hay disponible una nueva edición de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="67759-141">After it completes, a notification is shown to the user that a new edition of Windows 10 is available.</span></span> <span data-ttu-id="67759-142">Después, el usuario puede reiniciar el sistema manualmente o, después de dos horas, el dispositivo se reiniciará automáticamente para completar la actualización.</span><span class="sxs-lookup"><span data-stu-id="67759-142">The user can then restart their system manually or, after two hours, the device will restart automatically to complete the upgrade.</span></span> <span data-ttu-id="67759-143">El usuario recibirá una notificación de recordatorio 10 minutos antes del reinicio automático.</span><span class="sxs-lookup"><span data-stu-id="67759-143">The user will receive a reminder notification 10 minutes before the automatic restart.</span></span><br/> <span data-ttu-id="67759-144">Una vez que se reinicia el dispositivo, se completa el proceso de actualización de la edición.</span><span class="sxs-lookup"><span data-stu-id="67759-144">After the device restarts, the edition upgrade process completes.</span></span> <span data-ttu-id="67759-145">El usuario recibirá una notificación de la actualización correcta.</span><span class="sxs-lookup"><span data-stu-id="67759-145">The user will receive a notification of the successful upgrade.</span></span>
<blockquote>
[!Important]<br />
<span data-ttu-id="67759-146">Si otra directiva requiere que se reinicie el sistema cuando se está ejecutando <strong>changepk.exe</strong> , se producirá un error en la actualización de la edición.</span><span class="sxs-lookup"><span data-stu-id="67759-146">If another policy requires a system reboot that occurs when <strong>changepk.exe</strong> is running, the edition upgrade will fail.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="67759-147">Si se especifica una clave de producto en un paquete de aprovisionamiento y el usuario inicia la instalación del paquete, se muestra una notificación al usuario que indica que el sistema se reiniciará para completar la instalación del paquete.</span><span class="sxs-lookup"><span data-stu-id="67759-147">If a product key is entered in a provisioning package and the user begins installation of the package, a notification is shown to the user that their system will restart to complete the package installation.</span></span> <span data-ttu-id="67759-148">Tras el consentimiento explícito del usuario para continuar, el paquete continúa la instalación y <strong>changepk.exe</strong> se ejecuta con la clave de producto.</span><span class="sxs-lookup"><span data-stu-id="67759-148">Upon explicit consent from the user to proceed, the package continues installation and <strong>changepk.exe</strong> runs using the product key.</span></span> <span data-ttu-id="67759-149">El usuario recibirá una notificación de recordatorio de 30 segundos antes del reinicio automático.</span><span class="sxs-lookup"><span data-stu-id="67759-149">The user will receive a reminder notification 30 seconds before the automatic restart.</span></span> <br/> <span data-ttu-id="67759-150">Una vez que se reinicia el dispositivo, se completa el proceso de actualización de la edición.</span><span class="sxs-lookup"><span data-stu-id="67759-150">After the device restarts, the edition upgrade process completes.</span></span> <span data-ttu-id="67759-151">El usuario recibirá una notificación de la actualización correcta.</span><span class="sxs-lookup"><span data-stu-id="67759-151">The user will receive a notification of the successful upgrade.</span></span> <br/> <span data-ttu-id="67759-152">Este nodo también se puede usar para activar o cambiar una clave de producto en una edición determinada del dispositivo de escritorio de Windows 10 mediante la especificación de una clave de producto.</span><span class="sxs-lookup"><span data-stu-id="67759-152">This node can also be used to activate or change a product key on a particular edition of Windows 10 desktop device by entering a product key.</span></span> <span data-ttu-id="67759-153">La activación o el cambio de una clave de producto no requiere un reinicio y es un proceso silencioso para el usuario.</span><span class="sxs-lookup"><span data-stu-id="67759-153">Activation or changing a product key does not require a reboot and is a silent process for the user.</span></span><br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="67759-154">La clave de producto especificada debe tener 29 caracteres (es decir, debe incluir guiones); de lo contrario, se producirá un error en la activación, la actualización de edición o el cambio de clave de producto en los dispositivos de escritorio de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="67759-154">The product key entered must be 29 characters (that is, it should include dashes), otherwise the activation, edition upgrade, or product key change on Windows 10 desktop devices will fail.</span></span> <span data-ttu-id="67759-155">La clave de producto se adquiere del centro de servicios de licencias por volumen de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="67759-155">The product key is acquired from Microsoft Volume Licensing Service Center.</span></span> <span data-ttu-id="67759-156">Su organización debe tener un contrato de licencias por volumen con Microsoft para tener acceso al portal.</span><span class="sxs-lookup"><span data-stu-id="67759-156">Your organization must have a Volume Licensing contract with Microsoft to access the portal.</span></span>
</blockquote>
<br/> <span data-ttu-id="67759-157">A continuación se indican las rutas de actualización de edición válidas al usar este nodo a través de un MDM:</span><span class="sxs-lookup"><span data-stu-id="67759-157">The following are valid edition upgrade paths when using this node through an MDM:</span></span>
<ul>
<li><span data-ttu-id="67759-158">Educación de Windows 10 Enterprise a Windows 10</span><span class="sxs-lookup"><span data-stu-id="67759-158">Windows 10 Enterprise to Windows 10 Education</span></span></li>
<li><span data-ttu-id="67759-159">Windows 10 Home a Windows 10 Education</span><span class="sxs-lookup"><span data-stu-id="67759-159">Windows 10 Home to Windows 10 Education</span></span></li>
<li><span data-ttu-id="67759-160">Windows 10 Pro a Windows 10 Education</span><span class="sxs-lookup"><span data-stu-id="67759-160">Windows 10 Pro to Windows 10 Education</span></span></li>
<li><span data-ttu-id="67759-161">Windows 10 Pro a Windows 10 Enterprise</span><span class="sxs-lookup"><span data-stu-id="67759-161">Windows 10 Pro to Windows 10 Enterprise</span></span></li>
</ul>
<br/> <span data-ttu-id="67759-162">La activación o el cambio de una clave de producto se puede llevar a cabo en las siguientes ediciones:</span><span class="sxs-lookup"><span data-stu-id="67759-162">Activation or changing a product key can be carried out on the following editions:</span></span>
<ul>
<li><span data-ttu-id="67759-163">Windows 10 Education</span><span class="sxs-lookup"><span data-stu-id="67759-163">Windows 10 Education</span></span></li>
<li><span data-ttu-id="67759-164">Windows 10 Enterprise</span><span class="sxs-lookup"><span data-stu-id="67759-164">Windows 10 Enterprise</span></span></li>
<li><span data-ttu-id="67759-165">Windows 10 Home</span><span class="sxs-lookup"><span data-stu-id="67759-165">Windows 10 Home</span></span></li>
<li><span data-ttu-id="67759-166">Windows 10 Pro</span><span class="sxs-lookup"><span data-stu-id="67759-166">Windows 10 Pro</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="67759-167">Propiedades</span><span class="sxs-lookup"><span data-stu-id="67759-167">Properties</span></span>

<span data-ttu-id="67759-168">La **clase \_ WindowsLicensing de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="67759-168">The **MDM\_WindowsLicensing** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="67759-169">Edición</span><span class="sxs-lookup"><span data-stu-id="67759-169">Edition</span></span>](/windows/client-management/mdm/windowslicensing-csp#edition)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67759-170">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67759-170">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67759-171">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67759-171">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="67759-172">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="67759-172">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67759-173">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67759-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67759-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67759-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67759-175">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="67759-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="67759-176">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="67759-176">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="67759-177">LicenseKeyType</span><span class="sxs-lookup"><span data-stu-id="67759-177">LicenseKeyType</span></span>](/windows/client-management/mdm/windowslicensing-csp#licensekeytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67759-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67759-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67759-179">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67759-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="67759-180">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="67759-180">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67759-181">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67759-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67759-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67759-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67759-183">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="67759-183">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="67759-184">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="67759-184">Describes the full path to the parent node.</span></span> <span data-ttu-id="67759-185">Para esta clase, la cadena es "./Vendor/MSFT/".</span><span class="sxs-lookup"><span data-stu-id="67759-185">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="67759-186">Estado</span><span class="sxs-lookup"><span data-stu-id="67759-186">Status</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67759-187">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67759-187">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67759-188">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67759-188">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="67759-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67759-189">Requirements</span></span>



| <span data-ttu-id="67759-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="67759-190">Requirement</span></span> | <span data-ttu-id="67759-191">Value</span><span class="sxs-lookup"><span data-stu-id="67759-191">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67759-192">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67759-192">Minimum supported client</span></span><br/> | <span data-ttu-id="67759-193">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="67759-193">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="67759-194">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67759-194">Minimum supported server</span></span><br/> | <span data-ttu-id="67759-195">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="67759-195">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="67759-196">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="67759-196">Namespace</span></span><br/>                | <span data-ttu-id="67759-197">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="67759-197">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="67759-198">MOF</span><span class="sxs-lookup"><span data-stu-id="67759-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67759-199"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67759-199"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="67759-200">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="67759-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67759-201"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67759-201"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67759-202">Vea también</span><span class="sxs-lookup"><span data-stu-id="67759-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67759-203">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="67759-203">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

