---
description: Puede aplicar la actualización pequeña a una instalación local de MNP2000 con la revisión de ejemplo MNPpatch. MSP creada en la generación de un paquete de revisión.
ms.assetid: 928182ae-5ddb-446f-a9b8-e8b3aa4ce49c
title: Aplicar un paquete de revisión a una instalación local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09ca0372870d46db67b49c0571045aadabf54c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276527"
---
# <a name="applying-a-patch-package-to-a-local-installation"></a><span data-ttu-id="b785a-103">Aplicar un paquete de revisión a una instalación local</span><span class="sxs-lookup"><span data-stu-id="b785a-103">Applying a Patch Package to a Local Installation</span></span>

<span data-ttu-id="b785a-104">Puede aplicar la actualización pequeña a una instalación local de MNP2000 con la revisión de ejemplo MNPpatch. MSP creada en la [generación de un paquete de revisión](generating-a-patch-package.md).</span><span class="sxs-lookup"><span data-stu-id="b785a-104">You may apply the small update to a local installation of MNP2000 with the sample patch MNPpatch.msp created in [Generating a Patch Package](generating-a-patch-package.md).</span></span> <span data-ttu-id="b785a-105">El procedimiento general se describe en la sección [aplicar actualizaciones pequeñas mediante la revisión de la instalación local del producto](applying-small-updates-by-patching-the-local-installation-of-the-product.md).</span><span class="sxs-lookup"><span data-stu-id="b785a-105">The general procedure is discussed in the section [Applying Small Updates by Patching the Local Installation of the Product](applying-small-updates-by-patching-the-local-installation-of-the-product.md).</span></span>

<span data-ttu-id="b785a-106">Instale el producto MNP2000 original localmente en el equipo.</span><span class="sxs-lookup"><span data-stu-id="b785a-106">Install the original MNP2000 product locally on your computer.</span></span> <span data-ttu-id="b785a-107">Compruebe que tiene el error Concert.txt que la actualización pequeña se va a corregir.</span><span class="sxs-lookup"><span data-stu-id="b785a-107">Verify that this has the error Concert.txt that the small update is to fix.</span></span> <span data-ttu-id="b785a-108">Después, inicie la instalación escribiendo la siguiente línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="b785a-108">Next launch the installation by entering the following command line.</span></span>

<span data-ttu-id="b785a-109">**msiexec/p MNP2000. MSP REINSTALL = ALL REINSTALLMODE = OMUs**</span><span class="sxs-lookup"><span data-stu-id="b785a-109">**msiexec /p MNP2000.msp REINSTALL=ALL REINSTALLMODE=omus**</span></span>

<span data-ttu-id="b785a-110">Reexamine el Concert.txt que pertenece a MNP2000 para comprobar que el instalador ha aplicado la actualización pequeña para corregir este archivo.</span><span class="sxs-lookup"><span data-stu-id="b785a-110">Reexamine the Concert.txt belonging to MNP2000 to verify that the installer has applied the small update to fix this file.</span></span>

<span data-ttu-id="b785a-111">Para aplicar la actualización pequeña a una imagen administrativa, consulte [aplicar un paquete de revisión a una instalación administrativa](applying-a-patch-package-to-an-administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="b785a-111">To apply the small update to an administrative image, see [Applying a Patch Package to an Administrative Installation](applying-a-patch-package-to-an-administrative-installation.md).</span></span>

[<span data-ttu-id="b785a-112">Continuar</span><span class="sxs-lookup"><span data-stu-id="b785a-112">Continue</span></span>](applying-a-patch-package-to-an-administrative-installation.md)

 

 



