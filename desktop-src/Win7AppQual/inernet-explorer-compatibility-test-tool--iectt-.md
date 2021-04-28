---
description: Herramienta de prueba de compatibilidad de Internet Explorer (IECTT)
ms.assetid: 11169540-555A-48A9-A4CD-535D5765C005
title: Herramienta de prueba de compatibilidad de Internet Explorer (IECTT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a35b3120e95c668f2808c9c525d0c1d4f89f8f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088293"
---
# <a name="internet-explorer-compatibility-test-tool-iectt"></a><span data-ttu-id="f4aa8-103">Herramienta de prueba de compatibilidad de Internet Explorer (IECTT)</span><span class="sxs-lookup"><span data-stu-id="f4aa8-103">Internet Explorer Compatibility Test Tool (IECTT)</span></span>

<span data-ttu-id="f4aa8-104">La Internet Explorer de prueba de compatibilidad de aplicaciones (IECTT) es un componente del kit [de herramientas de compatibilidad de aplicaciones de Microsoft](/windows-hardware/get-started/adk-install).</span><span class="sxs-lookup"><span data-stu-id="f4aa8-104">The Internet Explorer Compatibility Test Tool (IECTT) is a component of the [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).</span></span> <span data-ttu-id="f4aa8-105">Esta herramienta puede ayudarle a diagnosticar problemas en las aplicaciones web mostrando problemas en tiempo real y, opcionalmente, cargando los resultados en una base de datos act.</span><span class="sxs-lookup"><span data-stu-id="f4aa8-105">This tool can help you diagnose issues in your web applications by displaying issues in real time and optionally uploading the results to an ACT database.</span></span> <span data-ttu-id="f4aa8-106">Los resultados incluyen detalles sobre posibles problemas de compatibilidad y vínculos para obtener más información sobre cada problema de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="f4aa8-106">The results include details about possible compatibility issues and links for more information about each compatibility issue.</span></span> <span data-ttu-id="f4aa8-107">IECTT también permite excluir problemas y modificar los atributos disponibles.</span><span class="sxs-lookup"><span data-stu-id="f4aa8-107">IECTT also enables you to exclude issues and modify available attributes.</span></span>

## <a name="to-open-iectt"></a><span data-ttu-id="f4aa8-108">Para abrir IECTT</span><span class="sxs-lookup"><span data-stu-id="f4aa8-108">To open IECTT</span></span>

1.  <span data-ttu-id="f4aa8-109">Instale el kit [de herramientas de compatibilidad de aplicaciones de Microsoft](/windows-hardware/get-started/adk-install).</span><span class="sxs-lookup"><span data-stu-id="f4aa8-109">Install the [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).</span></span>
2.  <span data-ttu-id="f4aa8-110">Haga clic **en** Inicio , seleccione **Programas,** Microsoft Application Compatibility **Toolkit 5.6,** Herramientas de desarrollador y evaluador **y,** a continuación, haga clic Internet Explorer Herramienta de prueba **de** compatibilidad .</span><span class="sxs-lookup"><span data-stu-id="f4aa8-110">Click **Start**, point to **Programs**, point to **Microsoft Application Compatibility Toolkit 5.6**, point to **Developer and Tester Tools**, and then click **Internet Explorer Compatibility Test Tool**.</span></span>

<span data-ttu-id="f4aa8-111">En las secciones siguientes se describen escenarios comunes de IECTT.</span><span class="sxs-lookup"><span data-stu-id="f4aa8-111">The following sections describe common IECTT scenarios.</span></span>

## <a name="view-issues-in-real-time"></a><span data-ttu-id="f4aa8-112">Ver problemas en tiempo real</span><span class="sxs-lookup"><span data-stu-id="f4aa8-112">View Issues in Real Time</span></span>

<span data-ttu-id="f4aa8-113">Puede buscar y ver los problemas basados en web en tiempo real, mientras prueba sus sitios web y aplicaciones web en Windows Internet Explorer 7 y Windows Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="f4aa8-113">You can locate and view your web-based issues in real time, while you are testing your websites and web applications against Windows Internet Explorer 7 and Windows Internet Explorer 8.</span></span> <span data-ttu-id="f4aa8-114">Después de completar las pruebas, puede ver los resultados en la pantalla **Datos en directo** de IECTT.</span><span class="sxs-lookup"><span data-stu-id="f4aa8-114">After you complete your testing, you can view your results in the **Live Data** screen of the IECTT.</span></span>

## <a name="upload-issues-to-your-act-database"></a><span data-ttu-id="f4aa8-115">Carga de problemas en la base de datos de ACT</span><span class="sxs-lookup"><span data-stu-id="f4aa8-115">Upload Issues to Your ACT Database</span></span>

<span data-ttu-id="f4aa8-116">Puede cargar los problemas basados en web en la base de datos ACT, que procesa la información y le permite ver los resultados en la pantalla Analizar del Administrador de compatibilidad de aplicaciones. </span><span class="sxs-lookup"><span data-stu-id="f4aa8-116">You can upload your web-based issues to the ACT database, which processes the information and enables you to view your results on the **Analyze** screen of the Application Compatibility Manager.</span></span>

## <a name="collect-your-compatibility-data"></a><span data-ttu-id="f4aa8-117">Recopilación de los datos de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="f4aa8-117">Collect Your Compatibility Data</span></span>

<span data-ttu-id="f4aa8-118">Puede recopilar datos de compatibilidad relacionados con el sitio web y la aplicación web mediante la herramienta IECTT con Internet Explorer 7 o Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="f4aa8-118">You can collect your website and web application-related compatibility data by using the IECTT tool with either Internet Explorer 7 or Internet Explorer 7.</span></span>

<span data-ttu-id="f4aa8-119">**Para recopilar los datos de compatibilidad**</span><span class="sxs-lookup"><span data-stu-id="f4aa8-119">**To collect your compatibility data**</span></span>

1.  <span data-ttu-id="f4aa8-120">Cierre todas las ventanas de Windows Internet Explorer activas.</span><span class="sxs-lookup"><span data-stu-id="f4aa8-120">Close all of your active Windows Internet Explorer windows.</span></span>
2.  <span data-ttu-id="f4aa8-121">En IECTT, en la barra de herramientas **de la Internet Explorer de pruebas de compatibilidad,** haga clic en **Habilitar**.</span><span class="sxs-lookup"><span data-stu-id="f4aa8-121">In IECTT, on the **Internet Explorer Compatibility Test Tool** toolbar, click **Enable**.</span></span>
3.  <span data-ttu-id="f4aa8-122">Abra una Internet Explorer 7 o Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="f4aa8-122">Open an Internet Explorer 7 or Internet Explorer 8 window.</span></span>

    <span data-ttu-id="f4aa8-123">Aparece un mensaje que indica que el registro de evaluación de compatibilidad está activado.</span><span class="sxs-lookup"><span data-stu-id="f4aa8-123">A message appears and states that compatibility evaluation logging is turned on.</span></span>

4.  <span data-ttu-id="f4aa8-124">Visite los sitios web o las aplicaciones web que su organización necesita para su uso.</span><span class="sxs-lookup"><span data-stu-id="f4aa8-124">Visit the websites or web applications that are required for use by your organization.</span></span> <span data-ttu-id="f4aa8-125">A medida que visita cada sitio, la herramienta IECTT muestra, en tiempo real, los posibles problemas de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="f4aa8-125">As you visit each site, the IECTT tool displays, in real-time, your potential compatibility issues.</span></span>
5.  <span data-ttu-id="f4aa8-126">En la barra **Internet Explorer herramientas de pruebas de** compatibilidad, haga clic **en** Deshabilitar cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="f4aa8-126">On the **Internet Explorer Compatibility Test Tool** toolbar, click **Disable** when you are done.</span></span>

    <span data-ttu-id="f4aa8-127">El proceso de registro de compatibilidad finaliza y se detiene.</span><span class="sxs-lookup"><span data-stu-id="f4aa8-127">The compatibility logging process finishes and stops.</span></span>

## <a name="filter-your-issue-results"></a><span data-ttu-id="f4aa8-128">Filtrar los resultados del problema</span><span class="sxs-lookup"><span data-stu-id="f4aa8-128">Filter Your Issue Results</span></span>

<span data-ttu-id="f4aa8-129">Puede filtrar cualquiera de los resultados de IECTT por nombre de objeto, por tipo de problema o por ambos.</span><span class="sxs-lookup"><span data-stu-id="f4aa8-129">You can filter any of your IECTT results by object name, by issue type, or by both.</span></span>

<span data-ttu-id="f4aa8-130">**Para filtrar los resultados del problema**</span><span class="sxs-lookup"><span data-stu-id="f4aa8-130">**To filter your issue results**</span></span>

1.  <span data-ttu-id="f4aa8-131">En la pantalla **Internet Explorer de prueba de compatibilidad,** haga clic en **Filtrar.**</span><span class="sxs-lookup"><span data-stu-id="f4aa8-131">On the **Internet Explorer Compatibility Test Tool** screen, click **Filter**.</span></span>

    <span data-ttu-id="f4aa8-132">Aparece **el cuadro de diálogo** Filtro de problemas.</span><span class="sxs-lookup"><span data-stu-id="f4aa8-132">The **Issues Filter** dialog box appears.</span></span>

2.  <span data-ttu-id="f4aa8-133">Escriba el nombre del objeto que desea ver en el cuadro Escriba el nombre del objeto para **ver los problemas.**</span><span class="sxs-lookup"><span data-stu-id="f4aa8-133">Enter the name of the object that you intend to view in the **Enter the name of the object to view issues for** box.</span></span>

<span data-ttu-id="f4aa8-134">Para obtener más información sobre esta herramienta y otras herramientas de desarrolladores, vea [¿Qué](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) es la herramienta de prueba de compatibilidad de Internet Explorer? en MSDN Library y la entrada de blog Registro de compatibilidad de aplicaciones en [IE8.](/archive/blogs/ie/application-compatibility-logging-in-ie8)</span><span class="sxs-lookup"><span data-stu-id="f4aa8-134">For more information about this tool and other developers tools, see [What is the Internet Explorer Compatibility Test Tool?](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) in the MSDN Library and the [Application Compatibility Logging in IE8](/archive/blogs/ie/application-compatibility-logging-in-ie8) blog post.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4aa8-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f4aa8-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4aa8-136">Herramientas para depurar aplicaciones web y complementos</span><span class="sxs-lookup"><span data-stu-id="f4aa8-136">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 
