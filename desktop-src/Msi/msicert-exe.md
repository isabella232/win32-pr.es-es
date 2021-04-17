---
description: Windows Installer puede utilizar firmas digitales como medio para detectar recursos dañados.
ms.assetid: fc982813-583b-4fcd-88d8-9de227994e7b
title: Msicert.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0a4df800bbcfa9ed2fb0d016794b3ebcf1535be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279340"
---
# <a name="msicertexe"></a><span data-ttu-id="e9a42-103">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="e9a42-103">Msicert.exe</span></span>

<span data-ttu-id="e9a42-104">Windows Installer puede utilizar firmas digitales como medio para detectar recursos dañados.</span><span class="sxs-lookup"><span data-stu-id="e9a42-104">Windows Installer can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="e9a42-105">Un certificado de firmante puede compararse con el certificado de firma de un recurso externo que debe instalar el paquete.</span><span class="sxs-lookup"><span data-stu-id="e9a42-105">A signer certificate may be compared to the signer certificate of an external resource to be installed by the package.</span></span> <span data-ttu-id="e9a42-106">Para obtener más información, consulte [firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="e9a42-106">For more information, see [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

<span data-ttu-id="e9a42-107">MsiCert.exe es una utilidad de línea de comandos que se puede usar para rellenar la tabla [MsiDigitalSignature](msidigitalsignature-table.md) y la [tabla MsiDigitalCertificate](msidigitalcertificate-table.md) con la información de la firma digital de un archivo. cab externo.</span><span class="sxs-lookup"><span data-stu-id="e9a42-107">MsiCert.exe is a command line utility that can be used to populate the [MsiDigitalSignature table](msidigitalsignature-table.md) and [MsiDigitalCertificate table](msidigitalcertificate-table.md) with the digital signature information of an external cabinet file.</span></span> <span data-ttu-id="e9a42-108">El archivo. cab debe firmarse digitalmente y mostrarse en la [tabla de medios](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="e9a42-108">The cabinet file must by digitally signed and listed in the [Media table](media-table.md).</span></span> <span data-ttu-id="e9a42-109">MsiCert.exe usa la información del certificado del firmante del archivo. CAB firmado digitalmente y creará y agregará las tablas MsiDigitalSignature y MsiDigitalCertificate a la base de datos, si aún no existen.</span><span class="sxs-lookup"><span data-stu-id="e9a42-109">MsiCert.exe uses the signer certificate information from the digitally signed cabinet and will create and add the MsiDigitalSignature and MsiDigitalCertificate tables to the database if they do not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9a42-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9a42-110">Syntax</span></span>

<span data-ttu-id="e9a42-111">**msicert-d** *{Database}* **-m** *{media entry}* **-c** *{Cabinet}* **\[ -h \]**</span><span class="sxs-lookup"><span data-stu-id="e9a42-111">**msicert -d** *{database}* **-m** *{media entry}* **-c** *{cabinet}* **\[-h\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="e9a42-112">Opciones de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="e9a42-112">Command Line Options</span></span>

<span data-ttu-id="e9a42-113">Las opciones de la línea de comandos no distinguen mayúsculas de minúsculas y se pueden usar delimitadores de barra diagonal en lugar de un guión.</span><span class="sxs-lookup"><span data-stu-id="e9a42-113">The command line options are case-insensitive and slash delimiters may be used instead of a dash.</span></span>



| <span data-ttu-id="e9a42-114">Opción</span><span class="sxs-lookup"><span data-stu-id="e9a42-114">Option</span></span> | <span data-ttu-id="e9a42-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e9a42-115">Parameter</span></span>        | <span data-ttu-id="e9a42-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9a42-116">Description</span></span>                                                                                             |
|--------|------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9a42-117">-d</span><span class="sxs-lookup"><span data-stu-id="e9a42-117">-d</span></span>     | <database> | <span data-ttu-id="e9a42-118">La base de datos (archivo. msi) que se está actualizando.</span><span class="sxs-lookup"><span data-stu-id="e9a42-118">The database (.msi file) that is being updated.</span></span>                                                         |
| <span data-ttu-id="e9a42-119">-M</span><span class="sxs-lookup"><span data-stu-id="e9a42-119">-m</span></span>     | <media Id> | <span data-ttu-id="e9a42-120">La entrada en el campo de despatín de la [tabla de medios](media-table.md) en el registro del archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="e9a42-120">The entry in the DiskId field of the [Media table](media-table.md) in the record for the cabinet file.</span></span> |
| <span data-ttu-id="e9a42-121">-c</span><span class="sxs-lookup"><span data-stu-id="e9a42-121">-c</span></span>     | <cabinet>  | <span data-ttu-id="e9a42-122">La ruta de acceso al archivo. CAB firmado digitalmente.</span><span class="sxs-lookup"><span data-stu-id="e9a42-122">The path to the digitally signed cabinet file.</span></span>                                                          |
| <span data-ttu-id="e9a42-123">-H</span><span class="sxs-lookup"><span data-stu-id="e9a42-123">-h</span></span>     |                  | <span data-ttu-id="e9a42-124">Incluye el hash de la firma digital.</span><span class="sxs-lookup"><span data-stu-id="e9a42-124">Include the hash of the digital signature.</span></span> <span data-ttu-id="e9a42-125">Esto es opcional.</span><span class="sxs-lookup"><span data-stu-id="e9a42-125">This is optional.</span></span>                                            |



 

<span data-ttu-id="e9a42-126">Esta herramienta solo está disponible en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="e9a42-126">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9a42-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e9a42-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9a42-128">Herramientas de desarrollo de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e9a42-128">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="e9a42-129">Versiones publicadas, herramientas y redistribuibles</span><span class="sxs-lookup"><span data-stu-id="e9a42-129">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



