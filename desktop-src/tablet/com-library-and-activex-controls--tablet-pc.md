---
description: En esta sección se describe cómo configurar el entorno para usar las bibliotecas COM de la plataforma de Tablet PC en C++.
ms.assetid: c0d7f703-d4aa-4c26-ae81-a4c888383c1e
title: Biblioteca COM y controles ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9304880380ea95bc698c52d200931b77f64480
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705442"
---
# <a name="com-library-and-activex-controls"></a><span data-ttu-id="44fb0-103">Biblioteca COM y controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="44fb0-103">COM Library and ActiveX Controls</span></span>

<span data-ttu-id="44fb0-104">En esta sección se describe cómo configurar el entorno para usar las bibliotecas COM de la plataforma de Tablet PC en C++.</span><span class="sxs-lookup"><span data-stu-id="44fb0-104">This section describes how to set up your environment to use the Tablet PC platform COM libraries in C++.</span></span>

## <a name="microsoft-visual-c"></a><span data-ttu-id="44fb0-105">Microsoft Visual C++</span><span class="sxs-lookup"><span data-stu-id="44fb0-105">Microsoft Visual C++</span></span>

<span data-ttu-id="44fb0-106">Para compilar aplicaciones de Tablet PC en Visual C++, debe actualizar las variables de entorno del sistema, configurar las opciones de directorio de Visual Studio y tener acceso a las interfaces de Tablet PC en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="44fb0-106">To build Tablet PC applications in Visual C++, you need to update the system environment variables, set up directory options for Visual Studio, and access the Tablet PC interfaces in your project.</span></span>

<span data-ttu-id="44fb0-107">Para actualizar las variables de entorno, siga las instrucciones proporcionadas por el Windows SDK para agregar las variables de entorno a Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="44fb0-107">To update the environment variables, follow the instructions provided by the Windows SDK for adding the environment variables to Visual Studio.</span></span>

### <a name="accessing-the-tablet-pc-interfaces"></a><span data-ttu-id="44fb0-108">Acceso a las interfaces de Tablet PC</span><span class="sxs-lookup"><span data-stu-id="44fb0-108">Accessing the Tablet PC Interfaces</span></span>

<span data-ttu-id="44fb0-109">Para tener acceso a las interfaces de Tablet PC, debe incluir los archivos Msinkaut. h y Msinkaut \_ i. c en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="44fb0-109">To access the Tablet PC interfaces, you must include the Msinkaut.h and Msinkaut\_i.c files in your project.</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="44fb0-110">También puede utilizar la siguiente directiva de importación en lugar de las \# instrucciones include enumeradas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="44fb0-110">You can also use the following import directive instead of the \#include statements previously listed.</span></span>


```C++
#import "InkObj.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="44fb0-111">Para tener acceso a las interfaces de InkAnalysis, debe incluir los archivos IACom. h y IACom \_ i. c en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="44fb0-111">To access the InkAnalysis interfaces, you must include IACom.h and IACom\_i.c files in your project.</span></span>


```C++
#include <IACom.h>
#include <IACom_i.c>
```



<span data-ttu-id="44fb0-112">También puede utilizar la siguiente directiva de importación en lugar de las \# instrucciones include enumeradas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="44fb0-112">You can also use the following import directive instead of the \#include statements previously listed.</span></span>


```C++
#import "IACom.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="44fb0-113">Para tener acceso a las interfaces de [**InkDivider**](inkdivider-class.md) , debe incluir \_ los archivos msinkaut15 i. c y msinkaut15. h en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="44fb0-113">To access the [**InkDivider**](inkdivider-class.md) interfaces, you must include msinkaut15\_i.c and msinkaut15.h files in your project.</span></span>

> [!Note]  
> <span data-ttu-id="44fb0-114">InkDivider ha sido sustituido por las API de análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="44fb0-114">InkDivider has been superseded by the Ink Analysis APIs.</span></span>

 


```C++
#include <msinkaut15.h>
#include <msinkaut15_i.c>
```



<span data-ttu-id="44fb0-115">También puede utilizar la siguiente directiva de importación en lugar de las \# instrucciones include.</span><span class="sxs-lookup"><span data-stu-id="44fb0-115">You can also use the following import directive instead of the \# include statements.</span></span>


```C++
#import "InkDiv.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="44fb0-116">Para tener acceso a las interfaces de [**PenInputPanel**](peninputpanel-class.md) , debe incluir \_ los archivos PenInputPanel i. c y PenInputPanel. h en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="44fb0-116">To access the [**PenInputPanel**](peninputpanel-class.md) interfaces, you must include PenInputPanel\_i.c and PenInputPanel.h files in your project.</span></span>


```C++
#include <PenInputPanel.h>
#include <PenInputPanel_i.c>
```



<span data-ttu-id="44fb0-117">También puede utilizar la siguiente directiva de importación en lugar de las \# instrucciones include.</span><span class="sxs-lookup"><span data-stu-id="44fb0-117">You can also use the following import directive instead of the \# include statements.</span></span>


```C++
#import "PIPanel.dll" no_namespace 
```



> [!Note]  
> <span data-ttu-id="44fb0-118">Las API de PenInputPanel se han sustituido en Windows Vista por las nuevas interfaces del panel de entrada de texto.</span><span class="sxs-lookup"><span data-stu-id="44fb0-118">The PenInputPanel APIs have been superseded in Windows Vista by the new Text Input Panel interfaces.</span></span>

 

<span data-ttu-id="44fb0-119">Para tener acceso a las interfaces de control de [InkEdit](inkedit-control-reference.md) , debe incluir los archivos. h y. \_ c interactivos en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="44fb0-119">To access the [InkEdit](inkedit-control-reference.md) Control interfaces, you must include the Inked.h and Inked\_i.c files in your project.</span></span>


```C++
#include <inked.h>
#include <inked_i.c>
```



<span data-ttu-id="44fb0-120">Como alternativa, puede \# importar el archivo de InkEd.dll.</span><span class="sxs-lookup"><span data-stu-id="44fb0-120">Alternatively, you can \#import the InkEd.dll file.</span></span>


```C++
#import "InkEd.dll" no_namespace exclude("tagXFORM")
```



 

 



