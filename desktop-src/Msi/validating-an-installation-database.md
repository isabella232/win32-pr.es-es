---
description: Los autores de los paquetes de instalación siempre deben ejecutar la validación en sus paquetes antes de intentar instalar el paquete por primera vez y volver a ejecutar la validación cada vez que realice cambios en el paquete.
ms.assetid: 1f16a349-4919-46d2-9b78-2533b8679a73
title: Validar una base de datos de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6db262a280afa1d9222696d40a6f5949d69ece0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907612"
---
# <a name="validating-an-installation-database"></a><span data-ttu-id="450f1-103">Validar una base de datos de instalación</span><span class="sxs-lookup"><span data-stu-id="450f1-103">Validating an Installation Database</span></span>

<span data-ttu-id="450f1-104">Los autores de los paquetes de instalación siempre deben ejecutar la validación en sus paquetes antes de intentar instalar el paquete por primera vez y volver a ejecutar la validación cada vez que realice cambios en el paquete.</span><span class="sxs-lookup"><span data-stu-id="450f1-104">Authors of installation packages should always run validation on their packages before attempting to install the package for the first time and rerun validation whenever making any changes to the package.</span></span> <span data-ttu-id="450f1-105">La validación examina la base de datos en busca de errores que pueden parecer válidos de forma individual, pero que causan un comportamiento incorrecto en el contexto de toda la base de datos.</span><span class="sxs-lookup"><span data-stu-id="450f1-105">Validation scans the database for errors that may appear valid individually but that cause incorrect behavior in the context of the whole database.</span></span> <span data-ttu-id="450f1-106">Si intenta instalar un paquete que no supera la validación, puede dañar el sistema del usuario.</span><span class="sxs-lookup"><span data-stu-id="450f1-106">Attempting to install a package that fails validation can damage the user's system.</span></span> <span data-ttu-id="450f1-107">Vea las secciones [validación de paquetes](package-validation.md) y [evaluadores de coherencia interna-CIEM](internal-consistency-evaluators-ices.md).</span><span class="sxs-lookup"><span data-stu-id="450f1-107">See the sections [Package Validation](package-validation.md) and [Internal Consistency Evaluators - ICEs](internal-consistency-evaluators-ices.md).</span></span>

<span data-ttu-id="450f1-108">Puede validar el paquete de ejemplo mediante [Orca.exe](orca-exe.md) o [Msival2.exe](msival2-exe.md).</span><span class="sxs-lookup"><span data-stu-id="450f1-108">You can validate the sample package using [Orca.exe](orca-exe.md) or [Msival2.exe](msival2-exe.md).</span></span> <span data-ttu-id="450f1-109">Para ver la ayuda de Msival2.exe cambie los directorios y escriba en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="450f1-109">To view the help for Msival2.exe change directories and enter on the command line.</span></span>

<span data-ttu-id="450f1-110">Msival2 -?</span><span class="sxs-lookup"><span data-stu-id="450f1-110">Msival2 -?</span></span>

<span data-ttu-id="450f1-111">El archivo. Cub Darice. Cub contiene las acciones personalizadas de ICE que necesita Msival2.exe para realizar la validación.</span><span class="sxs-lookup"><span data-stu-id="450f1-111">The .cub file darice.cub contains the ICE custom actions needed by Msival2.exe to perform validation.</span></span> <span data-ttu-id="450f1-112">Para validar el MNP2000.msi escriba</span><span class="sxs-lookup"><span data-stu-id="450f1-112">To validate the MNP2000.msi enter</span></span>

<span data-ttu-id="450f1-113">msival2 MNP2000.msi Darice. Cub</span><span class="sxs-lookup"><span data-stu-id="450f1-113">msival2 MNP2000.msi Darice.cub</span></span>

<span data-ttu-id="450f1-114">Para obtener una descripción de los mensajes de error y de advertencia devueltos por la validación, consulte la [referencia de ICE](ice-reference.md).</span><span class="sxs-lookup"><span data-stu-id="450f1-114">For a description of the error and warning messages returned by validation see the [ICE Reference](ice-reference.md).</span></span> <span data-ttu-id="450f1-115">Corrija todos los errores del paquete y vuelva a ejecutar la validación según sea necesario hasta que el paquete pase la validación sin errores.</span><span class="sxs-lookup"><span data-stu-id="450f1-115">Correct all the errors in the package and rerun validation as necessary until the package passes validation without errors.</span></span>

<span data-ttu-id="450f1-116">Una vez que el paquete pasa la validación, puede instalar el paquete de ejemplo haciendo clic en el icono de MNP2000.msi o desde la línea de comandos con las opciones de la [línea de comandos](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="450f1-116">Once the package passes validation, you can install the sample package by clicking on the MNP2000.msi icon or from the command line using the [Command Line Options](command-line-options.md).</span></span>

<span data-ttu-id="450f1-117">Esto completa la instalación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="450f1-117">This completes the sample installation.</span></span>

## <a name="next-example"></a><span data-ttu-id="450f1-118">Ejemplo siguiente</span><span class="sxs-lookup"><span data-stu-id="450f1-118">Next example</span></span>

[<span data-ttu-id="450f1-119">Un ejemplo de actualización</span><span class="sxs-lookup"><span data-stu-id="450f1-119">An Upgrade Example</span></span>](an-upgrade-example.md)

 

 



