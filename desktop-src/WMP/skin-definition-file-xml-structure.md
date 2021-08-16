---
title: Estructura XML del archivo de definición de máscara
description: Estructura XML del archivo de definición de máscara
ms.assetid: 93325b94-667a-42a6-92f8-78288d36da81
keywords:
- crear máscaras, archivos de definición de máscara
- Reproductor de Windows Media máscaras, archivos de definición de máscara
- máscaras, archivos de definición de máscara
- archivos para máscaras, definición de máscara
- archivos de definición de máscara, estructura XML
- Estructura XML para archivos de definición de máscara
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc3506ab03d3af7445e75983299577c713412fbeb0899d39c7098c55be2450a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995255"
---
# <a name="skin-definition-file-xml-structure"></a>Estructura XML del archivo de definición de máscara

El archivo de definición de máscara se escribe en XML. Una de las características importantes de XML es que está completamente estructurado y es similar a un esquema. El código XML es simplemente una serie de elementos como **VIEW** y **BUTTONGROUP.** Comenzará con los elementos y, a continuación, los definirá con atributos. El resto de este tutorial le dará detalles sobre los atributos, pero este es el esquema de los elementos que se usarán:


```C++
<THEME>
    <VIEW>
        <BUTTONGROUP>
            <BUTTONELEMENT/>
            <BUTTONELEMENT/>
        </BUTTONGROUP>
    </VIEW>
<THEME>

```



Teniendo en cuenta la estructura simple de los elementos, puede tener sentido de los atributos que hacen que cada elemento sea único. Los detalles de cada elemento se tratarán en los temas restantes de esta sección. Para obtener más información sobre los elementos y atributos, vea [la Referencia de programación de máscaras](skin-programming-reference.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear el archivo de definición de máscara**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




