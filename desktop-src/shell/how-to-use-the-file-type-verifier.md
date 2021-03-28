---
description: En este tema se describe cómo usar el comprobador de tipo de archivo que se proporciona en el SDK de Windows 7.
ms.assetid: 96FCA74B-DEB2-49D1-B670-EBD8BE0783F1
title: Cómo usar el comprobador de tipo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f083897499f972f945867a0c02318df192e734d9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "104279697"
---
# <a name="how-to-use-the-file-type-verifier"></a><span data-ttu-id="f35f7-103">Cómo usar el comprobador de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="f35f7-103">How to Use the File Type Verifier</span></span>

<span data-ttu-id="f35f7-104">En este tema se describe cómo usar el comprobador de tipo de archivo que se proporciona en el [SDK de Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f35f7-104">This topic describes how to use the File Type Verifier that is provided in the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f35f7-105">Si el programa crea tipos de archivos con los que se espera que los usuarios interactúen desde el shell de Windows (normalmente almacenado en la carpeta conocida de un usuario, como **Mis documentos**), es muy importante probar la aplicación y comprobar que los archivos que crea están correctamente registrados y proporcionar una experiencia de usuario de alta calidad al examinar y buscar archivos.</span><span class="sxs-lookup"><span data-stu-id="f35f7-105">If your program creates file types that users are expected to interact with from the Windows Shell (typically stored in a user's known folder such as **My Documents**), it is very important to test your application and verify that the files it creates are properly registered and provide a high-quality user experience when browsing and searching files.</span></span> <span data-ttu-id="f35f7-106">Esto es especialmente importante si espera que los usuarios ejecuten sus aplicaciones en Windows 7, que se basa en controladores de tipo de archivo de alta calidad para muchas de las características de Shell.</span><span class="sxs-lookup"><span data-stu-id="f35f7-106">This is especially important if you expect users to run your applications on Windows 7, which relies on high-quality file type handlers for many of the Shell features.</span></span>

<span data-ttu-id="f35f7-107">Para comprobar el tipo de archivo mediante el comprobador de tipo de archivo, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="f35f7-107">To verify your file type using the File Type Verifier, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="f35f7-108">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="f35f7-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="f35f7-109">Paso 1:</span><span class="sxs-lookup"><span data-stu-id="f35f7-109">Step 1:</span></span>

<span data-ttu-id="f35f7-110">Instale la aplicación en el entorno de prueba y copie el comprobador de tipo de archivo en ese entorno.</span><span class="sxs-lookup"><span data-stu-id="f35f7-110">Install the application on your test environment, and copy the File Type Verifier to that environment.</span></span> <span data-ttu-id="f35f7-111">El comprobador de tipo de archivo está disponible en el [SDK de Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f35f7-111">The File Type Verifier is available in the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

### <a name="step-2"></a><span data-ttu-id="f35f7-112">Paso 2:</span><span class="sxs-lookup"><span data-stu-id="f35f7-112">Step 2:</span></span>

<span data-ttu-id="f35f7-113">Use la aplicación para crear un archivo que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="f35f7-113">Use your application to create a file to be tested.</span></span>

### <a name="step-3"></a><span data-ttu-id="f35f7-114">Paso 3:</span><span class="sxs-lookup"><span data-stu-id="f35f7-114">Step 3:</span></span>

<span data-ttu-id="f35f7-115">Inicie el comprobador de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="f35f7-115">Start the File Type Verifier.</span></span>

### <a name="step-4"></a><span data-ttu-id="f35f7-116">Paso 4:</span><span class="sxs-lookup"><span data-stu-id="f35f7-116">Step 4:</span></span>

<span data-ttu-id="f35f7-117">Seleccione la categoría del tipo de archivo, tal y como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="f35f7-117">Select the category for your file type, as shown in the following screen shot.</span></span>

![Captura de pantalla que muestra la función de arrastrar y colocar.](images/file-assoc/filetypeverifier1.png)

<span data-ttu-id="f35f7-119">La selección de categoría determina el conjunto de pruebas que ejecutará la herramienta.</span><span class="sxs-lookup"><span data-stu-id="f35f7-119">The category selection determines the set of tests that will be run by the tool.</span></span> <span data-ttu-id="f35f7-120">Si el tipo puede estar por debajo de más de una categoría (por ejemplo, un archivo TIF puede ser una imagen o un documento en función del contenido), vuelva a ejecutar la herramienta con cada categoría adecuada.</span><span class="sxs-lookup"><span data-stu-id="f35f7-120">If your type could fall under more than one category (for example, a TIF file might be a Picture or a Document depending on the content), run the tool again with each appropriate category.</span></span>

### <a name="step-5"></a><span data-ttu-id="f35f7-121">Paso 5:</span><span class="sxs-lookup"><span data-stu-id="f35f7-121">Step 5:</span></span>

<span data-ttu-id="f35f7-122">Con el explorador de Windows, busque un archivo que se va a probar y use el mouse para arrastrarlo al destino en el comprobador de tipo de archivo, como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="f35f7-122">Using Windows Explorer, locate a file to be tested and use the mouse to drag it to the target in File Type Verifier, as shown in the following screen shot.</span></span>

![captura de pantalla que muestra la función de arrastrar y colocar](images/file-assoc/filetypeverifier2.png)

### <a name="step-6"></a><span data-ttu-id="f35f7-124">Paso 6:</span><span class="sxs-lookup"><span data-stu-id="f35f7-124">Step 6:</span></span>

<span data-ttu-id="f35f7-125">Espere a que la herramienta Comprobador de tipo de archivo continúe a través de una serie de pruebas.</span><span class="sxs-lookup"><span data-stu-id="f35f7-125">Wait for the File Type Verifier tool to proceed through a series of tests.</span></span> <span data-ttu-id="f35f7-126">La barra de progreso muestra el progreso de las pruebas, como en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="f35f7-126">The progress of the testing is shown by the progress bar, as in the following screen shot.</span></span>

![captura de pantalla que muestra la barra de progreso](images/file-assoc/filetypeverifier3.png)

### <a name="step-7"></a><span data-ttu-id="f35f7-128">Paso 7:</span><span class="sxs-lookup"><span data-stu-id="f35f7-128">Step 7:</span></span>

<span data-ttu-id="f35f7-129">Revise el Resumen de resultados de las pruebas de tipo de archivo de documento, tal y como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="f35f7-129">Review the results summary of your Document file type tests, as shown in the following screen shot.</span></span>

![captura de pantalla que muestra el Resumen de resultados](images/file-assoc/filetypeverifier4.png)

### <a name="step-8"></a><span data-ttu-id="f35f7-131">Paso 8:</span><span class="sxs-lookup"><span data-stu-id="f35f7-131">Step 8:</span></span>

<span data-ttu-id="f35f7-132">Haga clic en cualquiera de los resultados de la página Resumen para ver el registro detallado.</span><span class="sxs-lookup"><span data-stu-id="f35f7-132">Click any of the results on the summary page to view the detailed log.</span></span> <span data-ttu-id="f35f7-133">En la captura de pantalla siguiente se muestra un registro de ejemplo para un controlador de vista previa.</span><span class="sxs-lookup"><span data-stu-id="f35f7-133">An example log for a preview handler is shown in the following screen shot.</span></span>

![captura de pantalla que muestra el registro del controlador de vista previa](images/file-assoc/filetypeverifier5.png)

### <a name="step-9"></a><span data-ttu-id="f35f7-135">Paso 9:</span><span class="sxs-lookup"><span data-stu-id="f35f7-135">Step 9:</span></span>

<span data-ttu-id="f35f7-136">Para guardar una copia del archivo de registro, haga clic en **Guardar archivo de registro** en la parte inferior de la pantalla del registro y elija una ubicación adecuada para almacenarlo en el equipo.</span><span class="sxs-lookup"><span data-stu-id="f35f7-136">To save a copy of the log file, click **Save Log File** at the bottom of the log display and choose an appropriate location for storing it on your computer.</span></span>

### <a name="step-10"></a><span data-ttu-id="f35f7-137">Paso 10:</span><span class="sxs-lookup"><span data-stu-id="f35f7-137">Step 10:</span></span>

<span data-ttu-id="f35f7-138">Si se detectan errores, realice los cambios apropiados en la aplicación y vuelva a ejecutar la herramienta para comprobar que los errores ya no se muestran en las pruebas.</span><span class="sxs-lookup"><span data-stu-id="f35f7-138">If failures are reported, make the appropriate changes in your application and run the tool again to verify that the failures are no longer showing up in the tests.</span></span> <span data-ttu-id="f35f7-139">Si se registran las advertencias, evalúelos y decida si son relevantes para su tipo de archivo concreto y realice los cambios apropiados en la aplicación según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="f35f7-139">If warnings are reported, evaluate them and decide whether they are relevant for your particular file type and make the appropriate changes to your application as necessary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f35f7-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f35f7-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f35f7-141">SDK de Windows 7</span><span class="sxs-lookup"><span data-stu-id="f35f7-141">Windows 7 SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
</dt> </dl>

 

 



