---
title: Punteros completos
description: A diferencia de los punteros únicos, los punteros completos admiten el alias.
ms.assetid: 38023942-a4c2-4de7-b7d5-10d508cf083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18687b496ddd28dca9e70afca8deafb18774500a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995359"
---
# <a name="full-pointers"></a>Punteros completos

A diferencia de los punteros [únicos](unique-pointers.md) , los punteros completos admiten el alias. Esto significa que varios punteros pueden hacer referencia a los mismos datos, tal y como se muestra en la ilustración siguiente:

![dos punteros que hacen referencia a los mismos datos](images/prog-a02.png)

Un puntero completo tiene las siguientes características:

-   Puede tener el valor null.
-   Puede cambiar de null a un valor distinto de NULL durante la llamada. Cuando el valor cambia a un valor distinto de NULL, el código auxiliar del cliente asigna una nueva memoria asignada en la devolución. El programa cliente debe liberar esta memoria antes de que finalice.
-   Puede cambiar de un valor distinto de null a NULL durante la llamada. Cuando el valor cambia a NULL, la aplicación es responsable de liberar memoria.
-   El valor puede cambiar de un valor distinto de null a otro.
-   El almacenamiento al que apunta un puntero completo puede ser accesible por otro puntero o nombre de la operación.
-   Los datos devueltos se escriben en el almacenamiento existente si el puntero no tiene el valor null.

Utilice el \[ [](/windows/desktop/Midl/ptr) \] atributo PTR para especificar un puntero completo, tal como se muestra en el ejemplo siguiente:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface FullPtrInterface
{
  void RemoteFn([in,ptr,string]) char *ptrName1,
                [in,ptr,string]  char *ptrName2);
}
```

En este ejemplo, los parámetros *ptrName1* y *ptrName2* se definen como punteros completos a una cadena. Es posible que ambos punteros señalen a la misma dirección de memoria que contiene una sola cadena.

\[**ptr** \] se requiere cuando se proporciona compatibilidad con los alias. Sin embargo, puesto que requiere la mayor parte del procesamiento de todos los punteros disponibles en RPC, no se recomienda para la mayoría de las aplicaciones.

 

 