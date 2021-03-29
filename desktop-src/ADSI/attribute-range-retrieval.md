---
title: Recuperación de intervalos de atributos
description: Un atributo con varios valores puede tener casi cualquier número de valores. En muchos casos, puede ser ventajoso, o incluso necesario, limitar el intervalo de valores recuperados por una consulta.
ms.assetid: 3a0eb764-fca9-4ca6-9991-b85f293961af
ms.tgt_platform: multiple
keywords:
- ADSI de recuperación de intervalo de atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f8787eb0b2aba30d1926b4d9cbb7e566e0f59c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993871"
---
# <a name="attribute-range-retrieval"></a>Recuperación de intervalos de atributos

Un atributo con varios valores puede tener casi cualquier número de valores. En muchos casos, puede ser ventajoso, o incluso necesario, limitar el intervalo de valores recuperados por una consulta.

La recuperación por rangos implica solicitar un número limitado de valores de atributo en una sola consulta. El número de valores solicitados debe ser menor o igual que el número máximo de valores admitidos por el servidor. Para reducir el número de veces que la consulta debe ponerse en contacto con el servidor, el número de valores solicitados debe ser lo más cercano posible a este máximo. Para permitir que una aplicación funcione correctamente con todos los servidores de Windows, se debe usar un número máximo de 1000.

Los especificadores de intervalo para una consulta de propiedad requieren el formato siguiente:


```C++
range=<low range>-<high range>
```



donde " &lt; Low Range &gt; " es el índice de base cero del primer valor de propiedad que se va a recuperar y " &lt; High Range &gt; " es el índice de base cero del último valor de propiedad que se va a recuperar. Se usa cero para &lt; el "intervalo inferior &gt; " para especificar la primera entrada. El carácter comodín ( \* ) se puede usar para " &lt; High Range &gt; " a fin de especificar todas las entradas restantes.

En la tabla siguiente se muestran ejemplos de especificadores de intervalo.



| Ejemplo      | Descripción                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------|
| intervalo = 0-\*   | Recupere todos los valores de propiedad. Esto está sujeto a los límites impuestos por el servidor.                |
| intervalo = 0-500  | Recupere de 1 a 501st valores inclusivos.                                                |
| intervalo = 2-3    | Recupere los valores 3 y 4.                                                                  |
| intervalo = 501-\* | Recupere el 502nd y todos los valores restantes. Esto está sujeto a los límites impuestos por el servidor. |



 

Hay varias maneras de recuperar un intervalo de valores de propiedad. El método [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) se puede utilizar en un lenguaje de automatización o en C++. El método **IADs. GetInfoEx** es el método preferido para realizar la recuperación de intervalos. Para obtener más información sobre el uso de **IADs. GetInfoEx** para la recuperación de intervalos, vea [usar iAds:: GetInfoEx para la recuperación de intervalos](using-iads--getinfoex-for-range-retrieval.md).

Si se utiliza un lenguaje de automatización, los objetos de directorio ActiveX (ADO) se pueden usar para recuperar un intervalo de valores de propiedad. Para obtener más información sobre el uso de ADO para la recuperación de intervalos, vea [usar ado para la recuperación por intervalos](using-ado-for-range-retrieval.md).

Si se usa C++, se pueden usar las interfaces [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) y [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para recuperar un intervalo de valores de propiedad. Para obtener más información sobre el uso de **IDirectorySearch** y **IDirectoryObject** para la recuperación de intervalos, vea [usar IDirectorySearch y IDirectoryObject para la recuperación de intervalos](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md).

 

 




