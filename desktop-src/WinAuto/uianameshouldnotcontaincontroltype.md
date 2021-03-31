---
title: UiaNameShouldNotContainControlType
description: UiaNameShouldNotContainControlType
ms.assetid: 96F7A5FC-1879-4706-9E67-5B43D57F7281
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6178ca4cd4c4b2ed0deb0070116b597ba3bd1bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903321"
---
# <a name="uianameshouldnotcontaincontroltype"></a><span data-ttu-id="df069-103">UiaNameShouldNotContainControlType</span><span class="sxs-lookup"><span data-stu-id="df069-103">UiaNameShouldNotContainControlType</span></span>

## <a name="text"></a><span data-ttu-id="df069-104">Texto</span><span class="sxs-lookup"><span data-stu-id="df069-104">Text</span></span>

<span data-ttu-id="df069-105">El nombre del elemento ( {0} ) no debe contener el texto de ControlType ( {1} )</span><span class="sxs-lookup"><span data-stu-id="df069-105">Element's Name ({0}) should not contain the text of the ControlType ({1})</span></span>

## <a name="type"></a><span data-ttu-id="df069-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="df069-106">Type</span></span>

<span data-ttu-id="df069-107">Advertencia</span><span class="sxs-lookup"><span data-stu-id="df069-107">Warning</span></span>

## <a name="description"></a><span data-ttu-id="df069-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="df069-108">Description</span></span>

<span data-ttu-id="df069-109">El nombre de un elemento incorpora su tipo de control UIA.</span><span class="sxs-lookup"><span data-stu-id="df069-109">The name of an element incorporates its UIA control type.</span></span> <span data-ttu-id="df069-110">Por ejemplo, esta advertencia puede producirse si la propiedad de nombre de UIA para un elemento con el tipo de control Button está establecida en "My Button".</span><span class="sxs-lookup"><span data-stu-id="df069-110">For example, this warning can occur if the UIA Name property for an element with the Button control type is set to "My Button".</span></span>

<span data-ttu-id="df069-111">Este problema causa problemas para las personas que confían en un lector de pantalla y un teclado para la navegación porque el tipo de control se leerá dos veces, o puede que no sea pronunciable o no intuitivo para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="df069-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because the control type will be read twice, or it may be unpronounceable or non-intuitive for users.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="df069-112">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="df069-112">Possible causes</span></span>

-   <span data-ttu-id="df069-113">El elemento o su elemento primario tiene un nombre o una etiqueta asignados incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="df069-113">The element or its parent has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="df069-114">El elemento o su elemento primario tiene un nombre predeterminado que no se ha revisado en un nombre descriptivo.</span><span class="sxs-lookup"><span data-stu-id="df069-114">The element or its parent has a default name that has not been revised to a friendly name.</span></span> <span data-ttu-id="df069-115">Por ejemplo, button1.</span><span class="sxs-lookup"><span data-stu-id="df069-115">For example, button1.</span></span>
-   <span data-ttu-id="df069-116">Un desarrollador no es consciente de que los lectores de pantalla leen los nombres y los tipos de control.</span><span class="sxs-lookup"><span data-stu-id="df069-116">A developer is not aware that screen readers read names and control types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df069-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="df069-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df069-118">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="df069-118">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="df069-119">**IUIAutomationElement::CurrentName**</span><span class="sxs-lookup"><span data-stu-id="df069-119">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




