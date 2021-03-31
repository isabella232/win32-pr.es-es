---
description: 'Hay cuatro niveles en la biblioteca de análisis de tinta: Windows Forms, WPF, COM y el nivel base. En esta sección se describe el uso de cada capa.'
ms.assetid: bd190606-5bd8-4280-ba2b-267588904ed3
title: Uso de la API de análisis de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e291066d6cfd6ecdec319728b7394d730ba311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000977"
---
# <a name="ink-analysis-api-usage"></a><span data-ttu-id="b2c7c-104">Uso de la API de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="b2c7c-104">Ink Analysis API Usage</span></span>

<span data-ttu-id="b2c7c-105">Hay cuatro niveles en la biblioteca de análisis de tinta: Windows Forms, WPF, COM y el nivel base.</span><span class="sxs-lookup"><span data-stu-id="b2c7c-105">There are four layers to the Ink Analysis library: Windows Forms, WPF, COM, and the base layer.</span></span> <span data-ttu-id="b2c7c-106">En esta sección se describe el uso de cada capa.</span><span class="sxs-lookup"><span data-stu-id="b2c7c-106">This section describes when to use each layer.</span></span>

## <a name="ink-analysis-api-overview"></a><span data-ttu-id="b2c7c-107">Introducción a Ink Analysis API</span><span class="sxs-lookup"><span data-stu-id="b2c7c-107">Ink Analysis API Overview</span></span>

<span data-ttu-id="b2c7c-108">Las bibliotecas de análisis de tinta están diseñadas para usarse en diversos entornos de programación admitidos.</span><span class="sxs-lookup"><span data-stu-id="b2c7c-108">The Ink Analysis libraries are designed to be used in a variety of supported programming environments.</span></span> <span data-ttu-id="b2c7c-109">Hay cuatro capas básicas a través de las que la aplicación puede hacer uso del análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="b2c7c-109">There are four basic layers through which your application can make use of Ink Analysis.</span></span> <span data-ttu-id="b2c7c-110">Estos niveles son:</span><span class="sxs-lookup"><span data-stu-id="b2c7c-110">These layers are:</span></span>

-   <span data-ttu-id="b2c7c-111">Capa de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b2c7c-111">The Windows Forms layer</span></span>
-   <span data-ttu-id="b2c7c-112">Nivel de WPF</span><span class="sxs-lookup"><span data-stu-id="b2c7c-112">The WPF layer</span></span>
-   <span data-ttu-id="b2c7c-113">El nivel COM</span><span class="sxs-lookup"><span data-stu-id="b2c7c-113">The COM layer</span></span>
-   <span data-ttu-id="b2c7c-114">Nivel base</span><span class="sxs-lookup"><span data-stu-id="b2c7c-114">The base layer</span></span>

### <a name="windows-forms-applications"></a><span data-ttu-id="b2c7c-115">Aplicaciones de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b2c7c-115">Windows Forms Applications</span></span>

<span data-ttu-id="b2c7c-116">Puede usar la API de análisis de tinta en el proyecto administrado agregando una referencia a las siguientes bibliotecas:</span><span class="sxs-lookup"><span data-stu-id="b2c7c-116">You can use the Ink Analysis API in your managed project by adding a reference to the following libraries:</span></span>

-   <span data-ttu-id="b2c7c-117">Microsoft. Ink. Analysis (Microsoft.Ink.Analysis.dll)</span><span class="sxs-lookup"><span data-stu-id="b2c7c-117">Microsoft.Ink.Analysis (Microsoft.Ink.Analysis.dll)</span></span>
-   <span data-ttu-id="b2c7c-118">Biblioteca de análisis de documentos de entrada manuscrita (IACore.dll)</span><span class="sxs-lookup"><span data-stu-id="b2c7c-118">Ink Document Analysis Library (IACore.dll)</span></span>

<span data-ttu-id="b2c7c-119">En Windows Forms aplicaciones, lo más probable es que use las bibliotecas junto con los objetos de la plataforma de Tablet PC estándar que se encuentran en el ensamblado Microsoft Tablet PC API v 1.7.</span><span class="sxs-lookup"><span data-stu-id="b2c7c-119">In Windows Forms applications, you will most likely use the libraries in conjunction with the standard Tablet PC platform objects found in the Microsoft Tablet PC API v1.7 assembly.</span></span> <span data-ttu-id="b2c7c-120">Asegúrese de que también tiene una referencia a:</span><span class="sxs-lookup"><span data-stu-id="b2c7c-120">Be sure you also have a reference to:</span></span>

-   <span data-ttu-id="b2c7c-121">Microsoft Tablet PC API v 1.7.2600.2180 (Microsoft.Ink.dll)</span><span class="sxs-lookup"><span data-stu-id="b2c7c-121">Microsoft Tablet PC API v1.7.2600.2180 (Microsoft.Ink.dll)</span></span>

### <a name="windows-presentation-framework-applications"></a><span data-ttu-id="b2c7c-122">Aplicaciones de Windows Presentation Framework</span><span class="sxs-lookup"><span data-stu-id="b2c7c-122">Windows Presentation Framework Applications</span></span>

<span data-ttu-id="b2c7c-123">Puede usar la API de análisis de tinta en el proyecto de WPF agregando una referencia a los miembros del análisis de tinta que se definen en el espacio de nombres System. Windows. Ink en el ensamblado de IAWinFX.dll.</span><span class="sxs-lookup"><span data-stu-id="b2c7c-123">You can use the Ink Analysis API in your WPF project by adding a reference to the Ink Analysis members that are defined in the System.Windows.Ink namespace in the IAWinFX.dll assembly.</span></span> <span data-ttu-id="b2c7c-124">Este ensamblado se instala mediante el SDK de.</span><span class="sxs-lookup"><span data-stu-id="b2c7c-124">This assembly is installed by the SDK.</span></span>

### <a name="com-applications"></a><span data-ttu-id="b2c7c-125">Aplicaciones COM</span><span class="sxs-lookup"><span data-stu-id="b2c7c-125">COM Applications</span></span>

<span data-ttu-id="b2c7c-126">Las aplicaciones COM que no son de automatización deben usar el nivel COM de las API de análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="b2c7c-126">Non-Automation COM applications should use the COM layer of the Ink Analysis APIs.</span></span>

<span data-ttu-id="b2c7c-127">Los objetos [ContextNode](/previous-versions/ms551996(v=vs.100)) específicos de tipo, como [ParagraphNode](/previous-versions/ms580136(v=vs.100)), [InkWordNode](/previous-versions/ms580133(v=vs.100))y others, no se usan en el nivel com.</span><span class="sxs-lookup"><span data-stu-id="b2c7c-127">Type specific [ContextNode](/previous-versions/ms551996(v=vs.100)) objects-such as [ParagraphNode](/previous-versions/ms580136(v=vs.100)), [InkWordNode](/previous-versions/ms580133(v=vs.100)), and others-are not used in the COM layer.</span></span> <span data-ttu-id="b2c7c-128">En su lugar, debe usar [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) en la interfaz [**IContextNode**](icontextnode.md) estándar.</span><span class="sxs-lookup"><span data-stu-id="b2c7c-128">Rather, you should use the [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) on the standard [**IContextNode**](icontextnode.md) interface.</span></span>

<span data-ttu-id="b2c7c-129">Debe \# incluir "IACom. h".</span><span class="sxs-lookup"><span data-stu-id="b2c7c-129">You must \#include "IACom.h".</span></span> <span data-ttu-id="b2c7c-130">Lo más probable es que use las bibliotecas junto con el objeto de tinta de la plataforma de Tablet PC, por lo que también debe \# incluir "msinkaut. h".</span><span class="sxs-lookup"><span data-stu-id="b2c7c-130">You will most likely use the libraries in conjunction wit the Tablet PC platform Ink object, so you should also \#include "msinkaut.h".</span></span>

### <a name="rts-and-other-applications"></a><span data-ttu-id="b2c7c-131">RTS y otras aplicaciones</span><span class="sxs-lookup"><span data-stu-id="b2c7c-131">RTS and Other Applications</span></span>

<span data-ttu-id="b2c7c-132">La capa de base de análisis de tinta funciona de forma diferente a la de los demás en cuanto a los datos de punto para el análisis en lugar de los objetos de [trazo](/previous-versions/ms552692(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="b2c7c-132">The Ink Analysis base layer works differently than the others in that it takes point data for analysis rather than [Stroke](/previous-versions/ms552692(v=vs.100)) objects.</span></span> <span data-ttu-id="b2c7c-133">Algunos ejemplos de dónde trabajaría con el nivel base directamente en lugar de utilizar los niveles de Windows Forms o COM son las aplicaciones que no usan objetos de tinta de la plataforma de Tablet PC de primera generación o las aplicaciones que usan las API de [**RealTimeStylus**](realtimestylus-class.md) para administrar la entrada del lápiz en lugar de usar los objetos de [tinta](/previous-versions/ms583670(v=vs.100)) de la plataforma de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="b2c7c-133">Examples of where you would work with the Base layer directly rather than using the Windows forms or COM layers include applications that do not use first generation Tablet PC Platform Ink objects, or applications that use the [**RealTimeStylus**](realtimestylus-class.md) APIs to manage stylus input rather than using the Tablet PC Platform [Ink](/previous-versions/ms583670(v=vs.100)) objects.</span></span>

## <a name="32-bit-support-only"></a><span data-ttu-id="b2c7c-134">Solo compatibilidad con 32 bits</span><span class="sxs-lookup"><span data-stu-id="b2c7c-134">32-bit Support Only</span></span>

<span data-ttu-id="b2c7c-135">Tenga en cuenta que las bibliotecas de análisis de tinta solo se admiten en procesos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b2c7c-135">Note that the Ink Analysis libraries are only supported in 32-bit processes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2c7c-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b2c7c-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2c7c-137">Información general de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="b2c7c-137">Ink Analysis Overview</span></span>](ink-analysis-overview.md)
</dt> <dt>

[<span data-ttu-id="b2c7c-138">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="b2c7c-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 
