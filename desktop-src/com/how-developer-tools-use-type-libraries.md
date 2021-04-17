---
title: Cómo usan las herramientas de desarrolladores las bibliotecas de tipos
description: Cómo usan las herramientas de desarrolladores las bibliotecas de tipos
ms.assetid: 260aa694-1055-4a43-93aa-69a9d7359881
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0cc0f5249075aa861a1301466f86a0f769b8bf3
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "105717321"
---
# <a name="how-developer-tools-use-type-libraries"></a><span data-ttu-id="9ac8f-103">Cómo usan las herramientas de desarrolladores las bibliotecas de tipos</span><span class="sxs-lookup"><span data-stu-id="9ac8f-103">How Developer Tools Use Type Libraries</span></span>

<span data-ttu-id="9ac8f-104">En el diagrama siguiente se muestra cómo interactúan las diversas herramientas de desarrollo con la biblioteca de tipos de un objeto COM.</span><span class="sxs-lookup"><span data-stu-id="9ac8f-104">The following diagram illustrates how the various development tools interact with a COM object's type library.</span></span> <span data-ttu-id="9ac8f-105">Cada biblioteca de tipos expone interfaces de programación estándar que las herramientas pueden llamar para obtener información sobre los elementos descritos en esa biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="9ac8f-105">Each type library exposes standard programmatic interfaces that tools can call to get information about the elements described in that type library.</span></span> <span data-ttu-id="9ac8f-106">En este diagrama, GUID representa el identificador único global y la RPC para la llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="9ac8f-106">In this diagram, GUID stands for globally unique identifier and RPC for remote procedure call.</span></span>

![Diagrama que muestra cómo las herramientas de desarrollo interactúan con la biblioteca de tipos de un objeto de C O M.](images/09983c96-3f01-4ad5-8d3e-12b8ed28c35d.png)

<span data-ttu-id="9ac8f-108">En el diagrama anterior, las herramientas de conversión de C++, como el compilador MIDL y los asistentes proporcionados por el sistema de desarrollo de Microsoft Visual C++, generan archivos de encabezado y de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="9ac8f-108">In the preceding diagram, the C++ conversion tools, such as the MIDL compiler and the wizards provided by the Microsoft Visual C++ development system, generate header and stub files.</span></span> <span data-ttu-id="9ac8f-109">Puede agregar estos archivos al proyecto para usar el objeto COM descrito por la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="9ac8f-109">You can add these files to your project in order to use the COM object described by the type library.</span></span>

<span data-ttu-id="9ac8f-110">Del mismo modo, en Java las herramientas de desarrollo generan archivos de código fuente y de clase Java, que luego puede importar en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9ac8f-110">Similarly, in Java the developer tools generate Java class and source files, which you can then import into your application.</span></span>

<span data-ttu-id="9ac8f-111">En Visual Basic, el escenario es algo más sencillo.</span><span class="sxs-lookup"><span data-stu-id="9ac8f-111">In Visual Basic, the scenario is somewhat simpler.</span></span> <span data-ttu-id="9ac8f-112">No es necesario generar archivos adicionales.</span><span class="sxs-lookup"><span data-stu-id="9ac8f-112">You do not need to generate additional files.</span></span> <span data-ttu-id="9ac8f-113">El entorno de Visual Basic proporciona cuadros de diálogo que enumeran los objetos COM actualmente instalados en el equipo.</span><span class="sxs-lookup"><span data-stu-id="9ac8f-113">The Visual Basic environment provides dialog boxes listing the COM objects currently installed on your computer.</span></span> <span data-ttu-id="9ac8f-114">Seleccione el componente al que desea llamar desde la aplicación y se agrega al proyecto, ya sea como un componente o como una referencia.</span><span class="sxs-lookup"><span data-stu-id="9ac8f-114">You select the component you want to call from your application, and it is added to your project, either as a component or a reference.</span></span>

<span data-ttu-id="9ac8f-115">El visor OLE-COM Lee una biblioteca de tipos, genera un archivo IDL temporal basado en la biblioteca de tipos y lo muestra a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="9ac8f-115">The OLE-COM viewer reads a type library, generates a temporary IDL file based on the type library, and displays it to users.</span></span> <span data-ttu-id="9ac8f-116">El visor OLE-COM también muestra la sintaxis de C++ para los elementos COM enumerados en la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="9ac8f-116">The OLE-COM viewer also displays the C++ syntax for the COM elements listed in the type library.</span></span>

<span data-ttu-id="9ac8f-117">Para obtener más información sobre las bibliotecas de tipos, vea [bibliotecas de tipos y lenguaje de descripción de objetos](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).</span><span class="sxs-lookup"><span data-stu-id="9ac8f-117">For more information about type libraries, see [Type Libraries and the Object Description Language](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).</span></span>

 

 