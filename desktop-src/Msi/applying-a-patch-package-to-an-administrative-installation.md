---
description: Puede aplicar la actualización pequeña a una imagen de origen administrativa de MNP2000.msi instalando la revisión de ejemplo MNP2000. MSP creada en la generación de un paquete de revisión.
ms.assetid: 24ae9cd6-2057-4345-90ec-943da7620cb0
title: Aplicar un paquete de revisión a una instalación administrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e0645bdd2c472e725a3a5eeef22693aa35b8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001750"
---
# <a name="applying-a-patch-package-to-an-administrative-installation"></a><span data-ttu-id="e8276-103">Aplicar un paquete de revisión a una instalación administrativa</span><span class="sxs-lookup"><span data-stu-id="e8276-103">Applying a Patch Package to an Administrative Installation</span></span>

<span data-ttu-id="e8276-104">Puede aplicar la actualización pequeña a una imagen de origen administrativa de MNP2000.msi instalando la revisión de ejemplo MNP2000. MSP creada en la [generación de un paquete de revisión](generating-a-patch-package.md).</span><span class="sxs-lookup"><span data-stu-id="e8276-104">You may apply the small update to an administrative source image of MNP2000.msi by installing the sample patch MNP2000.msp created in [Generating a Patch Package](generating-a-patch-package.md).</span></span> <span data-ttu-id="e8276-105">La actualización se puede propagar a los usuarios solicitando que vuelvan a instalar la aplicación desde la nueva imagen de origen administrativa.</span><span class="sxs-lookup"><span data-stu-id="e8276-105">The update can then be propagated to users by requesting that they reinstall the application from the new administrative source image.</span></span>

<span data-ttu-id="e8276-106">Un administrador puede usar la siguiente línea de comandos para actualizar la imagen de origen administrativa que se encuentra en//Server/MNP2000.msi a una nueva imagen de origen que sea igual que la que se produciría en una instalación administrativa desde un CD-ROM totalmente actualizado.</span><span class="sxs-lookup"><span data-stu-id="e8276-106">An administrator can use the following command line to update the administrative source image located at //server/MNP2000.msi to a new source image that is the same as would be produced by an administrative installation from a fully updated CD-ROM.</span></span>

<span data-ttu-id="e8276-107">**msiexec/a//Server/MNP2000.msi/p MNP2000. MSP**</span><span class="sxs-lookup"><span data-stu-id="e8276-107">**msiexec /a //server/MNP2000.msi /p MNP2000.msp**</span></span>

<span data-ttu-id="e8276-108">Los miembros del grupo de trabajo que usan MNP2000 deben volver a instalar la aplicación desde la nueva imagen de origen administrativa para recibir la actualización.</span><span class="sxs-lookup"><span data-stu-id="e8276-108">Members of the workgroup using MNP2000 then must reinstall the application from the new administrative source image to receive the update.</span></span>

<span data-ttu-id="e8276-109">Para reinstalar completamente las aplicaciones y almacenar en caché el archivo. msi actualizado en el equipo del usuario, los usuarios pueden escribir cualquiera de los siguientes comandos.</span><span class="sxs-lookup"><span data-stu-id="e8276-109">To completely reinstall the applications and cache the updated .msi file on the user's computer, users may enter either of the following commands.</span></span>

<span data-ttu-id="e8276-110">**msiexec/fvomus//Server/MNP2000.msi**</span><span class="sxs-lookup"><span data-stu-id="e8276-110">**msiexec /fvomus //server/MNP2000.msi**</span></span>

<span data-ttu-id="e8276-111">**msiexec/I//Server/MNP2000.msi REINSTALL = ALL REINSTALLMODE = vomus**</span><span class="sxs-lookup"><span data-stu-id="e8276-111">**msiexec /I //server/MNP2000.msi REINSTALL=ALL REINSTALLMODE=vomus**</span></span>

<span data-ttu-id="e8276-112">Para reinstalar solo la característica de concierto actualizada y almacenar en caché el archivo. msi actualizado en el equipo del usuario, los usuarios pueden escribir el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="e8276-112">To reinstall only the updated Concert feature and cache the updated .msi file on the user's computer, users may enter the following command.</span></span>

<span data-ttu-id="e8276-113">**msiexec/I//Server/MNP2000.msi REINSTALL = concierto REINSTALLMODE = vomus**</span><span class="sxs-lookup"><span data-stu-id="e8276-113">**msiexec /I //server/MNP2000.msi REINSTALL=Concert REINSTALLMODE=vomus**</span></span>

## <a name="next-example"></a><span data-ttu-id="e8276-114">Ejemplo siguiente</span><span class="sxs-lookup"><span data-stu-id="e8276-114">Next example</span></span>

[<span data-ttu-id="e8276-115">Un ejemplo de localización</span><span class="sxs-lookup"><span data-stu-id="e8276-115">A Localization Example</span></span>](a-localization-example.md)

 

 



