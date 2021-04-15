---
title: Anotación de asignación de valores
description: Anotación de asignación de valores
ms.assetid: f7c9304a-0eed-4a73-ab06-56723f3cfa5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d21b04374344475689989c2570af6975dc97c13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104555605"
---
# <a name="value-map-annotation"></a>Anotación de asignación de valores

Con la anotación de asignación de valores, puede utilizar una cadena de asignación para indicar cómo corresponde el índice de imagen de un elemento de una vista de lista o vista de árbol con su rol o estado. Por ejemplo, una cadena de asignación puede indicar que el índice 0 de la imagen de una vista de lista se asigna a un rol de la casilla, mientras que el índice de imagen 1 se asigna a un rol de botón de radio.

También puede usar la anotación de asignación de valores para especificar cadenas que se asignan a los valores numéricos en un control deslizante.

## <a name="when-to-use-this-technique"></a>Cuándo usar esta técnica

Considere la posibilidad de utilizar la anotación de asignación de valores en las siguientes situaciones.

-   Cuando una vista de lista o una vista de árbol dibujada por el propietario incorpora el uso de imágenes y desea proporcionar una descripción accesible personalizada (propiedad [**Description**](description-property.md) ) basada en esa imagen. En la siguiente ilustración se muestra un ejemplo.

    ![Ilustración del menú Inicio, donde los iconos proporcionan pistas visuales al contenido](images/iconlist.gif)

-   Cuando una vista de lista dibujada por el propietario o un control de vista de árbol incorpora el uso de imágenes para que el árbol o los elementos de la lista actúen como controles simples, normalmente las casillas o los botones de radio, y desea asignar la imagen a un rol. En la captura de pantalla siguiente se muestra un ejemplo.

    ![captura de pantalla de las opciones de Internet Explorer para establecer el valor de las casillas y los botones de radio](images/customlist.gif)

-   Cuando se usa un control deslizante para seleccionar un valor que se puede describir como algo distinto de un entero simple, como en la siguiente captura de pantalla, donde la configuración de la resolución de pantalla se describe mediante una cadena.

    ![captura de pantalla de un control deslizante que se usa para establecer la resolución de pantalla](images/slider.gif)

Con la anotación de asignación de valores, una cadena de asignación indica el modo en que el índice de imagen del árbol o de la lista corresponde a su rol o estado. O bien, puede indicar el modo en que el valor numérico de un control deslizante corresponde a una cadena. Por ejemplo, una cadena de asignación puede indicar que el índice 0 de la imagen de una vista de lista se asigna a un rol de casilla y el índice de imagen 1 se asigna a un rol de botón de radio. Use [**IAccPropServices:: SetHwndPropStr ()**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) para adjuntar la cadena de asignación al control.

Dado que se requiere conocimiento específico del control para admitir la asignación de valores, hay un número limitado de controles y propiedades que admiten la anotación de asignación de valores, incluidos los mapas de valores del control deslizante, las vistas de lista y las vistas de árbol.

## <a name="slider-value-map&quot;></a>Mapa de valores de control deslizante

**PROPID \_ ACC \_** se incluye en una asignación de las posiciones internas del control deslizante a cadenas legibles para el usuario. Esta propiedad es compatible con el Oleacc.dll el proxy de control deslizante. Si el valor del control deslizante actual se encuentra en el mapa de valores, la cadena correspondiente se expondrá como el valor en lugar de la cadena de porcentaje predeterminada (por ejemplo, &quot;50").

## <a name="list-view-and-tree-view"></a>Vista de lista y vista de árbol

**PROPID \_ ACC \_ ROLEMAP**, **PROPID \_ ACC \_ STATEMAP** y **PROPID \_ ACC \_ DESCRIPTONMAP** proporcionan asignaciones desde los índices de imagen de estado a los valores de rol y estado. Estos mapas permiten asignar esos índices de imagen a los roles adecuados (normalmente, [**CHECKBUTTON \_ del \_ sistema de roles**](object-roles.md) o de [**\_ sistema \_ de roles**](object-roles.md)) y bits de estado adicionales (normalmente, el [**sistema de estado \_ \_ está activado**](object-state-constants.md)).

Para obtener más información sobre la anotación de asignación de valores, vea los temas siguientes:

-   [Usar anotación de asignación de valores](using-value-map-annotation.md)
-   [Ejemplo de anotación de mapa de valores](value-map-annotation-sample.md)

## <a name="annotation-map-format"></a>Formato de asignación de anotaciones

En la tabla siguiente se describen los campos que se incluyen en una asignación de anotación.



| Campo               | Descripción                                                                                                                                                                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Un                 | Indica que se utiliza un esquema de codificación determinado. Es posible que se admitan prefijos adicionales para los esquemas de codificación futuros.                                                                                                                                                          |
| Carácter delimitador | Normalmente dos puntos (:) se usa, pero puede ser otro carácter excepto **null** o un espacio vacío. Dado que este carácter se utilizará como delimitador para los campos restantes, no se puede usar como parte de un valor en el mapa.                                               |
| 0, 1 o 2          | Valor que indica qué clave se está usando. En las vistas de árbol y de vista de lista y en las asignaciones de estado, esta clave puede ser 0 (índice de imagen), 1 (índice de imagen de estado) o 2 (índice de imagen superpuesta). En el caso de los controles deslizantes y otros controles que no ofrecen una selección de claves, este valor debe ser 0. |
| Carácter delimitador | :                                                                                                                                                                                                                                                                             |
| Pares clave-valor     | Cada par se compone de una cadena de clave y un carácter delimitador. La cadena de clave es un número y puede estar en formato decimal o hexadecimal (con un prefijo "0x" inicial).                                                                                                            |
| Cadena de valor        | En el caso de los mapas de valores, se trata de una cadena. En el caso de las asignaciones de roles y Estados, es un número (decimal o hexadecimal).                                                                                                                                                                         |
| Carácter delimitador | :                                                                                                                                                                                                                                                                             |



 

Por ejemplo, un mapa puede tener un aspecto similar al siguiente:


```C++
A:0:0:Cold:1:Warm:3:Hot:
```



Cuando se aplica este mapa de valores a un control deslizante, se expondrá un valor "cálido" cuando el control deslizante esté en la posición 1. Dado que el valor 2 no se incluye en este ejemplo, se expondrá el valor predeterminado de esa posición. Para un control deslizante, el valor predeterminado sería un valor porcentual, como 33.

 

 




