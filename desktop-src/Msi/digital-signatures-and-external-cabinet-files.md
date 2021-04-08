---
description: Windows Installer puede utilizar firmas digitales para detectar recursos dañados.
ms.assetid: 49f1c1f9-d342-47e0-8888-2eadc5dbd000
title: Firmas digitales y archivos. cab externos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f10e921b324a43a919a417f47953c0a44e4777ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910957"
---
# <a name="digital-signatures-and-external-cabinet-files"></a><span data-ttu-id="dd133-103">Firmas digitales y archivos. cab externos</span><span class="sxs-lookup"><span data-stu-id="dd133-103">Digital Signatures and External Cabinet Files</span></span>

<span data-ttu-id="dd133-104">Windows Installer puede utilizar firmas digitales para detectar recursos dañados.</span><span class="sxs-lookup"><span data-stu-id="dd133-104">Windows Installer can use digital signatures to detect corrupted resources.</span></span> <span data-ttu-id="dd133-105">Al instalar un recurso externo, el certificado de firmante que pertenece al recurso se puede comprobar con un certificado de firma de referencia creado en el paquete.</span><span class="sxs-lookup"><span data-stu-id="dd133-105">When installing an external resource, the signer certificate belonging to the resource may be verified against a reference signer certificate authored in the package.</span></span> <span data-ttu-id="dd133-106">El instalador no puede comprobar las firmas de los archivadores internos.</span><span class="sxs-lookup"><span data-stu-id="dd133-106">The installer cannot verify signatures for internal cabinets.</span></span> <span data-ttu-id="dd133-107">Solo puede comprobar firmas digitales mediante la [tabla MsiDigitalSignature](msidigitalsignature-table.md) y la [tabla MsiDigitalCertificate](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="dd133-107">It can only verify digital signatures by using the [MsiDigitalSignature table](msidigitalsignature-table.md) and [MsiDigitalCertificate table](msidigitalcertificate-table.md).</span></span>

<span data-ttu-id="dd133-108">Windows Installer hace lo siguiente al instalar un archivo almacenado en un archivo. cab externo:</span><span class="sxs-lookup"><span data-stu-id="dd133-108">Windows Installer does the following when installing a file stored in an external cabinet:</span></span>

-   <span data-ttu-id="dd133-109">El instalador comprueba si la entrada de medios para ese contenedor externo aparece en la [tabla MsiDigitalSignature](msidigitalsignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="dd133-109">The installer checks to see whether the media entry for that external cabinet is listed in the [MsiDigitalSignature table](msidigitalsignature-table.md).</span></span> <span data-ttu-id="dd133-110">Un archivo almacenado en un archivo. cab externo se identifica con una entrada en la columna Cabinet de la [tabla de medios](media-table.md) que no tiene el prefijo " \# ".</span><span class="sxs-lookup"><span data-stu-id="dd133-110">A file stored in an external cabinet is identified by having an entry in the Cabinet column of the [Media table](media-table.md) that is not prefixed by a '\#' character.</span></span>
-   <span data-ttu-id="dd133-111">Antes de abrir el archivo. cab externo, el instalador llama a WinVerifyTrust para extraer la información del certificado y hash actual.</span><span class="sxs-lookup"><span data-stu-id="dd133-111">Before opening the external cabinet, the installer calls WinVerifyTrust to extract the current certificate and hash information.</span></span> <span data-ttu-id="dd133-112">Si hay una discrepancia entre la información de firma actual del archivo. cab y la información de firma creada en el paquete, se produce un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="dd133-112">If there is a mismatch between the current signature information on the cabinet and the signature information authored in the package, the installation fails.</span></span> <span data-ttu-id="dd133-113">Se produce un error en la instalación porque es posible que el archivo. cab se haya puesto en peligro y no sea de confianza.</span><span class="sxs-lookup"><span data-stu-id="dd133-113">The installation fails because the cabinet may have been compromised and cannot be trusted.</span></span>

<span data-ttu-id="dd133-114">Para obtener más información sobre el uso de firmas digitales, certificados digitales y [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust), consulte la sección [seguridad](https://msdn.microsoft.com/library/cc527452.aspx) del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="dd133-114">For more information regarding the use of digital signatures, digital certificates, and [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust), see the [Security](https://msdn.microsoft.com/library/cc527452.aspx) section of the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="dd133-115">Para obtener más información, vea [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), [MsiDigitalCertificate Table](msidigitalcertificate-table.md)y [MsiDigitalSignature Table](msidigitalsignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="dd133-115">For more information, see [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), [MsiDigitalCertificate table](msidigitalcertificate-table.md), and [MsiDigitalSignature table](msidigitalsignature-table.md).</span></span>

 

 
