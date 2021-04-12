---
title: Agregando el cerrar BUTTONELEMENT
description: Agregando el cerrar BUTTONELEMENT
ms.assetid: 18f0ee9d-b0d4-4134-8dd6-6ece480b2818
keywords:
- crear máscaras, elemento BUTTONELEMENT
- Aspectos de Windows Media Player, elemento BUTTONELEMENT
- máscaras, elemento BUTTONELEMENT
- archivos de definición de máscara, elemento BUTTONELEMENT
- BUTTONELEMENT (elemento)
- elementos, BUTTONELEMENT
- crear máscaras, cerrar botones
- Aspectos de Windows Media Player, botones de cierre
- máscaras, botones de cierre
- archivos de definición de máscara, botones de cierre
- Botones cerrar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40716d4094d23eaf6ab86414f37c0778cc8d89cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268870"
---
# <a name="adding-the-close-buttonelement"></a>Agregando el cerrar BUTTONELEMENT

El botón Cerrar es similar en concepto al botón reproducir, pero tiene códigos y colores distintos.

Coloque el código **BUTTONELEMENT** de cierre después del corchete angular de cierre de la ejecución de **ButtonElement**.


```C++
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick="JScript: view.close();" />

```



Los atributos siguientes se usan para definir **BUTTONELEMENT** para el botón Cerrar:

**mappingColor**

Este es el valor de color de la región en el archivo de imagen de asignación que creó antes. En este caso, es el color rojo sólido. Este atributo es necesario para cualquier **BUTTONELEMENT**. Al definir este color, está indicando a Windows Media Player que asocie esta área de color con el código XML de este botón.

**Información sobre herramientas**

Define el texto que se mostrará cuando el usuario mantenga el mouse sobre el botón. Es lo mismo que el botón reproducir, salvo que tiene la etiqueta "cerrar".

**AlHacerClic**

Define el evento que se produce cuando se hace clic con el mouse en el botón. El valor de este atributo de evento se denomina controlador de eventos y será una línea de código de Microsoft JScript o una función de JScript en un archivo de texto externo cargado por el atributo **loadScript** de una **vista**. En este caso, el código JScript llama al método **Close** del elemento **View** mediante la **vista** de atributos global, que cierra la vista y cierra Windows Media Player.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear el archivo de definición de máscara**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




