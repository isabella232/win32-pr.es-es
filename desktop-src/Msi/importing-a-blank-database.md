---
description: Para reproducir el ejemplo, debe copiar, o crear con una herramienta de software, un archivo de base de datos de Windows Installer.
ms.assetid: e239bbe4-3290-40f0-9f28-0e8aa4ed23f8
title: Importar una base de datos en blanco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b654b0de118013e8f211a9b06e896cc3f486faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277744"
---
# <a name="importing-a-blank-database"></a><span data-ttu-id="d63a9-103">Importar una base de datos en blanco</span><span class="sxs-lookup"><span data-stu-id="d63a9-103">Importing a Blank Database</span></span>

<span data-ttu-id="d63a9-104">Para reproducir el ejemplo, debe copiar, o crear con una herramienta de software, un archivo de base de datos de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d63a9-104">To reproduce the sample you need to copy, or create with a software tool, a Windows Installer database file.</span></span> <span data-ttu-id="d63a9-105">Se proporciona una base de datos de instalación totalmente vacía, Schema.msi, con los [componentes Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="d63a9-105">A totally blank installation database, Schema.msi, is provided with the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="d63a9-106">El SDK también proporciona una base de datos parcialmente vacía, uisample.msi, que contiene las tablas y los datos de secuencia sugeridos necesarios para una interfaz de usuario sencilla.</span><span class="sxs-lookup"><span data-stu-id="d63a9-106">The SDK also provides a partially blank database, uisample.msi, that contains the suggested sequence tables and data required for a simple user interface.</span></span> <span data-ttu-id="d63a9-107">Realice una copia de uisample.msi y muévala en el mismo directorio que contiene la carpeta del Bloc de notas que ha creado en [el planeamiento de la instalación](planning-the-installation.md).</span><span class="sxs-lookup"><span data-stu-id="d63a9-107">Make a copy of uisample.msi and move it into the same directory containing the Notepad folder you created in [Planning the Installation](planning-the-installation.md).</span></span> <span data-ttu-id="d63a9-108">Cambie el nombre del archivo MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="d63a9-108">Rename the file MNP2000.msi.</span></span> <span data-ttu-id="d63a9-109">El archivo de base de datos de instalación y los archivos de código fuente deben estar ubicados en la raíz del mismo directorio.</span><span class="sxs-lookup"><span data-stu-id="d63a9-109">The installation database file and the source files must both be located at the root of the same directory.</span></span> <span data-ttu-id="d63a9-110">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d63a9-110">For example:</span></span>

<span data-ttu-id="d63a9-111">C: \\MNP2000.msi de ejemplo \\</span><span class="sxs-lookup"><span data-stu-id="d63a9-111">C:\\Sample\\MNP2000.msi</span></span>

<span data-ttu-id="d63a9-112">C: \\ Bloc de notas de ejemplo </span><span class="sxs-lookup"><span data-stu-id="d63a9-112">C:\\Sample\\Notepad</span></span>\\\\

<span data-ttu-id="d63a9-113">Si no usa Uisample.msi, debe obtener una base de datos en blanco, como Schema.msi, y especificar información para la instalación mediante una herramienta de edición de bases de datos como orca, que se proporciona con el SDK u otro editor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="d63a9-113">If you do not use Uisample.msi, then you must obtain a blank database, such as Schema.msi, and enter information for the installation using a database editing tool such as Orca, which is provided with the SDK, or another database editor.</span></span>

[<span data-ttu-id="d63a9-114">Continuar</span><span class="sxs-lookup"><span data-stu-id="d63a9-114">Continue</span></span>](specifying-directory-structure.md)

 

 



