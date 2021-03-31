---
title: UiaNameLengthTooLong
description: UiaNameLengthTooLong
ms.assetid: 01AF3F1E-9A3F-48B4-8219-6E80BAFC82EE
keywords:
- UIA_NamePropertyId identificador AutomationElement. NameProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab786b7167dab4a25384ce3abe2509babcf1f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419045"
---
# <a name="uianamelengthtoolong"></a><span data-ttu-id="0d29a-104">UiaNameLengthTooLong</span><span class="sxs-lookup"><span data-stu-id="0d29a-104">UiaNameLengthTooLong</span></span>

## <a name="text"></a><span data-ttu-id="0d29a-105">Texto</span><span class="sxs-lookup"><span data-stu-id="0d29a-105">Text</span></span>

<span data-ttu-id="0d29a-106">El nombre del elemento no debe devolver una cadena más larga que el {0} carácter</span><span class="sxs-lookup"><span data-stu-id="0d29a-106">Element's name should not return a string longer than {0} character</span></span>

## <a name="type"></a><span data-ttu-id="0d29a-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="0d29a-107">Type</span></span>

<span data-ttu-id="0d29a-108">Error</span><span class="sxs-lookup"><span data-stu-id="0d29a-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="0d29a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d29a-109">Description</span></span>

<span data-ttu-id="0d29a-110">El nombre de un elemento contiene demasiados caracteres.</span><span class="sxs-lookup"><span data-stu-id="0d29a-110">The name of an element contains too many characters.</span></span> <span data-ttu-id="0d29a-111">Por ejemplo, el método [**IUIAutomationElement:: CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) que se usa para recuperar el nombre de UIA de un elemento devuelve una cadena mayor que el límite.</span><span class="sxs-lookup"><span data-stu-id="0d29a-111">For example, the [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) method used to retrieve the UIA name of an element returns a string greater than the limit.</span></span>

<span data-ttu-id="0d29a-112">Este problema causa problemas para las personas que dependen de un lector de pantalla y un teclado para la navegación porque un elemento podría tener un nombre no descriptivo y no intuitivo.</span><span class="sxs-lookup"><span data-stu-id="0d29a-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="0d29a-113">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="0d29a-113">Possible causes</span></span>

<span data-ttu-id="0d29a-114">El elemento o su elemento primario tiene un nombre o una etiqueta asignados incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="0d29a-114">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d29a-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0d29a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d29a-116">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0d29a-116">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="0d29a-117">**IUIAutomationElement::CurrentName**</span><span class="sxs-lookup"><span data-stu-id="0d29a-117">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




