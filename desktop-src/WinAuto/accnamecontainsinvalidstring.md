---
title: AccNameContainsInvalidString
description: AccNameContainsInvalidString
ms.assetid: 392E4D10-4A8E-4118-B0E7-F74571812043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670672769c22cba556c164b8d03b2e9148fb8b1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695462"
---
# <a name="accnamecontainsinvalidstring"></a><span data-ttu-id="fb82d-103">AccNameContainsInvalidString</span><span class="sxs-lookup"><span data-stu-id="fb82d-103">AccNameContainsInvalidString</span></span>

## <a name="text"></a><span data-ttu-id="fb82d-104">Texto</span><span class="sxs-lookup"><span data-stu-id="fb82d-104">Text</span></span>

<span data-ttu-id="fb82d-105">accName no debe contener la cadena {0}</span><span class="sxs-lookup"><span data-stu-id="fb82d-105">accName should not contain the string {0}</span></span>

## <a name="type"></a><span data-ttu-id="fb82d-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb82d-106">Type</span></span>

<span data-ttu-id="fb82d-107">Error</span><span class="sxs-lookup"><span data-stu-id="fb82d-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="fb82d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb82d-108">Description</span></span>

<span data-ttu-id="fb82d-109">El nombre de un elemento contiene caracteres no válidos (estos caracteres se reemplazan por AccChecker).</span><span class="sxs-lookup"><span data-stu-id="fb82d-109">The name of an element contains invalid characters (these characters are replaced by AccChecker).</span></span> <span data-ttu-id="fb82d-110">Por ejemplo, el método [**Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) que se usa para recuperar el nombre de MSAA de un elemento devuelve una cadena que contiene caracteres de tabulación, nueva línea o de y comercial.</span><span class="sxs-lookup"><span data-stu-id="fb82d-110">For example, the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method used to retrieve the MSAA name of an element returns a string that contains tab, newline, or ampersand characters.</span></span>

<span data-ttu-id="fb82d-111">Este problema causa problemas para las personas que dependen de un lector de pantalla y un teclado para la navegación porque un elemento podría tener un nombre no descriptivo y no intuitivo.</span><span class="sxs-lookup"><span data-stu-id="fb82d-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="fb82d-112">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="fb82d-112">Possible causes</span></span>

<span data-ttu-id="fb82d-113">El elemento o su elemento primario tiene un nombre o una etiqueta asignados incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="fb82d-113">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb82d-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb82d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb82d-115">**IAccessible:: get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="fb82d-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="fb82d-116">Propiedad Name</span><span class="sxs-lookup"><span data-stu-id="fb82d-116">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




