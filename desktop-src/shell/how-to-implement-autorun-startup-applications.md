---
description: En esencia, no hay restricciones en cuanto a cómo escribir una aplicación de inicio de ejecución automática.
ms.assetid: 6D95E5F0-8D93-47A8-9D8C-49CBDCA150A7
title: Cómo implementar aplicaciones de inicio de ejecución automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b553e102f574835103898b17558541000633412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001907"
---
# <a name="how-to-implement-autorun-startup-applications"></a><span data-ttu-id="8c71f-103">Cómo implementar aplicaciones de inicio de ejecución automática</span><span class="sxs-lookup"><span data-stu-id="8c71f-103">How to Implement AutoRun Startup Applications</span></span>

<span data-ttu-id="8c71f-104">En esencia, no hay restricciones en cuanto a cómo escribir una aplicación de inicio de ejecución automática.</span><span class="sxs-lookup"><span data-stu-id="8c71f-104">There are essentially no constraints on how to write an AutoRun startup application.</span></span> <span data-ttu-id="8c71f-105">Puede implementar la aplicación de inicio para hacer todo lo que encuentre necesario para instalar, desinstalar, configurar o ejecutar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8c71f-105">You can implement the startup application to do whatever you find necessary to install, uninstall, configure, or run your application.</span></span> <span data-ttu-id="8c71f-106">Sin embargo, las siguientes sugerencias proporcionan algunas instrucciones para implementar una aplicación de inicio de ejecución automática en vigor.</span><span class="sxs-lookup"><span data-stu-id="8c71f-106">However, the following tips provide some guidelines to implementing an effective AutoRun startup application.</span></span>

## <a name="instructions"></a><span data-ttu-id="8c71f-107">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="8c71f-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="8c71f-108">Paso 1:</span><span class="sxs-lookup"><span data-stu-id="8c71f-108">Step 1:</span></span>

<span data-ttu-id="8c71f-109">Asegúrese de que los usuarios reciben los comentarios lo antes posible después de insertar un disco de ejecución automática en la unidad.</span><span class="sxs-lookup"><span data-stu-id="8c71f-109">Make sure that users receive feedback as soon as possible after they insert an AutoRun disc into the drive.</span></span> <span data-ttu-id="8c71f-110">Las aplicaciones de inicio deben ser programas pequeños que se cargan rápidamente.</span><span class="sxs-lookup"><span data-stu-id="8c71f-110">Startup applications should be small programs that load quickly.</span></span> <span data-ttu-id="8c71f-111">Deben identificar claramente la aplicación y proporcionar una manera sencilla de cancelar la operación.</span><span class="sxs-lookup"><span data-stu-id="8c71f-111">They should clearly identify the application and provide an easy way to cancel the operation.</span></span>

### <a name="step-2"></a><span data-ttu-id="8c71f-112">Paso 2:</span><span class="sxs-lookup"><span data-stu-id="8c71f-112">Step 2:</span></span>

<span data-ttu-id="8c71f-113">Compruebe si el programa ya está instalado.</span><span class="sxs-lookup"><span data-stu-id="8c71f-113">Check to see if the program is already installed.</span></span> <span data-ttu-id="8c71f-114">Si no es así, el paso siguiente será probablemente el procedimiento de instalación.</span><span class="sxs-lookup"><span data-stu-id="8c71f-114">If not, the next step will probably be the setup procedure.</span></span> <span data-ttu-id="8c71f-115">La aplicación de inicio puede aprovechar las ventajas del tiempo que el usuario emplea en leer el cuadro de diálogo al iniciar otro subproceso para empezar a cargar el código de instalación.</span><span class="sxs-lookup"><span data-stu-id="8c71f-115">The startup application can take advantage of the time the user spends reading the dialog box by starting another thread to begin loading the setup code.</span></span> <span data-ttu-id="8c71f-116">En el momento en que el usuario hace clic en **Aceptar**, el programa de instalación ya estará en parte si no se ha cargado por completo.</span><span class="sxs-lookup"><span data-stu-id="8c71f-116">By the time the user clicks **OK**, your setup program will already be partly if not fully loaded.</span></span> <span data-ttu-id="8c71f-117">Este enfoque reduce significativamente la percepción del usuario de la cantidad de tiempo que se tarda en cargar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8c71f-117">This approach significantly reduces the user's perception of the amount of time it takes to load your application.</span></span>

> [!Note]  
> <span data-ttu-id="8c71f-118">Normalmente, la parte inicial de la aplicación de inicio presenta a los usuarios una interfaz de usuario, como un cuadro de diálogo, preguntándoles cómo desea continuar.</span><span class="sxs-lookup"><span data-stu-id="8c71f-118">Typically, the initial part of the startup application presents users with a user interface, such as a dialog box, asking them how they would like to proceed.</span></span>

 

### <a name="step-3"></a><span data-ttu-id="8c71f-119">Paso 3:</span><span class="sxs-lookup"><span data-stu-id="8c71f-119">Step 3:</span></span>

<span data-ttu-id="8c71f-120">Inicie otro subproceso para empezar a cargar código de aplicación para acortar el tiempo de espera del usuario.</span><span class="sxs-lookup"><span data-stu-id="8c71f-120">Start another thread to begin loading application code to shorten the waiting time for the user.</span></span> <span data-ttu-id="8c71f-121">Si ya se ha instalado la aplicación, es probable que el usuario haya insertado el disco para ejecutar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8c71f-121">If the application has already been installed, the user probably inserted the disk to run the application.</span></span>

### <a name="step-4"></a><span data-ttu-id="8c71f-122">Paso 4:</span><span class="sxs-lookup"><span data-stu-id="8c71f-122">Step 4:</span></span>

<span data-ttu-id="8c71f-123">Use las siguientes sugerencias para minimizar el uso del disco duro:</span><span class="sxs-lookup"><span data-stu-id="8c71f-123">Use the following hints to minimize hard disk usage:</span></span>

-   <span data-ttu-id="8c71f-124">Mantenga el número mínimo de archivos que deben estar en el disco duro.</span><span class="sxs-lookup"><span data-stu-id="8c71f-124">Keep the number of files that must be on the hard disk to a minimum.</span></span> <span data-ttu-id="8c71f-125">Deben estar restringidos a los archivos que son esenciales para ejecutar el programa o que tardarán una cantidad de tiempo inaceptablemente grande en leerse desde el medio.</span><span class="sxs-lookup"><span data-stu-id="8c71f-125">They should be restricted to files that are essential to running the program or that would take an unacceptably large amount of time to read from the media.</span></span>
-   <span data-ttu-id="8c71f-126">En muchos casos, no es necesario instalar archivos no esenciales en el disco duro, pero puede proporcionar ventajas como el aumento del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="8c71f-126">In many cases, installing nonessential files on the hard disk is not necessary, but might provide benefits such as increased performance.</span></span> <span data-ttu-id="8c71f-127">Ofrezca al usuario la opción de decidir cómo sacar el equilibrio entre los costos y las ventajas del almacenamiento en disco duro.</span><span class="sxs-lookup"><span data-stu-id="8c71f-127">Give the user the option of deciding how to make the trade-off between the costs and benefits of hard disk storage.</span></span>
-   <span data-ttu-id="8c71f-128">Proporcionan una manera de desinstalar los componentes que se colocaron en el disco duro.</span><span class="sxs-lookup"><span data-stu-id="8c71f-128">Provide a way to uninstall any components that were placed on the hard disk.</span></span>
-   <span data-ttu-id="8c71f-129">Si la aplicación almacena en caché los datos, conceda al usuario algún control sobre él.</span><span class="sxs-lookup"><span data-stu-id="8c71f-129">If your application caches data, give the user some control over it.</span></span> <span data-ttu-id="8c71f-130">Incluir opciones en la aplicación de inicio, como establecer un límite en la cantidad máxima de datos almacenados en caché que se almacenarán en el disco duro, o hacer que la aplicación descarte los datos almacenados en caché cuando finalice.</span><span class="sxs-lookup"><span data-stu-id="8c71f-130">Include options in the startup application such as setting a limit on the maximum amount of cached data that will be stored on the hard disk, or having the application discard any cached data when it terminates.</span></span>

### <a name="step-5"></a><span data-ttu-id="8c71f-131">Paso 5:</span><span class="sxs-lookup"><span data-stu-id="8c71f-131">Step 5:</span></span>

<span data-ttu-id="8c71f-132">Deshabilite la ejecución automática si es necesario.</span><span class="sxs-lookup"><span data-stu-id="8c71f-132">Disable Autorun if needed.</span></span> <span data-ttu-id="8c71f-133">La ejecución automática se puede suprimir mediante programación o deshabilitar completamente con el registro, incluso cuando un medio tiene un archivo Autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="8c71f-133">AutoRun can be suppressed programmatically or disabled entirely with the registry, even when a medium has an Autorun.inf file.</span></span> <span data-ttu-id="8c71f-134">Vea [habilitar y deshabilitar la ejecución automática](autoplay-reg.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8c71f-134">See [Enabling and Disabling AutoRun](autoplay-reg.md) for more information.</span></span>

 

 



