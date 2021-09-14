---
title: Sección Descripción
description: Sección Descripción
ms.assetid: 280a9a4d-935f-440d-a606-94aeba0007db
keywords:
- Reproductor de Windows Media Máscaras móviles, sección Descripción
- máscaras, sección Descripción
- crear máscaras, sección Descripción
- escribir código para máscaras, sección Descripción
- Sección Descripción en máscaras
- archivos de definición de máscara, sección Descripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9518b6b1de128457dc3e6b3738ddab9be2a873
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068483"
---
# <a name="description-section"></a>Sección Descripción

A continuación, debe proporcionar una sección que describa el tamaño y la orientación de la máscara al crear una máscara para la serie 9 de Reproductor de Windows Media para Windows Mobile 2003 y versiones posteriores:


```C++
[ Description ]
//              <X,Y>       <DPI>
//              ------      -----
    Dimensions  240, 320    96

//    <Orientation>
//    -------------
    Orientation Portrait

```



La sección Descripción debe comenzar con la palabra Descripción entre corchetes e incluir una línea que especifique las dimensiones y la resolución de visualización de la máscara.

Las líneas que comienzan con dos barras diagonales no se procesan y se pueden usar para comentarios o, como se muestra en el código anterior, una plantilla para ayudarle a recordar lo que aparece en una sección. También puede usar plantillas para ayudar a alinear todo en columnas.

Para obtener más información sobre la sección Descripción, vea [Descripción en](description.md) la referencia de máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escritura del código**](writing-the-code.md)
</dt> </dl>

 

 




