---
title: Adición de Close BUTTONELEMENT
description: Adición de Close BUTTONELEMENT
ms.assetid: 18f0ee9d-b0d4-4134-8dd6-6ece480b2818
keywords:
- crear máscaras,elemento BUTTONELEMENT
- Reproductor de Windows Media máscaras, elemento BUTTONELEMENT
- skins,BUTTONELEMENT, elemento
- archivos de definición de máscara, elemento BUTTONELEMENT
- Elemento BUTTONELEMENT
- elements,BUTTONELEMENT
- crear máscaras, cerrar botones
- Reproductor de Windows Media máscaras, botones Cerrar
- máscaras, botones Cerrar
- archivos de definición de máscara, botones Cerrar
- Botones cerrar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40716d4094d23eaf6ab86414f37c0778cc8d89cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374318"
---
# <a name="adding-the-close-buttonelement"></a>Adición de Close BUTTONELEMENT

El botón Cerrar es similar en concepto al botón Reproducir, pero tiene diferentes códigos y colores.

Coloque el código **Close BUTTONELEMENT** después del corchete angular de cierre de **PLAY BUTTONELEMENT**.


```C++
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick="JScript: view.close();" />

```



Los atributos siguientes se usan para definir **BUTTONELEMENT** para el botón Cerrar:

**mappingColor**

Este es el valor de color de la región en el archivo de creación de mapas que creó antes. En este caso, es el color rojo sólido. Este atributo es necesario para cualquier **BUTTONELEMENT.** Al definir este color, se le Reproductor de Windows Media que asocie esta área de color con el código XML de este botón.

**upToolTip**

Esto define el texto que se mostrará cuando el usuario mantenga el mouse sobre el botón. Esto es lo mismo que el botón Reproducir, salvo que tiene la etiqueta "Cerrar".

**Onclick**

Esto define el evento que tiene lugar cuando el mouse hace clic en el botón. El valor de este atributo de evento se denomina controlador de eventos y será una línea de código de Microsoft JScript o una función JScript en un archivo de texto externo cargado por el atributo **loadScript** de una **vista**. En este caso, el JScript llama al método **close** del elemento **VIEW** mediante la vista de atributo global **,** que cierra la vista y cierra Reproductor de Windows Media.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación del archivo de definición de máscara**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




