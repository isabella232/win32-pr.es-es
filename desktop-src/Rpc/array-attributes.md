---
title: Atributos de matriz
description: Hay una relación estrecha entre matrices y punteros en el lenguaje C.
ms.assetid: 0d65c993-63e4-42ae-ae24-6c19a71386a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba7bdaa08352a96987066313d4db074872f28b71ec0be0856a32522a849029c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073525"
---
# <a name="array-attributes"></a>Atributos de matriz

Hay una relación estrecha entre matrices y punteros en el lenguaje C. Cuando se pasa como un parámetro a una función, un nombre de matriz se trata como un puntero al primer elemento de la matriz, como se muestra en el ejemplo siguiente:


```C++
/* fragment */
extern void f1(char * p1);

void main(void)
{
    char chArray[MAXSIZE];

    fLocal1(chArray);
}
```



En una llamada local, puede usar el parámetro de puntero para pasar por la memoria y examinar el contenido de otras direcciones:


```C++
/* dump memory (fragment) */
void fLocal1(char * pch1)
{
    int i;

    for (i = 0; i < MAXSIZE; i++)
       printf("%c ", *pch1++);
}
```



Cuando un cliente pasa un puntero a un procedimiento remoto, el código auxiliar del cliente transmite tanto el puntero como los datos a los que apunta. A menos que el puntero esté restringido a sus datos correspondientes, toda la memoria del cliente debe transmitirse con cada llamada remota. Al aplicar la escritura fuerte en la definición de interfaz, MIDL limita el procesamiento de código auxiliar de cliente a los datos que corresponden al puntero especificado.

El tamaño de la matriz y el intervalo de elementos de matriz transmitidos al equipo remoto pueden ser constantes o variables. Cuando estos valores son variables y, por tanto, se determinan en tiempo de ejecución, debe usar atributos en el archivo IDL para especificar cuántos elementos de matriz transmitir. Los siguientes atributos MIDL admiten límites de matriz.



| Atributo                             | Descripción                                             | Valor predeterminado |
|---------------------------------------|---------------------------------------------------------|---------|
| \[[ **en primer \_ lugar es**](/windows/desktop/Midl/first-is)\]   | Índice del primer elemento de matriz transmitido.           | 0       |
| \[[ **el \_ último es**](/windows/desktop/Midl/last-is)\]     | Índice del último elemento de matriz transmitido.            | \-      |
| \[[ **length \_ es**](/windows/desktop/Midl/length-is)\] | Número total de elementos de matriz transmitidos.             | \-      |
| \[[ **max \_ is**](/windows/desktop/Midl/max-is)\]       | Valor de índice de matriz válido más alto.                        | \-      |
| \[[ **min \_ es**](/windows/desktop/Midl/min-is)\]       | Valor de índice de matriz válido más bajo.                         | 0       |
| \[[ **el \_ tamaño es**](/windows/desktop/Midl/size-is)\]     | Número total de elementos de matriz asignados para la matriz. | \-      |



 

> [!Note]  
> El **atributo \_ min is** no se implementa en RPC. El índice mínimo de la matriz siempre se trata como cero.

 

 

 