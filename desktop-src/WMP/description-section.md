---
title: Sección Descripción
description: Sección Descripción
ms.assetid: 280a9a4d-935f-440d-a606-94aeba0007db
keywords:
- Aspectos de Windows Media Player Mobile, sección Descripción
- aspectos, sección Descripción
- crear máscaras, sección Descripción
- escribir código para máscaras, sección Descripción
- Sección de descripción en máscaras
- archivos de definición de máscara, sección Descripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9518b6b1de128457dc3e6b3738ddab9be2a873
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903800"
---
# <a name="description-section"></a>Sección Descripción

A continuación, debe proporcionar una sección que describa el tamaño y la orientación de la máscara al crear una máscara para Windows Media Player 9 series para Windows Mobile 2003 y versiones posteriores:


```C++
[ Description ]
//              <X,Y>       <DPI>
//              ------      -----
    Dimensions  240, 320    96

//    <Orientation>
//    -------------
    Orientation Portrait

```



La sección Descripción debe empezar con la palabra Description entre corchetes y, a continuación, incluir una línea que especifique las dimensiones y la resolución de pantalla de la máscara.

Las líneas que comienzan con dos barras diagonales no se procesan y se pueden usar para comentarios o, como se muestra en el código anterior, una plantilla para ayudarle a recordar lo que ocurre en una sección. También puede usar plantillas para ayudar a alinear todo en las columnas.

Para obtener más información sobre la sección de descripción, vea [Descripción](description.md) en la referencia de la máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escritura del código**](writing-the-code.md)
</dt> </dl>

 

 




