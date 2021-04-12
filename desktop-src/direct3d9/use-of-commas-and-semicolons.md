---
description: El uso de comas y puntos y comas puede ser el problema de sintaxis más complejo en el formato de archivo, y este uso es muy estricto. Las comas se usan para separar los miembros de la matriz; los puntos y comas terminan cada elemento de datos.
ms.assetid: 82582213-907c-4760-a849-e6cf5f6d60bc
title: Uso de comas y puntos y comas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba238d50ff5d0dace017f16b75547df6b016e14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152686"
---
# <a name="use-of-commas-and-semicolons"></a>Uso de comas y puntos y comas

El uso de comas y puntos y comas puede ser el problema de sintaxis más complejo en el formato de archivo, y este uso es muy estricto. Las comas se usan para separar los miembros de la matriz; los puntos y comas terminan cada elemento de datos.

Por ejemplo, si una plantilla se define de la siguiente manera:


```
template mytemp {
DWORD myvar;
}
```



Después, una instancia de esta plantilla tiene el siguiente aspecto:


```
mytemp dataTemp {
1;
}
```



Si una plantilla que contiene otra plantilla se define de la siguiente manera:


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



Después, una instancia de esta plantilla tiene el siguiente aspecto:


```
container dataContainer {
1.1;
2; 
3;;
}
```



Tenga en cuenta que la segunda línea que representa el contenedor de mi Temp tiene dos puntos y coma al final de la línea. El primer punto y coma indica el final del elemento de datos, aTemp (dentro del contenedor) y el segundo punto y coma indica el final del contenedor.

Si una matriz se define de la manera siguiente:


```
Template mytemp {

array DWORD myvar[3];

}
```



Después, una instancia de se parece a la siguiente:


```
mytemp aTemp {
1, 2, 3;
}
```



En el ejemplo de matriz, no es necesario separar los elementos de datos con punto y coma, porque se delimitan mediante comas. El punto y coma al final marca el final de la matriz.

Considere una plantilla que contiene una matriz de elementos de datos definida por una plantilla.


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



Una instancia de esto sería similar al ejemplo siguiente.


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

 

 



