---
description: Información general sobre el uso de Active Accessibility para exponer texto.
ms.assetid: c04ade90-5f17-4e16-b82b-c99230000954
title: Usar Active Accessibility para exponer texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d475a8c576e109f47be7b5a3d61cddf543038d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705545"
---
# <a name="using-active-accessibility-to-expose-text"></a><span data-ttu-id="c4e40-103">Usar Active Accessibility para exponer texto</span><span class="sxs-lookup"><span data-stu-id="c4e40-103">Using Active Accessibility to Expose Text</span></span>

<span data-ttu-id="c4e40-104">Las aplicaciones pueden usar Microsoft Active Accessibility para exponer texto.</span><span class="sxs-lookup"><span data-stu-id="c4e40-104">Applications can use Microsoft Active Accessibility to expose text.</span></span> <span data-ttu-id="c4e40-105">Sin embargo, la interfaz [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) definida por versiones anteriores de Active Accessibility no está optimizada para exponer grandes cantidades de texto enriquecido.</span><span class="sxs-lookup"><span data-stu-id="c4e40-105">However, the [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) interface defined by earlier versions of Active Accessibility is not optimized for exposing large amounts of rich text.</span></span> <span data-ttu-id="c4e40-106">Las versiones posteriores definen las interfaces que están optimizadas para exponer grandes cantidades de texto y atributos textuales.</span><span class="sxs-lookup"><span data-stu-id="c4e40-106">Later versions define interfaces that are optimized for exposing large amounts of text and textual attributes.</span></span>

<span data-ttu-id="c4e40-107">Para exponer texto de grandes cantidades, cree objetos de modelo de objetos componentes (COM) independientes que admitan [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible), o elementos secundarios, para representar cada ejecución de texto.</span><span class="sxs-lookup"><span data-stu-id="c4e40-107">To expose large amounts text, create separate Component Object Model (COM) objects that support [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible), or child elements, to represent each run of text.</span></span> <span data-ttu-id="c4e40-108">Una ejecución es una línea o parte de una línea que comparte el mismo formato.</span><span class="sxs-lookup"><span data-stu-id="c4e40-108">A run is a line, or portion of a line, that shares the same formatting.</span></span>

<span data-ttu-id="c4e40-109">Active Accessibility solo expone el texto y su ubicación, pero no tiene ningún mecanismo para exponer el formato del texto.</span><span class="sxs-lookup"><span data-stu-id="c4e40-109">Active Accessibility exposes only the text and its location, but has no mechanism for exposing the formatting of the text.</span></span> <span data-ttu-id="c4e40-110">A pesar de estas limitaciones, algunos programas usan Active Accessibility para exponer texto.</span><span class="sxs-lookup"><span data-stu-id="c4e40-110">Despite these limitations, some programs use Active Accessibility to expose text.</span></span> <span data-ttu-id="c4e40-111">Por ejemplo, Microsoft Internet Explorer y Microsoft Visual Studio usan Active Accessibility para exponer grandes cantidades de texto.</span><span class="sxs-lookup"><span data-stu-id="c4e40-111">For example, Microsoft Internet Explorer and Microsoft Visual Studio both use Active Accessibility to expose large amounts of text.</span></span>

<span data-ttu-id="c4e40-112">Para obtener más información sobre cómo exponer texto mediante Active Accessibility, vea [accesibilidad](../accessibility/accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="c4e40-112">For more information about exposing text by using Active Accessibility, see [Accessibility](../accessibility/accessibility.md).</span></span>

 

 
