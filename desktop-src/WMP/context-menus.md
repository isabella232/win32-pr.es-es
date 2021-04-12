---
title: Menús contextuales
description: Menús contextuales
ms.assetid: d1ea899a-9087-4502-8825-5cef1a87ef03
keywords:
- Windows Media Player tiendas en línea, menús contextuales
- tiendas en línea, menús contextuales
- tipo 1 tiendas en línea, menús contextuales
- Windows Media Player tiendas en línea, menús contextuales personalizados
- tiendas en línea, menús contextuales personalizados
- tipo 1 almacenes en línea, menús contextuales personalizados
- menús contextuales
- menús contextuales personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba3ed52b408651607cb1f6dab1a04f53282d3ef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420231"
---
# <a name="context-menus"></a><span data-ttu-id="45068-111">Menús contextuales</span><span class="sxs-lookup"><span data-stu-id="45068-111">Context Menus</span></span>

<span data-ttu-id="45068-112">Las tiendas en línea pueden proporcionar menús contextuales personalizados.</span><span class="sxs-lookup"><span data-stu-id="45068-112">Online stores can provide custom context menus.</span></span> <span data-ttu-id="45068-113">Para ello, el complemento de la tienda en línea implementa el método [IWMPContentPartner:: GetCommands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) .</span><span class="sxs-lookup"><span data-stu-id="45068-113">To do this, the online store plug-in implements the [IWMPContentPartner::GetCommands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) method.</span></span> <span data-ttu-id="45068-114">Windows Media Player llama a este método para proporcionar información sobre la ubicación en la interfaz de usuario en la que se muestra el menú contextual (donde el usuario hizo clic con el botón secundario).</span><span class="sxs-lookup"><span data-stu-id="45068-114">Windows Media Player calls this method to provide information about the location in the user interface where the context menu is displayed (where the user right-clicked).</span></span> <span data-ttu-id="45068-115">El complemento devuelve una matriz de estructuras [WMPContextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) que describen cada elemento de menú contextual, incluido un identificador de comando para cada uno.</span><span class="sxs-lookup"><span data-stu-id="45068-115">The plug-in returns an array of [WMPContextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) structures that describe each context menu item, including a command ID for each.</span></span>

<span data-ttu-id="45068-116">Una vez que Windows Media Player ha recuperado la matriz, el reproductor utiliza la matriz para crear el menú contextual que el usuario ve.</span><span class="sxs-lookup"><span data-stu-id="45068-116">After Windows Media Player has retrieved the array, the Player uses the array to build the context menu the user sees.</span></span> <span data-ttu-id="45068-117">Cuando el usuario hace clic en un elemento en el menú contextual, el reproductor llama a [IWMPContentPartner:: InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand), pasando el identificador de comando asociado al elemento de menú mediante el parámetro *dwCommandID* .</span><span class="sxs-lookup"><span data-stu-id="45068-117">When the user clicks an item in the context menu, the Player calls [IWMPContentPartner::InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand), passing the command ID associated with the menu item through the *dwCommandID* parameter.</span></span> <span data-ttu-id="45068-118">El reproductor también pasa un valor de ubicación de la biblioteca y una matriz de identificadores que representa los elementos en los que se invocó el menú, como una matriz de identificadores de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="45068-118">The Player also passes a library location value and an array of IDs that represents the items the menu was invoked upon, such as an array of track IDs.</span></span> <span data-ttu-id="45068-119">Con esta información, el complemento puede iniciar cualquier proceso adecuado en respuesta al clic del mouse del usuario.</span><span class="sxs-lookup"><span data-stu-id="45068-119">By using this information, the plug-in can start any appropriate process in response to the user's mouse click.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45068-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="45068-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45068-121">**Acerca de las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="45068-121">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> </dl>

 

 




