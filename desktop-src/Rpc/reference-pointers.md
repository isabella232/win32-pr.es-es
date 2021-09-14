---
title: Punteros de referencia
description: Los punteros de referencia son los punteros más sencillos y requieren la menor cantidad de procesamiento por parte del código auxiliar del cliente.
ms.assetid: 393aec84-8e8f-41b9-956f-d28a80d3a8c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427605f330b1a73c541c95019f8ca4bdd6cc8ef4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361905"
---
# <a name="reference-pointers"></a>Punteros de referencia

Los punteros de referencia son los punteros más sencillos y requieren la menor cantidad de procesamiento por parte del código auxiliar del cliente. Cuando un programa cliente pasa un puntero de referencia a un procedimiento remoto, el puntero de referencia siempre contiene la dirección de un bloque de memoria válido. Seguirá apuntando al mismo bloque de memoria cuando se complete el procedimiento remoto. Estos punteros se usan principalmente para implementar la semántica de referencia y para permitir parámetros \[ [**out**](/windows/desktop/Midl/out-idl) \] en C.

En el ejemplo siguiente, el valor del puntero no cambia durante la llamada, aunque el contenido de los datos en la dirección indicada por el puntero puede cambiar.

![cambio de datos en una dirección de puntero de referencia estática](images/prog-a07.png)

Un puntero de referencia tiene las siguientes características:

-   Siempre apunta al almacenamiento válido y nunca tiene el valor **NULL.**
-   Nunca cambia durante una llamada y siempre apunta al mismo almacenamiento antes y después de la llamada.
-   Los datos devueltos por el procedimiento remoto se escriben en el almacenamiento existente.
-   Ningún otro puntero o cualquier otro nombre de la función puede tener acceso al almacenamiento al que apunta un puntero de referencia.

Use el \[ [**atributo ref**](/windows/desktop/Midl/ref) \] para especificar punteros de referencia en definiciones de interfaz, como se muestra en el ejemplo siguiente.

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, out, ref] char *pChar);
}
```

En este ejemplo se define el *parámetro pChar* como puntero a un solo carácter, no a una matriz de caracteres. Es un parámetro out y un puntero de referencia que apunta a la memoria que la rutina de servidor \[  \] RemoteFn rellenará con datos.

 

 