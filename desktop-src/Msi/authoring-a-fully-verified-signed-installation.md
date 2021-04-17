---
description: Siga estas instrucciones para cubrir una instalación Windows Installer completa mediante una firma digital.
ms.assetid: e70eab94-4615-4a73-bccc-e16bd24551f6
title: Crear una instalación firmada completamente comprobada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e76bbfb77eab8b020cb1591847d2a36d09c96a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667038"
---
# <a name="authoring-a-fully-verified-signed-installation"></a><span data-ttu-id="e6228-103">Crear una instalación firmada completamente comprobada</span><span class="sxs-lookup"><span data-stu-id="e6228-103">Authoring a Fully Verified Signed Installation</span></span>

<span data-ttu-id="e6228-104">Puede usar estas instrucciones para cubrir una instalación Windows Installer completa mediante una firma digital.</span><span class="sxs-lookup"><span data-stu-id="e6228-104">You can use these guidelines to cover an entire Windows Installer installation by a digital signature.</span></span>

<span data-ttu-id="e6228-105">Los autores de instalaciones de Windows Installer deben cumplir los siguientes pasos para asegurarse de que todas las partes de la instalación están tratadas por una firma digital:</span><span class="sxs-lookup"><span data-stu-id="e6228-105">Authors of Windows Installer installations must adhere to the following to ensure that all parts of the installation are covered by a digital signature:</span></span>

-   <span data-ttu-id="e6228-106">Use archivos. cab internos, o bien use archivos. cab externos firmados y cree correctamente la tabla [MsiDigitalSignature](msidigitalsignature-table.md) y la [tabla MsiDigitalCertificate](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="e6228-106">Use internal cabinet files, or use signed external cabinet files and correctly author the [MsiDigitalSignature table](msidigitalsignature-table.md) and [MsiDigitalCertificate table](msidigitalcertificate-table.md).</span></span>
-   <span data-ttu-id="e6228-107">Use solo las acciones personalizadas almacenadas en el paquete o instaladas con el paquete.</span><span class="sxs-lookup"><span data-stu-id="e6228-107">Use only custom actions stored within the package or installed with the package.</span></span>
-   <span data-ttu-id="e6228-108">Firme el paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="e6228-108">Sign the installation package.</span></span>
-   <span data-ttu-id="e6228-109">Incluya una [tabla MsiPatchCertificate](msipatchcertificate-table.md) en el paquete.</span><span class="sxs-lookup"><span data-stu-id="e6228-109">Include an [MsiPatchCertificate table](msipatchcertificate-table.md) in the package.</span></span> <span data-ttu-id="e6228-110">Para habilitar la [revisión de control de cuentas de usuario (UAC)](user-account-control--uac--patching.md), esta tabla debe contener información utilizada para identificar los certificados de firmante que se usan para firmar revisiones digitalmente.</span><span class="sxs-lookup"><span data-stu-id="e6228-110">To enable [User Account Control (UAC) Patching](user-account-control--uac--patching.md), this table must contain information used to identify the signer certificates used to digitally sign patches.</span></span> <span data-ttu-id="e6228-111">La aplicación de revisiones de UAC permite al autor del paquete de instalación identificar revisiones firmadas digitalmente que los usuarios que no son administradores pueden aplicar en el futuro.</span><span class="sxs-lookup"><span data-stu-id="e6228-111">UAC patching enables the author of the installation package to identify digitally-signed patches that can be applied in the future by non-administrator users.</span></span>

<span data-ttu-id="e6228-112">Para ver un ejemplo en el que se muestra cómo crear una instalación firmada mediante automatización, vea [crear una instalación firmada completamente comprobada mediante automatización](authoring-a-fully-verified-signed-installation-using-automation.md).</span><span class="sxs-lookup"><span data-stu-id="e6228-112">For an example showing how to author a signed installation using automation, see [Authoring a Fully Verified Signed Installation Using Automation](authoring-a-fully-verified-signed-installation-using-automation.md).</span></span>

 

 



