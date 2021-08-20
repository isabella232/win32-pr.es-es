---
description: El uso de comas y punto y coma puede ser el problema de sintaxis más complejo en el formato de archivo y este uso es muy estricto. Las comas se usan para separar los miembros de la matriz; los puntos y coma finalizan cada elemento de datos.
ms.assetid: 82582213-907c-4760-a849-e6cf5f6d60bc
title: Uso de comas y punto y coma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b44d20d4a8e99a75522fa3703d58d82f3bf4dfe130e530d18141b7f45e572717
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044063"
---
# <a name="use-of-commas-and-semicolons"></a>Uso de comas y punto y coma

El uso de comas y punto y coma puede ser el problema de sintaxis más complejo en el formato de archivo y este uso es muy estricto. Las comas se usan para separar los miembros de la matriz; los puntos y coma finalizan cada elemento de datos.

Por ejemplo, si una plantilla se define de la siguiente manera:


```
template mytemp {
DWORD myvar;
}
```



A continuación, una instancia de esta plantilla tiene un aspecto similar al siguiente:


```
mytemp dataTemp {
1;
}
```



Si una plantilla que contiene otra plantilla se define de la siguiente manera;


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
FLOAT aFloat;
mytemp aTemp;
}
```



A continuación, una instancia de esta plantilla tiene un aspecto similar al siguiente:


```
container dataContainer {
1.1;
2; 
3;;
}
```



Tenga en cuenta que la segunda línea que representa el mytemp dentro del contenedor tiene dos puntos y coma al final de la línea. El primer punto y coma indica el final del elemento de datos, aTemp (dentro del contenedor) y el segundo punto y coma indica el final del contenedor.

Si una matriz se define de la siguiente manera:


```
Template mytemp {

array DWORD myvar[3];

}
```



A continuación, una instancia de esto tiene un aspecto similar al siguiente:


```
mytemp aTemp {
1, 2, 3;
}
```



En el ejemplo de matriz, no es necesario que los elementos de datos estén separados por punto y coma porque se delinean mediante comas. El punto y coma al final marca el final de la matriz.

Considere una plantilla que contiene una matriz de elementos de datos definidos por una plantilla.


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
DWORD count;
array mytemp tempArray[count];
}
```



Una instancia de esto tendría un aspecto parecido al del ejemplo siguiente.


```
container aContainer {
3;
1;2;,3;4;,5;6;;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificación de texto](text-encoding.md)
</dt> </dl>

 

 



