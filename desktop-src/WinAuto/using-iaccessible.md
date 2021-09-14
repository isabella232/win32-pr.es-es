---
title: Uso de la interfaz IAccessible
description: La interfaz IAccessible es una colección de métodos que exponen los atributos y comportamientos más comunes de una amplia gama de elementos de interfaz de usuario.
ms.assetid: 82f6e934-58ea-47f2-98a3-2ab1c20f24c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218d009793dc1bebac2a7e5caeba8fa140ac0d96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253226"
---
# <a name="using-the-iaccessible-interface"></a>Uso de la interfaz IAccessible

La [**interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) es una colección de métodos que exponen los atributos y comportamientos más comunes de una amplia gama de elementos de interfaz de usuario. Un elemento de interfaz de usuario es un control, como un menú o un botón de inserción, que forma parte de la interfaz de usuario. Un objeto accesible es un elemento de interfaz de usuario que tiene una **interfaz IAccessible** significativa.

Algunas de las [**propiedades IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) no son aplicables a todos los tipos de elemento de interfaz de usuario. Además, la implementación de **IAccessible** varía de una aplicación a otra.

Aunque los parámetros y los valores devueltos para las propiedades y métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) están totalmente especificados, la forma en que un cliente debe usar una propiedad o cómo debe implementar un servidor una propiedad a veces está sujeta a interpretación.

En esta sección se proporcionan sugerencias, directrices y ejemplos para ayudar a las aplicaciones cliente a obtener información sobre los elementos de la interfaz de usuario y para ayudar a las aplicaciones de servidor a proporcionar la información adecuada.

## <a name="in-this-section"></a>En esta sección

-   [Contenido de propiedades descriptivas](content-of-descriptive-properties.md)
-   [Métodos y propiedades de selección y enfoque](selection-and-focus-properties-and-methods.md)
-   [Propiedades y métodos de navegación de objetos](object-navigation-properties-and-methods.md)

 

 




