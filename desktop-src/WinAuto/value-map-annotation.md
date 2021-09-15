---
title: Anotación de mapa de valores
description: Anotación de mapa de valores
ms.assetid: f7c9304a-0eed-4a73-ab06-56723f3cfa5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d21b04374344475689989c2570af6975dc97c13
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467916"
---
# <a name="value-map-annotation"></a>Anotación de mapa de valores

Con la anotación de mapa de valores, puede usar una cadena de asignación para indicar cómo el índice de imagen de un elemento en una vista de lista o vista de árbol corresponde a su rol o estado. Por ejemplo, una cadena de asignación puede indicar que el índice de imagen 0 de una vista de lista se asigna a un rol de casilla, mientras que el índice de imagen 1 se asigna a un rol de botón de radio.

También puede usar la anotación de mapa de valores para especificar cadenas que se asignan a los valores numéricos en un control deslizante.

## <a name="when-to-use-this-technique"></a>Cuándo usar esta técnica

Considere la posibilidad de usar anotación de mapa de valores en las situaciones siguientes.

-   Cuando una vista de lista o vista de árbol dibujada por el propietario incorpora el uso de imágenes, y desea proporcionar una descripción accesible personalizada [**(propiedad**](description-property.md) Descripción) basada en esa imagen. En la siguiente ilustración se muestra un ejemplo.

    ![ilustración del menú Inicio, donde los iconos proporcionan pistas visuales al contenido](images/iconlist.gif)

-   Cuando una vista de lista dibujada por el propietario o un control de vista de árbol incorpora el uso de imágenes para que los elementos de árbol o lista actúen como controles simples, normalmente casillas o botones de radio, y quiere asignar la imagen a un rol. En la siguiente captura de pantalla se muestra un ejemplo.

    ![captura de pantalla de las opciones de Internet Explorer para establecer el valor de las casillas y los botones de radio](images/customlist.gif)

-   Cuando se usa un control deslizante para seleccionar un valor que se puede describir como algo distinto de un entero simple, como en la siguiente captura de pantalla, donde la configuración de resolución de pantalla se describe mediante una cadena.

    ![captura de pantalla de un control deslizante que se usa para establecer la resolución de pantalla](images/slider.gif)

Con la anotación de mapa de valores, una cadena de asignación indica cómo el índice de imagen de la lista o árbol corresponde a su rol o estado. O bien, puede indicar cómo se corresponde el valor numérico de un control deslizante a una cadena. Por ejemplo, una cadena de asignación puede indicar que el índice de imagen 0 de una vista de lista se asigna a un rol de casilla e índice de imagen 1 se asigna a un rol de botón de radio. Use [**IAccPropServices::SetHwndPropStr() para**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) adjuntar la cadena de asignación al control.

Dado que el conocimiento específico del control es necesario para admitir la asignación de valores, hay un número limitado de controles y propiedades que admiten la anotación de mapa de valores, incluidos los mapas de valores de control deslizante, las vistas de lista y las vistas de árbol.

## <a name="slider-value-map"></a>Mapa de valores de control deslizante

**PROPID \_ ACC \_ VALUEMAP** contiene una asignación de las posiciones del control deslizante interno a las cadenas legibles por el usuario. Esta propiedad es compatible con el proxy Oleacc.dll control deslizante. Si el valor del control deslizante actual se encuentra en la asignación de valores, la cadena correspondiente se expone como el valor en lugar de la cadena de porcentaje predeterminada (por ejemplo, "50").

## <a name="list-view-and-tree-view"></a>Vista de lista y vista de árbol

**PROPID \_ ROLEMAP \_ de ACC,** **PROPID \_ ACC \_ STATEMAP** y **PROPID \_ ACC \_ DESCRIPTONMAP** proporcionan asignaciones de índices de imagen de estado a valores de rol y estado. Estas asignaciones permiten asignar esos índices de imagen a los roles adecuados (normalmente [**ROLE \_ SYSTEM \_ RADIOBUTTON**](object-roles.md) o [**ROLE SYSTEM \_ \_ CHECKBUTTON)**](object-roles.md)y bits de estado adicionales (normalmente [**STATE SYSTEM \_ \_ CHECKED**](object-state-constants.md)).

Para obtener más información sobre la anotación de mapa de valores, vea los temas siguientes:

-   [Usar anotación de mapa de valores](using-value-map-annotation.md)
-   [Ejemplo de anotación de mapa de valores](value-map-annotation-sample.md)

## <a name="annotation-map-format"></a>Formato del mapa de anotaciones

En la tabla siguiente se describen los campos que se incluyen en un mapa de anotaciones.



| Campo               | Descripción                                                                                                                                                                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 'A'                 | Indica que se usa un esquema de codificación determinado. Es posible que se admiten prefijos adicionales para esquemas de codificación futuros.                                                                                                                                                          |
| Carácter delimitador | Normalmente, dos puntos (:) se usa, pero puede ser otro carácter excepto **NULL** o un espacio vacío. Dado que este carácter se usará como delimitador para los campos restantes, puede que no se utilice como parte de un valor en el mapa.                                               |
| 0, 1 o 2          | Valor que indica qué clave se está utilizando. Para los roles Vista de árbol y Vista de lista y Mapas de estado, esta clave puede ser 0 (índice de imagen), 1 (índice de imagen de estado) o 2 (índice de imagen superpuesta). Para los controles deslizantes y otros controles que no ofrecen una opción de claves, este valor debe ser 0. |
| Carácter delimitador | :                                                                                                                                                                                                                                                                             |
| Pares clave-valor     | Cada par consta de una cadena de clave y un carácter delimitador. La cadena de clave es un número y puede estar en formato decimal o hexadecimal (con un prefijo "0x" inicial).                                                                                                            |
| Cadena de valor        | En el caso de las asignaciones de valores, se trata de una cadena. En el caso de las asignaciones de roles y estados, se trata de un número (decimal o hexadecimal).                                                                                                                                                                         |
| Carácter delimitador | :                                                                                                                                                                                                                                                                             |



 

Por ejemplo, un mapa puede tener un aspecto parecido al siguiente:


```C++
A:0:0:Cold:1:Warm:3:Hot:
```



Cuando este mapa de valores se aplica a un control deslizante, se expone un valor de "Warm" cuando el control deslizante está en la posición 1. Dado que el valor 2 no se incluye en este ejemplo, se expone el valor predeterminado para esa posición. Para un control deslizante, el valor predeterminado sería un valor de porcentaje, como 33.

 

 




