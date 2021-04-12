---
title: Usar la interfaz IAccessible
description: La interfaz IAccessible es una colección de métodos que exponen los atributos y comportamientos más comunes de una amplia gama de elementos de la interfaz de usuario.
ms.assetid: 82f6e934-58ea-47f2-98a3-2ab1c20f24c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218d009793dc1bebac2a7e5caeba8fa140ac0d96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357210"
---
# <a name="using-the-iaccessible-interface"></a><span data-ttu-id="12dc6-103">Usar la interfaz IAccessible</span><span class="sxs-lookup"><span data-stu-id="12dc6-103">Using the IAccessible Interface</span></span>

<span data-ttu-id="12dc6-104">La interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) es una colección de métodos que exponen los atributos y comportamientos más comunes de una amplia gama de elementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="12dc6-104">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is a collection of methods that expose the most common attributes and behaviors of a wide range of UI elements.</span></span> <span data-ttu-id="12dc6-105">Un elemento de la interfaz de usuario es un control, como un menú o un botón de menú, que forma parte de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="12dc6-105">A UI element is a control, such as a menu or push button, that is part of the user interface.</span></span> <span data-ttu-id="12dc6-106">Un objeto accesible es un elemento de la interfaz de usuario que tiene una interfaz **IAccessible** significativa.</span><span class="sxs-lookup"><span data-stu-id="12dc6-106">An accessible object is a UI element that has a meaningful **IAccessible** interface.</span></span>

<span data-ttu-id="12dc6-107">Algunas de las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) no se pueden aplicar a todos los tipos de elemento de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="12dc6-107">Some of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties are not applicable to every kind of user interface element.</span></span> <span data-ttu-id="12dc6-108">Además, la implementación de **IAccessible** varía de una aplicación a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="12dc6-108">Also, the implementation of **IAccessible** varies from application to application.</span></span>

<span data-ttu-id="12dc6-109">Aunque los parámetros y los valores devueltos para las propiedades y los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) están totalmente especificados, el modo en que un cliente debe utilizar una propiedad o el modo en que un servidor debe implementar una propiedad a veces está sujeto a una interpretación.</span><span class="sxs-lookup"><span data-stu-id="12dc6-109">Although the parameters and return values for the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods are fully specified, how a client should use a property or how a server should implement a property is sometimes subject to interpretation.</span></span>

<span data-ttu-id="12dc6-110">En esta sección se proporcionan sugerencias, instrucciones y ejemplos para ayudar a las aplicaciones cliente a obtener información sobre los elementos de la interfaz de usuario y para ayudar a las aplicaciones de servidor a proporcionar información adecuada.</span><span class="sxs-lookup"><span data-stu-id="12dc6-110">This section provides suggestions, guidelines, and examples for helping client applications obtain information about UI elements and for helping server applications provide appropriate information.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="12dc6-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="12dc6-111">In this section</span></span>

-   [<span data-ttu-id="12dc6-112">Contenido de propiedades descriptivas</span><span class="sxs-lookup"><span data-stu-id="12dc6-112">Content of Descriptive Properties</span></span>](content-of-descriptive-properties.md)
-   [<span data-ttu-id="12dc6-113">Propiedades y métodos de selección y foco</span><span class="sxs-lookup"><span data-stu-id="12dc6-113">Selection and Focus Properties and Methods</span></span>](selection-and-focus-properties-and-methods.md)
-   [<span data-ttu-id="12dc6-114">Métodos y propiedades de navegación de objetos</span><span class="sxs-lookup"><span data-stu-id="12dc6-114">Object Navigation Properties and Methods</span></span>](object-navigation-properties-and-methods.md)

 

 




