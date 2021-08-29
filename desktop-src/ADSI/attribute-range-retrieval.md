---
title: Recuperación del intervalo de atributos
description: Un atributo con varios valores puede tener casi cualquier número de valores. En muchos casos, puede ser ventajoso o incluso necesario limitar el intervalo de valores recuperados por una consulta.
ms.assetid: 3a0eb764-fca9-4ca6-9991-b85f293961af
ms.tgt_platform: multiple
keywords:
- ADSI de recuperación de intervalos de atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc140a713feb141890478f830bbd24a95a4e7ef7
ms.sourcegitcommit: 3fbe7c00125bed49e333b44b2ed733079e4a1cac
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/16/2021
ms.locfileid: "122208171"
---
# <a name="attribute-range-retrieval"></a>Recuperación del intervalo de atributos

Un atributo con varios valores puede tener casi cualquier número de valores. En muchos casos, puede ser ventajoso o incluso necesario limitar el intervalo de valores recuperados por una consulta.

La recuperación de intervalos implica solicitar un número limitado de valores de atributo en una sola consulta. El número de valores solicitados debe ser menor o igual que el número máximo de valores admitidos por el servidor. Para reducir el número de veces que la consulta debe ponerse en contacto con el servidor, el número de valores solicitados debe estar lo más cerca posible de este máximo. Para permitir que una aplicación funcione correctamente con todos los Windows, se debe usar un número máximo de 1000.

Los especificadores de intervalo para una consulta de propiedades requieren el formato siguiente:


```C++
range=<low range>-<high range>
```



donde " low range " es el índice de base cero del primer valor de propiedad que se va a recuperar y " high range " es el índice de base cero del último valor de propiedad que se va a &lt; &gt; &lt; &gt; recuperar. Cero se usa para &lt; "intervalo &gt; bajo" para especificar la primera entrada. El carácter comodín ( \* ) se puede usar para " intervalo alto " para especificar todas las entradas &lt; &gt; restantes.

En la tabla siguiente se enumeran ejemplos de especificadores de intervalo.



| Ejemplo      | Descripción                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------|
| range=0-\*   | Recupere todos los valores de propiedad. Esto está sujeto a los límites impuestos por el servidor.                |
| range=0-500  | Recupere de los valores 1 a 501, ambos incluidos.                                                |
| range=2-3    | Recupere los valores 3 y 4.                                                                  |
| range=501-\* | Recupere el 502 y todos los valores restantes. Esto está sujeto a los límites impuestos por el servidor. |



 

Hay varias maneras diferentes de recuperar un intervalo de valores de propiedad. El [**método IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) se puede usar en un lenguaje de automatización o en C++. El **método IADs.GetInfoEx** es el método preferido para realizar la recuperación de intervalos. Para obtener más información sobre el uso de **IADs.GetInfoEx** para la recuperación de [intervalos, vea Using IADs::GetInfoEx for Range Retrieval](using-iads--getinfoex-for-range-retrieval.md).

Si se usa un lenguaje de automatización, ActiveX Directory Objects (ADO) se puede usar para recuperar un intervalo de valores de propiedad. Para obtener más información sobre el uso de ADO para la recuperación de intervalos, vea [Uso de ADO para la recuperación de intervalos.](using-ado-for-range-retrieval.md)

Si se usa C++, las interfaces [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) e [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) se pueden usar para recuperar un intervalo de valores de propiedad. Para obtener más información sobre el **uso de IDirectorySearch** e **IDirectoryObject** para la recuperación de intervalos, vea Uso de [IDirectorySearch e IDirectoryObject para la recuperación de intervalos.](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md)  Este tipo de recuperación debe realizarse en consultas con un tipo de ámbito base (ADS_SCOPE_BASE).

 

 




