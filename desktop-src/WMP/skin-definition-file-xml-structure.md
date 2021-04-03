---
title: Estructura XML del archivo de definición de máscara
description: Estructura XML del archivo de definición de máscara
ms.assetid: 93325b94-667a-42a6-92f8-78288d36da81
keywords:
- crear máscaras, archivos de definición de máscara
- Aspectos de Windows Media Player, archivos de definición de máscara
- máscaras, archivos de definición de máscara
- archivos para máscaras, definición de máscara
- archivos de definición de máscara, estructura XML
- Estructura XML para los archivos de definición de máscara
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8508f1a458930bc2b60d564a45ef08a9f9f5a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075988"
---
# <a name="skin-definition-file-xml-structure"></a>Estructura XML del archivo de definición de máscara

El archivo de definición de máscara se escribe en XML. Una de las características importantes de XML es que está completamente estructurada y es similar a un esquema. El código XML simplemente es una serie de elementos como **View** y **BUTTONGROUP**. Empezará con los elementos y, a continuación, los definirá con atributos. En el resto de este tutorial se proporcionan detalles sobre los atributos, pero aquí se muestra el esquema de los elementos que se van a usar:


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



Teniendo en cuenta la estructura simple de los elementos, puede tener sentido los atributos que hacen que cada elemento sea único. Los detalles de cada elemento se tratarán en los temas restantes de esta sección. Para obtener más información sobre los elementos y atributos, vea la [referencia de programación](skin-programming-reference.md)de la máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear el archivo de definición de máscara**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




