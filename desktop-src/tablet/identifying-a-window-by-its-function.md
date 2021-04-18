---
description: Descripción de la identificación de una ventana por su función para Tablet PC.
ms.assetid: 513e0c9d-4c9e-4e7c-8314-bd7603489e89
title: Identificar una ventana por su función
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497f660d6690bd4dc37c252f82f2408da3e3655d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715221"
---
# <a name="identifying-a-window-by-its-function"></a><span data-ttu-id="0ffd0-103">Identificar una ventana por su función</span><span class="sxs-lookup"><span data-stu-id="0ffd0-103">Identifying a Window by Its Function</span></span>

<span data-ttu-id="0ffd0-104">Identifique cada tipo de ventana asignándole una clase de ventana única.</span><span class="sxs-lookup"><span data-stu-id="0ffd0-104">Identify each type of window by assigning it a unique window class.</span></span> <span data-ttu-id="0ffd0-105">Evite tener una sola clase de ventana que se utilice para una amplia variedad de funciones.</span><span class="sxs-lookup"><span data-stu-id="0ffd0-105">Avoid having a single window class that is used for a wide variety of functions.</span></span>

<span data-ttu-id="0ffd0-106">Las ayudas de accesibilidad deben tener esta identificación para poder administrar diferentes ventanas dentro de la misma aplicación.</span><span class="sxs-lookup"><span data-stu-id="0ffd0-106">Accessibility aids must have this identification in order to handle different windows within the same application.</span></span> <span data-ttu-id="0ffd0-107">Puede haber instrucciones independientes para controlar estas ventanas, como anunciar áreas específicas cuando cambia el contenido.</span><span class="sxs-lookup"><span data-stu-id="0ffd0-107">There may be separate instructions for handling these windows, such as announcing specific areas when the content changes.</span></span>

<span data-ttu-id="0ffd0-108">Si no puede usar clases de ventana independientes, puede exponer las diferencias a través de Microsoft <entity type="reg"/> Active Accessibility <entity type="reg"/> , o, si es necesario, por un mensaje de ventana privada que documente en su sitio Web.</span><span class="sxs-lookup"><span data-stu-id="0ffd0-108">If you cannot use separate window classes, you can expose the differences through Microsoft<entity type="reg"/> Active Accessibility<entity type="reg"/>, or if necessary, by a private window message that you document on your website.</span></span>

<span data-ttu-id="0ffd0-109">Para obtener más información sobre cómo exponer clases de ventana mediante Active Accessibility, vea la sección [accesibilidad](/windows/desktop/accessibility) .</span><span class="sxs-lookup"><span data-stu-id="0ffd0-109">For more information about exposing window classes by using Active Accessibility, see the [Accessibility](/windows/desktop/accessibility) section.</span></span>

 

 
