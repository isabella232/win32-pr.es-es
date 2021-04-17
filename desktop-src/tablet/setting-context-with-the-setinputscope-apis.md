---
description: La técnica de programación recomendada para establecer contextos en una aplicación que no está habilitada para tinta es usar las funciones de SetInputScope para asociar el contexto con los campos de la aplicación.
ms.assetid: 95b93804-8079-4b97-b1b0-dfc0138c94e8
title: Configuración del contexto con las API de SetInputScope
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c1b507b1719bea8c04288dca9214ad5675f8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678039"
---
# <a name="setting-context-with-the-setinputscope-apis"></a><span data-ttu-id="622d1-103">Configuración del contexto con las API de SetInputScope</span><span class="sxs-lookup"><span data-stu-id="622d1-103">Setting Context with the SetInputScope APIs</span></span>

<span data-ttu-id="622d1-104">La técnica de programación recomendada para establecer contextos en una aplicación que no está habilitada para tinta es usar las funciones de [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) para asociar el contexto con los campos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="622d1-104">The recommended programmatic technique for setting contexts in an application that is not ink enabled is to use the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions to associate context with the fields in the application.</span></span>

<span data-ttu-id="622d1-105">El kit de desarrollo de Microsoft Windows XP Tablet PC Edition 1,7 era la primera versión de Microsoft Windows para ofrecer [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span><span class="sxs-lookup"><span data-stu-id="622d1-105">The Microsoft Windows XP Tablet PC Edition Development Kit 1.7 was the first version of Microsoft Windows to offer [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span></span> <span data-ttu-id="622d1-106">Windows Vista también proporciona compatibilidad con estas funciones.</span><span class="sxs-lookup"><span data-stu-id="622d1-106">Windows Vista also provides support for these functions.</span></span> <span data-ttu-id="622d1-107">Las definiciones de **SetInputScope** se declaran en InputScope. idl e InputScope. h.</span><span class="sxs-lookup"><span data-stu-id="622d1-107">The **SetInputScope** definitions are declared in InputScope.idl and InputScope.h.</span></span> <span data-ttu-id="622d1-108">Para obtener más información, vea [Text Services Framework](../tsf/text-services-framework.md).</span><span class="sxs-lookup"><span data-stu-id="622d1-108">For more details, see [Text Services Framework](../tsf/text-services-framework.md).</span></span>

<span data-ttu-id="622d1-109">Las funciones [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) son el método recomendado para establecer el contexto de los controles y las aplicaciones que no están habilitadas para tinta.</span><span class="sxs-lookup"><span data-stu-id="622d1-109">The [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions are the recommended way to set context for controls and applications that are not ink enabled.</span></span>

## <a name="common-input-scopes"></a><span data-ttu-id="622d1-110">Ámbitos de entrada comunes</span><span class="sxs-lookup"><span data-stu-id="622d1-110">Common Input Scopes</span></span>

<span data-ttu-id="622d1-111">Con las funciones [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) y el conjunto definido de ámbitos de entrada comunes descritos en la enumeración [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) , puede mejorar la precisión del reconocimiento de los reconocedores de escritura a mano de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="622d1-111">Using the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions and the defined set of common input scopes described in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration, you can improve the recognition accuracy of the Microsoft handwriting recognizers.</span></span>

> [!Note]  
> <span data-ttu-id="622d1-112">Los reconocedores para inglés (Estados Unidos), Inglés (Reino Unido), alemán, Francés, Italiano, español, holandés y Portugués actualmente admiten el uso de los ámbitos de entrada comunes con [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span><span class="sxs-lookup"><span data-stu-id="622d1-112">The recognizers for English (United States), English (United Kingdom), German, French, Italian, Spanish, Dutch, and Portuguese currently support using the common input scopes with [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span></span>

 

 

 
