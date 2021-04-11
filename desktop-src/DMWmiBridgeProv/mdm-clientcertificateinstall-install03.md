---
title: MDM_ClientCertificateInstall_Install03 (clase)
description: La \_ clase Install03 de ClientCertificateInstall de MDM \_ permite a la empresa establecer la instalación de certificados de cliente.
ms.assetid: 0083e54c-e621-47da-a20d-17c8bbf7dd3a
keywords:
- MDM_ClientCertificateInstall_Install03 (clase)
- MDM_ClientCertificateInstall_Install03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03
- MDM_ClientCertificateInstall_Install03.InstanceID
- MDM_ClientCertificateInstall_Install03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ac690808551e05d6ceba4f3c84bcaa521d4d01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150732"
---
# <a name="mdm_clientcertificateinstall_install03-class"></a><span data-ttu-id="09720-105">\_Clase Install03 ClientCertificateInstall de MDM \_</span><span class="sxs-lookup"><span data-stu-id="09720-105">MDM\_ClientCertificateInstall\_Install03 class</span></span>

<span data-ttu-id="09720-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="09720-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="09720-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="09720-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="09720-108">La **clase \_ \_ Install03 de ClientCertificateInstall de MDM** permite a la empresa establecer la instalación de certificados de cliente. Necesario para la inscripción de certificados SCEP.</span><span class="sxs-lookup"><span data-stu-id="09720-108">The **MDM\_ClientCertificateInstall\_Install03** class enables the enterprise to set the installation of client certificates.Required for SCEP certificate enrollment.</span></span> <span data-ttu-id="09720-109">Nodo primario para agrupar la solicitud relacionada con la instalación de certificados SCEP.</span><span class="sxs-lookup"><span data-stu-id="09720-109">Parent node to group SCEP cert install related request.</span></span>

> [!Note]  
> <span data-ttu-id="09720-110">Aunque los nodos secundarios de instalar admiten comandos Replace, después de que el comando exec se envíe al dispositivo, el dispositivo tomará los valores que se establecen cuando se acepta el comando exec.</span><span class="sxs-lookup"><span data-stu-id="09720-110">Even though the child nodes under Install support Replace commands, after the Exec command is sent to the device, the device will take the values which are set when the Exec command is accepted.</span></span> <span data-ttu-id="09720-111">El servidor no debería esperar que el cambio de valor del nodo después de que se acepte el comando exec afectará a la inscripción actual.</span><span class="sxs-lookup"><span data-stu-id="09720-111">The server should not expect the node value change after Exec command is accepted will impact the current undergoing enrollment.</span></span> <span data-ttu-id="09720-112">El servidor debe comprobar el valor del nodo de estado y asegurarse de que el dispositivo no está en fase desconocida antes de cambiar los valores de los nodos secundarios.</span><span class="sxs-lookup"><span data-stu-id="09720-112">The server should check the Status node value and make sure the device is not at unknown stage before changing child node values.</span></span>

 

<span data-ttu-id="09720-113">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="09720-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="09720-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09720-114">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_Install03
{
  string InstanceID;
  string ParentID;
  string ServerURL;
  string Challenge;
  string EKUMapping;
  sint32 KeyUsage;
  string SubjectName;
  sint32 KeyProtection;
  sint32 RetryDelay;
  sint32 RetryCount;
  string TemplateName;
  sint32 KeyLength;
  string HashAlgorithm;
  string CAThumbprint;
  string SubjectAlternativeNames;
  string ValidPeriod;
  sint32 ValidPeriodUnits;
  string ContainerName;
  string CustomTextToShowInPrompt;
  string AADKeyIdentifierList;
};
```

## <a name="members"></a><span data-ttu-id="09720-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="09720-115">Members</span></span>

<span data-ttu-id="09720-116">La **clase \_ \_ Install03 de MDM ClientCertificateInstall** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="09720-116">The **MDM\_ClientCertificateInstall\_Install03** class has these types of members:</span></span>

-   [<span data-ttu-id="09720-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="09720-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="09720-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="09720-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="09720-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="09720-119">Methods</span></span>

<span data-ttu-id="09720-120">La **clase \_ \_ Install03 de MDM ClientCertificateInstall** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="09720-120">The **MDM\_ClientCertificateInstall\_Install03** class has these methods.</span></span>



| <span data-ttu-id="09720-121">Método</span><span class="sxs-lookup"><span data-stu-id="09720-121">Method</span></span>                                                                      | <span data-ttu-id="09720-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="09720-122">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="09720-123">**EnrollMethod**</span><span class="sxs-lookup"><span data-stu-id="09720-123">**EnrollMethod**</span></span>](mdm-clientcertificateinstall-install03-enrollmethod.md) | <span data-ttu-id="09720-124">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="09720-124">Required.</span></span> <span data-ttu-id="09720-125">Desencadena el dispositivo para iniciar la inscripción de certificados.</span><span class="sxs-lookup"><span data-stu-id="09720-125">Triggers the device to start the certificate enrollment.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="09720-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="09720-126">Properties</span></span>

<span data-ttu-id="09720-127">La **clase \_ \_ Install03 de MDM ClientCertificateInstall** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="09720-127">The **MDM\_ClientCertificateInstall\_Install03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="09720-128">AADKeyIdentifierList</span><span class="sxs-lookup"><span data-stu-id="09720-128">AADKeyIdentifierList</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-aadkeyidentifierlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09720-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="09720-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09720-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09720-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="09720-131">CAThumbprint</span><span class="sxs-lookup"><span data-stu-id="09720-131">CAThumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-cathumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09720-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="09720-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09720-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09720-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="09720-134">Desafío</span><span class="sxs-lookup"><span data-stu-id="09720-134">Challenge</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-challenge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09720-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="09720-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09720-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09720-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="09720-137">ContainerName</span><span class="sxs-lookup"><span data-stu-id="09720-137">ContainerName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-containername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09720-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="09720-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09720-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09720-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="09720-140">CustomTextToShowInPrompt</span><span class="sxs-lookup"><span data-stu-id="09720-140">CustomTextToShowInPrompt</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-customtexttoshowinprompt)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09720-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="09720-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09720-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09720-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="09720-143">EKUMapping</span><span class="sxs-lookup"><span data-stu-id="09720-143">EKUMapping</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-ekumapping)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09720-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="09720-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09720-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09720-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="09720-146">HashAlgorithm</span><span class="sxs-lookup"><span data-stu-id="09720-146">HashAlgorithm</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-hashalgorithm)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09720-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="09720-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09720-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09720-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="09720-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="09720-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09720-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="09720-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09720-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="09720-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09720-152">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="09720-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="09720-153">Necesario para la inscripción de certificados SCEP.</span><span class="sxs-lookup"><span data-stu-id="09720-153">Required for SCEP certificate enrollment.</span></span> <span data-ttu-id="09720-154">Nodo primario para agrupar la solicitud relacionada con la instalación de certificados SCEP.</span><span class="sxs-lookup"><span data-stu-id="09720-154">Parent node to group SCEP cert install related request.</span></span>

<span data-ttu-id="09720-155">El formato es node.</span><span class="sxs-lookup"><span data-stu-id="09720-155">The Format is node.</span></span>

</dd> <dt>

[<span data-ttu-id="09720-156">KeyLength</span><span class="sxs-lookup"><span data-stu-id="09720-156">KeyLength</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-keylength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09720-157">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="09720-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="09720-158">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09720-158">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="09720-159">KeyProtection</span><span class="sxs-lookup"><span data-stu-id="09720-159">KeyProtection</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-keyprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09720-160">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="09720-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="09720-161">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09720-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="09720-162">KeyUsage</span><span class="sxs-lookup"><span data-stu-id="09720-162">KeyUsage</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09720-163">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="09720-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="09720-164">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09720-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="09720-165">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="09720-165">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09720-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="09720-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09720-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="09720-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09720-168">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="09720-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="09720-169">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="09720-169">Describes the full path to the parent node.</span></span>

<span data-ttu-id="09720-170">La cadena es "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall/SCEP/*UniqueID*"</span><span class="sxs-lookup"><span data-stu-id="09720-170">The string is "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall/SCEP/*UniqueID*"</span></span>

</dd> <dt>

[<span data-ttu-id="09720-171">RetryCount</span><span class="sxs-lookup"><span data-stu-id="09720-171">RetryCount</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-retrycount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09720-172">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="09720-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="09720-173">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09720-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="09720-174">RetryDelay</span><span class="sxs-lookup"><span data-stu-id="09720-174">RetryDelay</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-retrydelay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09720-175">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="09720-175">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="09720-176">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09720-176">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="09720-177">ServerURL</span><span class="sxs-lookup"><span data-stu-id="09720-177">ServerURL</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-serverurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09720-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="09720-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09720-179">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09720-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="09720-180">SubjectAlternativeNames</span><span class="sxs-lookup"><span data-stu-id="09720-180">SubjectAlternativeNames</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-subjectalternativenames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09720-181">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="09720-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09720-182">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09720-182">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="09720-183">SubjectName</span><span class="sxs-lookup"><span data-stu-id="09720-183">SubjectName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-subjectname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09720-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="09720-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09720-185">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09720-185">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="09720-186">TemplateName</span><span class="sxs-lookup"><span data-stu-id="09720-186">TemplateName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-templatename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09720-187">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="09720-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09720-188">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09720-188">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="09720-189">ValidPeriod</span><span class="sxs-lookup"><span data-stu-id="09720-189">ValidPeriod</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-validperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09720-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="09720-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09720-191">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09720-191">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="09720-192">ValidPeriodUnits</span><span class="sxs-lookup"><span data-stu-id="09720-192">ValidPeriodUnits</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-validperiodunits)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09720-193">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="09720-193">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="09720-194">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09720-194">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09720-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09720-195">Requirements</span></span>



| <span data-ttu-id="09720-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="09720-196">Requirement</span></span> | <span data-ttu-id="09720-197">Value</span><span class="sxs-lookup"><span data-stu-id="09720-197">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09720-198">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09720-198">Minimum supported client</span></span><br/> | <span data-ttu-id="09720-199">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="09720-199">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="09720-200">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09720-200">Minimum supported server</span></span><br/> | <span data-ttu-id="09720-201">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="09720-201">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="09720-202">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="09720-202">Namespace</span></span><br/>                | <span data-ttu-id="09720-203">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="09720-203">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="09720-204">MOF</span><span class="sxs-lookup"><span data-stu-id="09720-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09720-205"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09720-205"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="09720-206">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="09720-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09720-207"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09720-207"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09720-208">Vea también</span><span class="sxs-lookup"><span data-stu-id="09720-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09720-209">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="09720-209">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

