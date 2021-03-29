---
title: Atributos de matriz
description: Hay una relación de cierre entre las matrices y los punteros en el lenguaje C.
ms.assetid: 0d65c993-63e4-42ae-ae24-6c19a71386a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ed669a2a81528afa84b41a1be25a0c84f70fbe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793227"
---
# <a name="array-attributes"></a>Atributos de matriz

Hay una relación de cierre entre las matrices y los punteros en el lenguaje C. Cuando se pasa como un parámetro a una función, el nombre de una matriz se trata como un puntero al primer elemento de la matriz, como se muestra en el ejemplo siguiente:


```C++
/* fragment */
extern void f1(char * p1);

void main(void)
{
    char chArray[MAXSIZE];

    fLocal1(chArray);
}
```



En una llamada local, puede usar el parámetro de puntero a marzo a través de la memoria y examinar el contenido de otras direcciones:


```C++
/* dump memory (fragment) */
void fLocal1(char * pch1)
{
    int i;

    for (i = 0; i < MAXSIZE; i++)
       printf("%c ", *pch1++);
}
```



Cuando un cliente pasa un puntero a un procedimiento remoto, el código auxiliar del cliente transmite el puntero y los datos a los que señala. A menos que el puntero esté restringido a sus datos correspondientes, toda la memoria del cliente se debe transmitir con cada llamada remota. Al exigir un establecimiento de tipos seguros en la definición de interfaz, MIDL limita el procesamiento de código auxiliar de cliente a los datos correspondientes al puntero especificado.

El tamaño de la matriz y el intervalo de elementos de la matriz transmitidos al equipo remoto pueden ser constantes o variables. Cuando estos valores son variables y, por tanto, se determinan en tiempo de ejecución, debe utilizar atributos en el archivo IDL para especificar el número de elementos de matriz que se van a transmitir. Los siguientes atributos de MIDL admiten límites de matriz.



| Atributo                             | Descripción                                             | Valor predeterminado |
|---------------------------------------|---------------------------------------------------------|---------|
| \[el [ **primero \_ es**](/windows/desktop/Midl/first-is)\]   | Índice del primer elemento de la matriz transmitido.           | 0       |
| \[[ **última \_ es**](/windows/desktop/Midl/last-is)\]     | Índice del último elemento de la matriz transmitido.            | \-      |
| \[la [ **longitud \_ es**](/windows/desktop/Midl/length-is)\] | Número total de elementos de matriz transmitidos.             | \-      |
| \[[ **Max \_ es**](/windows/desktop/Midl/max-is)\]       | Valor de índice de matriz válido más alto.                        | \-      |
| \[[ **min \_ es**](/windows/desktop/Midl/min-is)\]       | Valor de índice de matriz válido más bajo.                         | 0       |
| \[[ **el tamaño \_ es**](/windows/desktop/Midl/size-is)\]     | Número total de elementos de matriz asignados a la matriz. | \-      |



 

> [!Note]  
> El atributo **min \_ is** no se implementa en RPC. El índice mínimo de la matriz siempre se trata como cero.

 

 

 