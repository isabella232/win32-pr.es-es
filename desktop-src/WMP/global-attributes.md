---
title: Atributos globales (SDK de Windows Media Player)
description: Atributos globales
ms.assetid: 2ed09506-990e-4da2-89d6-6ff77dc43eb2
keywords:
- Aspectos de Windows Media Player, atributos globales
- máscaras, atributos globales
- referencia de máscaras, atributos globales
- atributos globales
- atributos, globales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c3f7a605b5c277b3207cefbbeaaa641f81f026
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2019
ms.locfileid: "104419867"
---
# <a name="global-attributes"></a><span data-ttu-id="cb680-108">Atributos globales</span><span class="sxs-lookup"><span data-stu-id="cb680-108">Global Attributes</span></span>

<span data-ttu-id="cb680-109">Los atributos globales son atributos que proporcionan un acceso fácil a determinados elementos o objetos del reproductor desde cualquier lugar dentro de una máscara.</span><span class="sxs-lookup"><span data-stu-id="cb680-109">Global attributes are attributes that provide easy access to certain player elements or objects from anywhere within a skin.</span></span>

<span data-ttu-id="cb680-110">El atributo global **Player** es una referencia al objeto [Player](player-object.md) y se utiliza para tener acceso a la funcionalidad principal de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="cb680-110">The **player** global attribute is a reference to the [Player](player-object.md) object, and is used to access the primary functionality of Windows Media Player.</span></span> <span data-ttu-id="cb680-111">En el ejemplo siguiente se usa **Player** para comenzar la reproducción de archivos multimedia digitales.</span><span class="sxs-lookup"><span data-stu-id="cb680-111">The following example uses **player** to begin digital media playback.</span></span>


```C++
<BUTTON
  onclick="jscript:player.controls.play();"
/>

```



<span data-ttu-id="cb680-112">El atributo global **Theme** es una referencia al elemento [Theme](theme-element.md) .</span><span class="sxs-lookup"><span data-stu-id="cb680-112">The **theme** global attribute is a reference to the [THEME](theme-element.md) element.</span></span> <span data-ttu-id="cb680-113">Esta es la manera adecuada para tener acceso a los atributos de **tema** , en lugar de especificar un identificador dentro del elemento de **tema** .</span><span class="sxs-lookup"><span data-stu-id="cb680-113">This is the proper way to access **THEME** attributes, rather than by specifying an ID within the **THEME** element.</span></span> <span data-ttu-id="cb680-114">En el ejemplo siguiente se usa el **tema** para abrir una nueva vista.</span><span class="sxs-lookup"><span data-stu-id="cb680-114">The following example uses **theme** to open a new view.</span></span>


```C++
<TEXT 
  value="open" 
  onclick="jscript:theme.openView('newView');"
/>

```



<span data-ttu-id="cb680-115">El atributo de **vista** global es una referencia a la [vista](view-element.md)actual.</span><span class="sxs-lookup"><span data-stu-id="cb680-115">The **view** global attribute is a reference to the current [VIEW](view-element.md).</span></span> <span data-ttu-id="cb680-116">Se puede utilizar en lugar del identificador especificado dentro de los distintos elementos de **vista** .</span><span class="sxs-lookup"><span data-stu-id="cb680-116">This can be used instead of the ID specified within the various **VIEW** elements.</span></span> <span data-ttu-id="cb680-117">En el ejemplo siguiente se usa la **vista** para cerrar la vista actual.</span><span class="sxs-lookup"><span data-stu-id="cb680-117">The following example uses **view** to close the current view.</span></span>


```C++
<BUTTON 
  id="quitbutton"
  onclick="jscript:view.close();"
/>

```



<span data-ttu-id="cb680-118">El atributo global **Event** se usa para tener acceso a los atributos de evento de ambiente desde los controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="cb680-118">The **event** global attribute is used to access ambient event attributes from within event handlers.</span></span> <span data-ttu-id="cb680-119">En el ejemplo siguiente se utiliza el **evento** para determinar si se presiona la tecla Alt al hacer clic en un botón.</span><span class="sxs-lookup"><span data-stu-id="cb680-119">The following example uses **event** to determine whether the ALT key is pressed when a button is clicked.</span></span>


```C++
<BUTTON
  onclick="jscript:if (event.altKey == true) myText.value='ALT';"
/>

```



<span data-ttu-id="cb680-120">El atributo global **playerApplication** es una referencia al objeto [playerApplication](playerapplication-object.md) y lo usan los archivos de máscara proporcionados como interfaces de usuario personalizadas para los controles de reproductor remotos.</span><span class="sxs-lookup"><span data-stu-id="cb680-120">The **playerApplication** global attribute is a reference to the [PlayerApplication](playerapplication-object.md) object, and is used by skin files provided as custom user interfaces for remoted Player controls.</span></span> <span data-ttu-id="cb680-121">El control Player solo se puede incrustar en modo remoto en programas de C++ que implementan la interfaz **IWMPRemoteMediaServices** .</span><span class="sxs-lookup"><span data-stu-id="cb680-121">The Player control can be embedded in remote mode only in C++ programs that implement the **IWMPRemoteMediaServices** interface.</span></span> <span data-ttu-id="cb680-122">En el ejemplo siguiente se usa **playerApplication** para cambiar al modo completo del reproductor.</span><span class="sxs-lookup"><span data-stu-id="cb680-122">The following example uses **playerApplication** to switch to the full mode of the Player.</span></span>


```C++
<BUTTON
  onclick="jscript:playerApplication.switchToPlayerApplication();"
/>

```



<span data-ttu-id="cb680-123">Para obtener más información, consulte [atributos de evento ambiente](ambient-event-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="cb680-123">For more information, see [Ambient Event Attributes](ambient-event-attributes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb680-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cb680-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb680-125">**Varios**</span><span class="sxs-lookup"><span data-stu-id="cb680-125">**Miscellaneous**</span></span>](miscellaneous.md)
</dt> </dl>

 

 




