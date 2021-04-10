---
title: Variables para almacenar propiedades
description: Variables para almacenar propiedades
ms.assetid: a90a6e21-00fb-46f8-96c8-654d8f205905
keywords:
- Complementos de Media Player de Windows, propiedades de ejemplo de eco
- complementos, propiedades de ejemplo de eco
- Complementos de procesamiento de señal digital, eco de propiedades de ejemplo
- Complementos DSP, propiedades de ejemplo de eco
- Ejemplo de complemento DSP de eco, propiedades
- Ejemplo de complemento DSP de eco, variables para almacenar propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d252962116ba9c72464273f9c4ea1688b151898
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268940"
---
# <a name="variables-to-store-properties"></a><span data-ttu-id="cce82-109">Variables para almacenar propiedades</span><span class="sxs-lookup"><span data-stu-id="cce82-109">Variables to Store Properties</span></span>

<span data-ttu-id="cce82-110">En primer lugar, necesitará una variable para almacenar el tiempo de retraso.</span><span class="sxs-lookup"><span data-stu-id="cce82-110">First, you will need a variable to store the delay time.</span></span> <span data-ttu-id="cce82-111">El ejemplo predeterminado creado por el Asistente para complementos de Windows Media Player proporciona una variable denominada m \_ fScaleFactor para almacenar el multiplicador de escalado que utiliza para el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="cce82-111">The default sample created by the Windows Media Player Plug-in Wizard provides a variable named m\_fScaleFactor to store the scaling multiplier it uses for processing.</span></span> <span data-ttu-id="cce82-112">Este ejemplo ya no necesita esta variable, por lo que puede cambiar su nombre y tipo para almacenar el valor de tiempo de retraso.</span><span class="sxs-lookup"><span data-stu-id="cce82-112">This sample no longer needs this variable, so you can change its name and type to store the delay time value.</span></span>

1.  <span data-ttu-id="cce82-113">Reemplace cada instancia de m \_ fScaleFactor en echo. h y ECHO. cpp por m \_ dwDelayTime.</span><span class="sxs-lookup"><span data-stu-id="cce82-113">Replace each instance of m\_fScaleFactor in Echo.h and Echo.cpp with m\_dwDelayTime.</span></span>
2.  <span data-ttu-id="cce82-114">Cambie el tipo de datos de m \_ fScaleFactor (Now \_ dwDelayTime) de Double a DWORD en echo. h.</span><span class="sxs-lookup"><span data-stu-id="cce82-114">Change the data type for m\_fScaleFactor (now m\_dwDelayTime) from double to DWORD in Echo.h.</span></span>
3.  <span data-ttu-id="cce82-115">En el constructor de CEcho, cambie el valor de tiempo de retraso predeterminado a 1000.</span><span class="sxs-lookup"><span data-stu-id="cce82-115">In the constructor for CEcho, change the default delay time value to 1000.</span></span>
    ```C++
    m_dwDelayTime = 1000;   // Default to a delay time of 1000 ms.
    
    ```

    

<span data-ttu-id="cce82-116">A continuación, declare dos nuevas variables de miembro para almacenar el porcentaje de la señal del efecto y el porcentaje de la señal de origen que se va a mezclar en el búfer de salida final.</span><span class="sxs-lookup"><span data-stu-id="cce82-116">Next, declare two new member variables to store the percentage of effect signal and the percentage of source signal to be mixed in the final output buffer.</span></span> <span data-ttu-id="cce82-117">El término "húmedo" hace referencia al efecto y el término "seco" hace referencia a la señal de origen.</span><span class="sxs-lookup"><span data-stu-id="cce82-117">The term "wet" refers to the effect, and the term "dry" refers to the source signal.</span></span> <span data-ttu-id="cce82-118">Agregue las declaraciones siguientes a ECHO. h:</span><span class="sxs-lookup"><span data-stu-id="cce82-118">Add the following declarations to Echo.h:</span></span>


```C++
double  m_fWetMix;    // percentage of effect
double  m_fDryMix;    // percentage of dry signal

```



<span data-ttu-id="cce82-119">Estos valores se almacenan como representaciones decimales de porcentajes, por lo que se pueden usar fácilmente como factores de escala.</span><span class="sxs-lookup"><span data-stu-id="cce82-119">These values are stored as decimal representations of percentages so they can easily be used as scale factors.</span></span> <span data-ttu-id="cce82-120">Por ejemplo, una combinación de efecto del 50 por ciento y una señal de origen del 50 por ciento se representará como un valor de 0,50 para cada variable.</span><span class="sxs-lookup"><span data-stu-id="cce82-120">For instance, a mixture of 50 percent effect and 50 percent source signal would be represented as a value of 0.50 for each variable.</span></span> <span data-ttu-id="cce82-121">La suma de los valores de m \_ fWetMix y m \_ fDryMix no debe ser superior a 1,0 (100 por ciento).</span><span class="sxs-lookup"><span data-stu-id="cce82-121">The sum of the values for m\_fWetMix and m\_fDryMix must not be more than 1.0 (100 percent).</span></span> <span data-ttu-id="cce82-122">Finalmente, estos valores serán accesibles como propiedades.</span><span class="sxs-lookup"><span data-stu-id="cce82-122">Eventually, these values will be accessible as properties.</span></span>

<span data-ttu-id="cce82-123">Agregue el código siguiente al constructor CEcho para establecer los valores predeterminados en 50 por ciento:</span><span class="sxs-lookup"><span data-stu-id="cce82-123">Add the following code to the CEcho constructor to set the default values to 50 percent each:</span></span>


```C++
m_fWetMix = 0.50;  // default to 50 percent wet
m_fDryMix = 0.50;  // default to 50 percent dry

```



## <a name="related-topics"></a><span data-ttu-id="cce82-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cce82-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cce82-125">**Eco de propiedades de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="cce82-125">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




