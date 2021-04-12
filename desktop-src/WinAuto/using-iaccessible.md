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
# <a name="using-the-iaccessible-interface"></a>Usar la interfaz IAccessible

La interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) es una colección de métodos que exponen los atributos y comportamientos más comunes de una amplia gama de elementos de la interfaz de usuario. Un elemento de la interfaz de usuario es un control, como un menú o un botón de menú, que forma parte de la interfaz de usuario. Un objeto accesible es un elemento de la interfaz de usuario que tiene una interfaz **IAccessible** significativa.

Algunas de las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) no se pueden aplicar a todos los tipos de elemento de la interfaz de usuario. Además, la implementación de **IAccessible** varía de una aplicación a la aplicación.

Aunque los parámetros y los valores devueltos para las propiedades y los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) están totalmente especificados, el modo en que un cliente debe utilizar una propiedad o el modo en que un servidor debe implementar una propiedad a veces está sujeto a una interpretación.

En esta sección se proporcionan sugerencias, instrucciones y ejemplos para ayudar a las aplicaciones cliente a obtener información sobre los elementos de la interfaz de usuario y para ayudar a las aplicaciones de servidor a proporcionar información adecuada.

## <a name="in-this-section"></a>En esta sección

-   [Contenido de propiedades descriptivas](content-of-descriptive-properties.md)
-   [Propiedades y métodos de selección y foco](selection-and-focus-properties-and-methods.md)
-   [Métodos y propiedades de navegación de objetos](object-navigation-properties-and-methods.md)

 

 




