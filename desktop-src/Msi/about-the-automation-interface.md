---
description: Un objeto instalador debe crearse inicialmente para cargar la compatibilidad de automatización necesaria para obtener acceso a los componentes del instalador a través de COM.
ms.assetid: 113ed443-a866-43d4-86bd-fc3b244f2edb
title: Acerca de la interfaz de automatización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655a01a4daccb805bec4a858337c1dce48f0fb82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276538"
---
# <a name="about-the-automation-interface"></a><span data-ttu-id="8b793-103">Acerca de la interfaz de automatización</span><span class="sxs-lookup"><span data-stu-id="8b793-103">About the Automation Interface</span></span>

<span data-ttu-id="8b793-104">Un [**objeto instalador**](installer-object.md) debe crearse inicialmente para cargar la compatibilidad de automatización necesaria para obtener acceso a los componentes del instalador a través de com.</span><span class="sxs-lookup"><span data-stu-id="8b793-104">An [**Installer object**](installer-object.md) must be created initially to load the automation support required to access the installer components through COM.</span></span> <span data-ttu-id="8b793-105">Este objeto proporciona contenedores para crear los objetos de nivel superior y obtener acceso a sus métodos.</span><span class="sxs-lookup"><span data-stu-id="8b793-105">This object provides wrappers to create the top-level objects and access their methods.</span></span> <span data-ttu-id="8b793-106">Estos contenedores simplemente proporcionan traducciones de parámetros para exponer las funciones del instalador de manera coherente con Microsoft Visual Basic sin cambiar el comportamiento de los métodos.</span><span class="sxs-lookup"><span data-stu-id="8b793-106">These wrappers simply provide parameter translations to expose the installer functions in a manner consistent with Microsoft Visual Basic without changing the behavior of the methods.</span></span>

<span data-ttu-id="8b793-107">Siempre que sea posible, se expone un par de métodos de C++ GET y set a Visual Basic como una propiedad única.</span><span class="sxs-lookup"><span data-stu-id="8b793-107">Whenever possible, a pair of Get and Set C++ methods are exposed to Visual Basic as a single property.</span></span> <span data-ttu-id="8b793-108">En algunos casos, los métodos de C++ que toman un argumento de índice se exponen como una propiedad indizada.</span><span class="sxs-lookup"><span data-stu-id="8b793-108">In some cases C++ methods taking an index argument are exposed as an indexed property.</span></span> <span data-ttu-id="8b793-109">Muchos métodos de C++ devuelven el resultado a través de un parámetro, ya que el valor devuelto se utiliza para devolver el error.</span><span class="sxs-lookup"><span data-stu-id="8b793-109">Many C++ methods return the result through a parameter because the return value is used for the error return.</span></span> <span data-ttu-id="8b793-110">Sin embargo, en Visual Basic, los errores se controlan mediante un mecanismo independiente y el resultado siempre se pasa en el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="8b793-110">However, in Visual Basic, errors are handled by a separate mechanism, and the result is always passed in the return value.</span></span>

<span data-ttu-id="8b793-111">Para obtener información sobre el uso de la automatización y la creación del objeto de instalador, vea [usar la interfaz de automatización](using-the-automation-interface.md).</span><span class="sxs-lookup"><span data-stu-id="8b793-111">For information about using automation and creating the Installer object, see [Using the Automation Interface](using-the-automation-interface.md).</span></span>

<span data-ttu-id="8b793-112">Para obtener material de referencia sobre los objetos de Windows Installer, vea referencia de la [interfaz de automatización](automation-interface-reference.md).</span><span class="sxs-lookup"><span data-stu-id="8b793-112">For reference material for the Windows Installer objects, see [Automation Interface Reference](automation-interface-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b793-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8b793-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b793-114">Ejemplos de scripting Windows Installer</span><span class="sxs-lookup"><span data-stu-id="8b793-114">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 



