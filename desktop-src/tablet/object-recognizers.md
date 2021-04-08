---
description: Además de reconocer texto, los reconocedores pueden reconocer una clase de objetos relacionados.
ms.assetid: 53b6137d-2998-4a3b-b469-3d1204ea194b
title: Reconocedores de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a258c8486bcf773f5f94c4de51c501e107fac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002501"
---
# <a name="object-recognizers"></a><span data-ttu-id="1a0d6-103">Reconocedores de objetos</span><span class="sxs-lookup"><span data-stu-id="1a0d6-103">Object Recognizers</span></span>

<span data-ttu-id="1a0d6-104">Además de reconocer texto, los reconocedores pueden reconocer una clase de objetos relacionados.</span><span class="sxs-lookup"><span data-stu-id="1a0d6-104">In addition to recognizing text, recognizers can recognize a class of related objects.</span></span> <span data-ttu-id="1a0d6-105">Los reconocedores de objetos reconocen las formas generales según su finalidad.</span><span class="sxs-lookup"><span data-stu-id="1a0d6-105">Object recognizers recognize general shapes, according to their purpose.</span></span> <span data-ttu-id="1a0d6-106">Los reconocedores de objetos se usan para reconocer:</span><span class="sxs-lookup"><span data-stu-id="1a0d6-106">Object recognizers are used to recognize:</span></span>

-   <span data-ttu-id="1a0d6-107">Notas musicales</span><span class="sxs-lookup"><span data-stu-id="1a0d6-107">Musical notes</span></span>
-   <span data-ttu-id="1a0d6-108">Formas geométricas</span><span class="sxs-lookup"><span data-stu-id="1a0d6-108">Geometric shapes</span></span>
-   <span data-ttu-id="1a0d6-109">Ecuaciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="1a0d6-109">Math equations</span></span>
-   <span data-ttu-id="1a0d6-110">Elementos de diagrama de flujo</span><span class="sxs-lookup"><span data-stu-id="1a0d6-110">Flow chart elements</span></span>

<span data-ttu-id="1a0d6-111">Normalmente, los objetos que reconoce este tipo de reconocedor están en una relación funcional o espacial bidimensional entre sí.</span><span class="sxs-lookup"><span data-stu-id="1a0d6-111">Usually, the objects that are recognized by such a recognizer are in a two-dimensional spatial or functional relationship with each other.</span></span> <span data-ttu-id="1a0d6-112">Por ejemplo, dentro de las relaciones complejas de una ecuación matemática, un reconocedor puede devolver resultados diferentes para un límite superior en un entero definito en lugar de un numerador de una fracción.</span><span class="sxs-lookup"><span data-stu-id="1a0d6-112">For example, within the complex relationships in a math equation, a recognizer can return different results for an upper limit on a definite integral as opposed to a numerator in a fraction.</span></span>

<span data-ttu-id="1a0d6-113">Debido a la naturaleza muy general de estas relaciones, es sumamente difícil definir el conjunto de interfaces que funcionarán para cada reconocedor de objetos.</span><span class="sxs-lookup"><span data-stu-id="1a0d6-113">Because of the very general nature of these relationships, it is extremely difficult to define the set of interfaces that will work for every object recognizer.</span></span>

<span data-ttu-id="1a0d6-114">La tecnología de Tablet PC proporciona un marco de trabajo básico para los reconocedores de objetos en la biblioteca administrada y las interfaces de automatización.</span><span class="sxs-lookup"><span data-stu-id="1a0d6-114">The Tablet PC Technology provides a basic framework for object recognizers in the Managed Library and Automation interfaces.</span></span> <span data-ttu-id="1a0d6-115">Sin embargo, debe desarrollar interfaces personalizadas que describan relaciones espaciales complejas entre objetos reconocidos para cada reconocedor de objetos.</span><span class="sxs-lookup"><span data-stu-id="1a0d6-115">However, you must develop custom interfaces that describe complex spatial relationships between recognized objects for each object recognizer.</span></span> <span data-ttu-id="1a0d6-116">En concreto, para los reconocedores de objetos, la plataforma proporciona el objeto [**RecognizerContext**](inkrecognizercontext-class.md) básico para asociar el objeto de [**entrada manuscrita**](inkdisp-class.md) con el contexto del reconocedor y para llamar al reconocedor para realizar el reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="1a0d6-116">Specifically, for object recognizers, the platform provides the basic [**RecognizerContext**](inkrecognizercontext-class.md) object for associating the [**Ink**](inkdisp-class.md) object with the recognizer context and for calling the recognizer to perform the recognition.</span></span>

 

 



