---
title: Agregar BUTTONGROUP
description: Agregar BUTTONGROUP
ms.assetid: 07a4a347-b3da-4dcb-b3e4-bee0d002b2e2
keywords:
- crear máscaras, elemento BUTTONGROUP
- Reproductor de Windows Media máscaras, elemento BUTTONGROUP
- máscaras, elemento BUTTONGROUP
- archivos de definición de máscara, elemento BUTTONGROUP
- Elemento BUTTONGROUP
- elements,BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6719bb3974b254f8d9446d45fd6d34385dbfcada4084c7bdd5c3a4e03bb06dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865204"
---
# <a name="adding-buttongroup"></a>Agregar BUTTONGROUP

En este ejemplo se usa **el elemento BUTTONGROUP** para la codificación en el archivo de definición de máscara. **BUTTONGROUP crea** una manera sencilla de procesar eventos del mouse sin tener que calcular ubicaciones exactas en la pantalla y usa el color en lugar de las coordenadas x e y.

En primer lugar, debe agregar las **etiquetas BUTTONGROUP** al archivo de definición de máscara que ha creado. Pónganlos después de los atributos de la etiqueta **THEME.**


```C++
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">


        </BUTTONGROUP>

```



Deje algunas líneas en blanco encima de la etiqueta **BUTTONGROUP de** cierre de los botones que agregará a continuación.

Los atributos siguientes se usan para definir **BUTTONGROUP**:

**mappingImage**

Este es el nombre de archivo del archivo de arte de asignación que creó antes, el que tiene los círculos rojo y verde. Este atributo es necesario para cualquier **BUTTONGROUP.**

**hoverImage**

Este es el nombre de archivo del archivo de arte que ha creado antes, el que tiene los dos botones amarillos que leen "Reproducir" y "Cerrar". Esto no es necesario, pero una imagen de mantener el puntero ayuda a proporcionar comentarios al usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear el archivo de definición de máscara**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




