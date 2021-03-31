---
title: Herramienta de Command-Line de JavaTLB
description: Herramienta de Command-Line de JavaTLB
ms.assetid: b46d7bcc-ccd9-4242-9b19-f398d2cb8f91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a0214648f7ad86613d6b35e3084021e2be24aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779963"
---
# <a name="javatlb-command-line-tool"></a><span data-ttu-id="d8b00-103">Herramienta de Command-Line de JavaTLB</span><span class="sxs-lookup"><span data-stu-id="d8b00-103">JavaTLB Command-Line Tool</span></span>

<span data-ttu-id="d8b00-104">JavaTLB es un componente de Visual J++ 5,0.</span><span class="sxs-lookup"><span data-stu-id="d8b00-104">JavaTLB is a component of Visual J++ 5.0.</span></span> <span data-ttu-id="d8b00-105">JavaTLB es una aplicación de línea de comandos que genera archivos de clase para un objeto COM.</span><span class="sxs-lookup"><span data-stu-id="d8b00-105">JavaTLB is a command-line application that generates class files for a COM object.</span></span> <span data-ttu-id="d8b00-106">Los métodos que contienen tipos de datos que no se pueden representar con precisión y de forma segura en Java no se convierten.</span><span class="sxs-lookup"><span data-stu-id="d8b00-106">Methods that contain data types that cannot be accurately and safely represented in Java are not converted.</span></span>

<span data-ttu-id="d8b00-107">A diferencia del [Asistente para la biblioteca de tipos de Java](java-type-library-wizard.md), JavaTLB no genera un archivo de resumen que contiene la información de la biblioteca de tipos de Java.</span><span class="sxs-lookup"><span data-stu-id="d8b00-107">Unlike the [Java Type Library Wizard](java-type-library-wizard.md), JavaTLB does not generate a summary file containing the Java type library information.</span></span>

<span data-ttu-id="d8b00-108">Para generar archivos de clase de Java para un único objeto COM, en el símbolo del sistema, ejecute:</span><span class="sxs-lookup"><span data-stu-id="d8b00-108">To generate Java class files for a single COM object, from the command prompt run:</span></span>

<span data-ttu-id="d8b00-109"> *nombre de archivo* JavaTLB</span><span class="sxs-lookup"><span data-stu-id="d8b00-109">**javatlb** *filename*</span></span>

<span data-ttu-id="d8b00-110">donde *filename* es el nombre del archivo que contiene la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="d8b00-110">where *filename* is the name of the file that contains the type library.</span></span> <span data-ttu-id="d8b00-111">Este archivo puede tener cualquiera de las siguientes extensiones de nombre de archivo:. tlb,. olb,. ocx,. dll o. exe.</span><span class="sxs-lookup"><span data-stu-id="d8b00-111">This file may have any of the following file name extensions: .tlb, .olb, .ocx, .dll, or .exe.</span></span>

<span data-ttu-id="d8b00-112">Para generar archivos de clase de Java para varios objetos COM, en el símbolo del sistema, ejecute:</span><span class="sxs-lookup"><span data-stu-id="d8b00-112">To generate Java class files for multiple COM objects, from the command prompt run:</span></span>

<span data-ttu-id="d8b00-113">\**JavaTLB @ \* \* \* TextFile*</span><span class="sxs-lookup"><span data-stu-id="d8b00-113">\**javatlb @\*\*\*TextFile*</span></span>

<span data-ttu-id="d8b00-114">donde *TextFile* es el nombre de un archivo de texto que contiene una lista de los archivos que contienen las bibliotecas de tipos del objeto com.</span><span class="sxs-lookup"><span data-stu-id="d8b00-114">where *TextFile* is the name of a text file that contains a list of the files containing the COM object's type libraries.</span></span>

> [!Note]  
> <span data-ttu-id="d8b00-115">En Visual J++ 6,0, la herramienta de línea de comandos JavaTLB se reemplaza por la [herramienta JActiveX](jactivex-command-line-tool.md).</span><span class="sxs-lookup"><span data-stu-id="d8b00-115">In Visual J++ 6.0, the JavaTLB command-line tool is replaced by the [JActiveX tool](jactivex-command-line-tool.md).</span></span> <span data-ttu-id="d8b00-116">Para obtener más información, vea la documentación de Visual J++ 6,0.</span><span class="sxs-lookup"><span data-stu-id="d8b00-116">For more information, see the Visual J++ 6.0 documentation.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d8b00-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d8b00-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8b00-118">Traducir a Java</span><span class="sxs-lookup"><span data-stu-id="d8b00-118">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




