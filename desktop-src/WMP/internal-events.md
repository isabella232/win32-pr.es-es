---
title: Eventos internos
description: Eventos internos
ms.assetid: d99e84ec-41db-42e7-ab26-5ca6a3ba610b
keywords:
- Aspectos de Windows Media Player, eventos internos
- máscaras, eventos internos
- eventos, internos
- escribir código para máscaras, eventos internos
- eventos internos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08ed2abca3f23a89ea6fe261a29639d671e0d58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994012"
---
# <a name="internal-events"></a><span data-ttu-id="c1866-108">Eventos internos</span><span class="sxs-lookup"><span data-stu-id="c1866-108">Internal Events</span></span>

<span data-ttu-id="c1866-109">Puede detectar los cambios que se producen en Windows Media Player o los cambios en su propia máscara.</span><span class="sxs-lookup"><span data-stu-id="c1866-109">You can detect changes that occur in Windows Media Player or changes in your own skin.</span></span> <span data-ttu-id="c1866-110">Estos pueden ser cambios en las propiedades o los métodos de los objetos de Windows Media Player, los cambios en los atributos de máscara, etc.</span><span class="sxs-lookup"><span data-stu-id="c1866-110">These can be changes in Windows Media Player object properties or methods, changes in skin attributes, and so on.</span></span>

## <a name="windows-media-player-property-changes"></a><span data-ttu-id="c1866-111">Cambios en las propiedades de Media Player de Windows</span><span class="sxs-lookup"><span data-stu-id="c1866-111">Windows Media Player Property Changes</span></span>

<span data-ttu-id="c1866-112">Puede procesar los cambios en Windows Media Player mediante el agente de escucha wmpprop.</span><span class="sxs-lookup"><span data-stu-id="c1866-112">You can process changes in Windows Media Player by using the wmpprop listener.</span></span> <span data-ttu-id="c1866-113">Debe configurar el agente de escucha como un valor de un atributo.</span><span class="sxs-lookup"><span data-stu-id="c1866-113">You must set up the listener as a value of an attribute.</span></span> <span data-ttu-id="c1866-114">Ponga el valor entre comillas dobles y empiece con la palabra "wmpprop" seguida de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="c1866-114">Put the value in double quotes, and start with the word "wmpprop" followed by a colon.</span></span> <span data-ttu-id="c1866-115">Después, incluya la propiedad que desea escuchar.</span><span class="sxs-lookup"><span data-stu-id="c1866-115">Then you include the property you want to listen to.</span></span> <span data-ttu-id="c1866-116">Cuando cambie la propiedad, también cambiará el valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="c1866-116">When the property changes, the value of the attribute will change also.</span></span> <span data-ttu-id="c1866-117">Por ejemplo, para cambiar el valor de un elemento Slider cuando cambie el valor del atributo **currentPosition** , escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c1866-117">For example, to have a slider element value change whenever the value of the **currentPosition** attribute changes, type the following:</span></span>


```C++
<SLIDER id="mySlider" value="wmpprop:player.Controls.currentPosition" />
```



-   <span data-ttu-id="c1866-118">**Importante** No use wmpprop en métodos de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="c1866-118">**Important** Do not use wmpprop on Windows Media Player methods.</span></span> <span data-ttu-id="c1866-119">Pueden producirse resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="c1866-119">Unexpected results may occur.</span></span>

## <a name="windows-media-player-method-changes"></a><span data-ttu-id="c1866-120">Cambios del método de Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="c1866-120">Windows Media Player Method Changes</span></span>

<span data-ttu-id="c1866-121">Puede hacer que la máscara responda a la disponibilidad de métodos en Windows Media Player mediante wmpenabled y wmpdisabled.</span><span class="sxs-lookup"><span data-stu-id="c1866-121">You can make your skin respond to the availability of methods on Windows Media Player using wmpenabled and wmpdisabled.</span></span> <span data-ttu-id="c1866-122">Se usan de forma similar al agente de escucha wmpprop, salvo que solo se pueden usar en métodos del objeto de **control** que son compatibles con el método **isavailable** .</span><span class="sxs-lookup"><span data-stu-id="c1866-122">These are used similarly to the wmpprop listener except that you can only use these on methods of the **Control** object that are supported by the **isAvailable** method.</span></span>

<span data-ttu-id="c1866-123">Por ejemplo, puede habilitar un botón solo cuando el método **Play** está habilitado, mediante código como el siguiente:</span><span class="sxs-lookup"><span data-stu-id="c1866-123">For example, you could enable a button only when the **Play** method is enabled, using code like this:</span></span>


```C++
<BUTTON ... enabled="wmpenabled:player.Controls.Play();" />

```



-   <span data-ttu-id="c1866-124">**Importante** No use wmpenabled o wmpdisabled en las propiedades de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="c1866-124">**Important** Do not use wmpenabled or wmpdisabled on Windows Media Player properties.</span></span> <span data-ttu-id="c1866-125">Pueden producirse resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="c1866-125">Unexpected results may occur.</span></span>

## <a name="skin-attribute-changes"></a><span data-ttu-id="c1866-126">Cambios en los atributos de máscara</span><span class="sxs-lookup"><span data-stu-id="c1866-126">Skin Attribute Changes</span></span>

<span data-ttu-id="c1866-127">Puede responder a los cambios en los atributos de máscara de una de las dos maneras siguientes: mediante wmpprop o el evento **\_ onchange** .</span><span class="sxs-lookup"><span data-stu-id="c1866-127">You can respond to changes in your skin attributes in one of two ways, by using wmpprop or the **\_onchange** event.</span></span>

<span data-ttu-id="c1866-128">Puede usar wmpprop para escuchar los cambios en su propia máscara.</span><span class="sxs-lookup"><span data-stu-id="c1866-128">You can use wmpprop to listen for changes in your own skin.</span></span> <span data-ttu-id="c1866-129">Por ejemplo, para mostrar el valor del control deslizante en un cuadro de texto, puede escribir lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c1866-129">For example, to show the Slider value in a text box, you could type the following:</span></span>


```C++
<TEXT ... value="wmpprop:mySlider.value">

```



<span data-ttu-id="c1866-130">Puede usar el evento **\_ onchange** para procesar eventos dentro de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c1866-130">You can use the **\_onchange** event to process events inside an element.</span></span> <span data-ttu-id="c1866-131">Debe adjuntar el nombre del atributo del que desea realizar un seguimiento a **\_ onchange**.</span><span class="sxs-lookup"><span data-stu-id="c1866-131">You must attach the name of the attribute you want to track to **\_onchange**.</span></span> <span data-ttu-id="c1866-132">Por ejemplo, si desea realizar un seguimiento del valor de un cuadro de texto, debe escribir:</span><span class="sxs-lookup"><span data-stu-id="c1866-132">For example, if you want to track the value of a text box, you would type:</span></span>


```C++
value_onchange

```



<span data-ttu-id="c1866-133">A continuación, asignaría una cadena de JScript que desea ejecutar cuando el valor cambie.</span><span class="sxs-lookup"><span data-stu-id="c1866-133">You would then assign a JScript string that you want to run when the value changes.</span></span> <span data-ttu-id="c1866-134">Por ejemplo, para responder a un cambio en el valor de un cuadro de texto que se puede usar para ajustar el volumen de Windows Media Player, escriba lo siguiente en el elemento de **texto** como atributo:</span><span class="sxs-lookup"><span data-stu-id="c1866-134">For example, to respond to a change in the value of a text box that can be used to adjust the volume of Windows Media Player, type the following inside your **TEXT** element as an attribute:</span></span>


```C++
value_onchange = "JScript: player.Settings.Volume = myText.value"

```



## <a name="related-topics"></a><span data-ttu-id="c1866-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c1866-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1866-136">**Controlar eventos**</span><span class="sxs-lookup"><span data-stu-id="c1866-136">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




