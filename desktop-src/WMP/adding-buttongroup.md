---
title: Agregar BUTTONGROUP
description: Agregar BUTTONGROUP
ms.assetid: 07a4a347-b3da-4dcb-b3e4-bee0d002b2e2
keywords:
- crear máscaras, elemento BUTTONGROUP
- Aspectos de Windows Media Player, elemento BUTTONGROUP
- aspectos, elemento BUTTONGROUP
- archivos de definición de máscara, elemento BUTTONGROUP
- Elemento BUTTONGROUP
- elementos, BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90659a2e867a65d2751532701b71810a532c8ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356873"
---
# <a name="adding-buttongroup"></a>Agregar BUTTONGROUP

En este ejemplo se usa el elemento **BUTTONGROUP** para la codificación en el archivo de definición de máscara. **BUTTONGROUP** crea una manera fácil de procesar eventos del mouse sin tener que calcular ubicaciones exactas en la pantalla y utiliza el color en lugar de las coordenadas x e y.

En primer lugar, debe agregar las etiquetas **BUTTONGROUP** al archivo de definición de máscara que creó. Colóquelos después de los atributos de la etiqueta de **tema** .


```C++
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">


        </BUTTONGROUP>

```



Deje unas cuantas líneas en blanco por encima de la etiqueta **BUTTONGROUP** de cierre para los botones que va a agregar a continuación.

Los atributos siguientes se usan para definir **BUTTONGROUP**:

**mappingImage**

Este es el nombre de archivo del archivo de imagen de asignación que creó antes, el que tiene los círculos rojo y verde. Este atributo es necesario para cualquier **BUTTONGROUP**.

**hoverImage**

Este es el nombre de archivo del archivo de imagen emergente que ha creado antes, el que tiene los dos botones amarillos que leen "Play" y "CLOSE". Esto no es necesario, pero una imagen de mantener el mouse ayuda a proporcionar comentarios al usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear el archivo de definición de máscara**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




