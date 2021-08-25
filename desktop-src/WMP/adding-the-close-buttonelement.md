---
title: Agregar el elemento BUTTONELEMENT de cierre
description: Agregar el elemento BUTTONELEMENT de cierre
ms.assetid: 18f0ee9d-b0d4-4134-8dd6-6ece480b2818
keywords:
- crear máscaras, elemento BUTTONELEMENT
- Reproductor de Windows Media máscaras,elemento BUTTONELEMENT
- skins,BUTTONELEMENT, elemento
- archivos de definición de máscara, elemento BUTTONELEMENT
- Elemento BUTTONELEMENT
- elements,BUTTONELEMENT
- crear máscaras, botones Cerrar
- Reproductor de Windows Media máscaras, botones Cerrar
- máscaras, botones Cerrar
- archivos de definición de máscara, botones Cerrar
- Botones cerrar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5d2a85e43ae4a664504c213d182b396707ff9cfa663187e7f153fa4cc154e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765484"
---
# <a name="adding-the-close-buttonelement"></a>Agregar el elemento BUTTONELEMENT de cierre

El botón Cerrar es similar en concepto al botón Reproducir, pero tiene códigos y colores diferentes.

Coloque el código **Close BUTTONELEMENT después** del corchete angular de cierre de **Play BUTTONELEMENT**.


```C++
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick="JScript: view.close();" />

```



Los atributos siguientes se usan para definir **BUTTONELEMENT** para el botón Cerrar:

**mappingColor**

Este es el valor de color de la región en el archivo de arte de asignación que creó antes. En este caso, es el color rojo sólido. Este atributo es necesario para cualquier **BUTTONELEMENT.** Al definir este color, se le Reproductor de Windows Media que asocie esta área de color con el código XML de este botón.

**upToolTip**

Esto define el texto que se mostrará cuando el usuario mantenga el mouse sobre el botón. Esto es lo mismo que el botón Reproducir, salvo que está etiquetado como "Cerrar".

**Onclick**

Esto define el evento que tiene lugar cuando el mouse hace clic en el botón. El valor de este atributo de evento se denomina controlador de eventos y será una línea de código de Microsoft JScript o una función JScript en un archivo de texto externo cargado por el atributo **loadScript** de **una vista**. En este caso, el código JScript llama al método **close** del elemento **VIEW** mediante la vista de atributo global **,** que cierra la vista y cierra Reproductor de Windows Media.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear el archivo de definición de máscara**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




