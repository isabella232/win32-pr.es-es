---
title: Punteros completos
description: A diferencia de los punteros únicos, los punteros completos admiten alias.
ms.assetid: 38023942-a4c2-4de7-b7d5-10d508cf083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18687b496ddd28dca9e70afca8deafb18774500a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361936"
---
# <a name="full-pointers"></a>Punteros completos

A [diferencia de](unique-pointers.md) los punteros únicos, los punteros completos admiten alias. Esto significa que varios punteros pueden hacer referencia a los mismos datos, como se muestra en la ilustración siguiente:

![dos punteros que hacen referencia a los mismos datos](images/prog-a02.png)

Un puntero completo tiene las siguientes características:

-   Puede tener el valor NULL.
-   Puede cambiar de null a non-null durante la llamada. Cuando el valor cambia a distinto de NULL, el código auxiliar del cliente asigna nueva memoria asignada en la devolución. El programa cliente debe liberar esta memoria antes de finalizar.
-   Puede cambiar de distinto de NULL a NULL durante la llamada. Cuando el valor cambia a NULL, la aplicación es responsable de liberar la memoria.
-   El valor puede cambiar de un valor distinto de NULL a otro.
-   Otro puntero o nombre de la operación puede tener acceso al almacenamiento al que apunta un puntero completo.
-   Los datos devueltos se escriben en el almacenamiento existente si el puntero no tiene el valor NULL.

Use el \[ [**atributo ptr**](/windows/desktop/Midl/ptr) \] para especificar un puntero completo, como se muestra en el ejemplo siguiente:

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

En este ejemplo, los *parámetros ptrName1* y *ptrName2* se definen como punteros completos a una cadena. Ambos punteros pueden apuntar a la misma dirección de memoria que contiene una sola cadena.

\[**ptr** \] es necesario al proporcionar compatibilidad con alias. Sin embargo, dado que requiere el mayor procesamiento de todos los punteros disponibles en RPC, no se recomienda para la mayoría de las aplicaciones.

 

 