---
title: Punteros únicos
description: En los programas de C, más de un puntero puede contener la dirección de los datos.
ms.assetid: da4f466d-2c59-4e48-b6c5-1a49b933621a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc8cf9a45965c82416ec838f8598c2796ba621a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071384"
---
# <a name="unique-pointers"></a>Punteros únicos

En los programas de C, más de un puntero puede contener la dirección de los datos. Se dice que los punteros crean un [*alias*](a-glos.md) para los datos. Los alias también se crean cuando los punteros apuntan a variables declaradas. En el fragmento de código siguiente se ilustran ambos métodos de alias:


```C++
int iAnInteger=50;

// The next statement makes ipAnIntegerPointer an
// alias for iAnInteger.
int *ipAnIntegerPointer = &iAnInteger;

// This statement creates an alias for ipAnIntegerPointer.
int *ipAnotherIntegerPointer = ipAnIntegerPointer;
```



En un programa típico de C, puede especificar un árbol binario con la siguiente definición:


```C++
typedef struct _treetype 
{
    long               lValue;
    struct _treetype * left;
    struct _treetype * right;
} TREETYPE;

TREETYPE * troot;
```



Más de un puntero puede tener acceso al contenido de un nodo de árbol. Por lo general, esto es bueno para las aplicaciones no desdistribuida. Sin embargo, este estilo de programación genera código de compatibilidad rpc más complicado. Los códigos auxiliares de cliente y servidor requieren el código adicional para administrar los datos y los punteros. El código auxiliar subyacente debe resolver los distintos punteros a las direcciones y determinar qué copia de los datos representa la versión más reciente.

La cantidad de procesamiento se puede reducir si se garantiza que el puntero es la única manera en que la aplicación puede acceder a esa área de memoria. El puntero todavía puede tener muchas de las características de un puntero de C. Por ejemplo, puede cambiar entre valores **NULL** y no **NULL** o permanecer igual. Esto se ilustra en el siguiente ejemplo: El puntero es **NULL antes** de la llamada y apunta a una cadena válida después de la llamada:

![cambio de puntero entre valores null y no NULL](images/prog-a01.png)

De forma predeterminada, el compilador midl aplica el \[ [atributo de](/windows/desktop/Midl/unique) \] puntero único a todos los punteros que no son parámetros. Esta configuración predeterminada se puede cambiar con el \[ [atributo predeterminado \_ del](/windows/desktop/Midl/pointer-default) \] puntero.

Un puntero único tiene las siguientes características:

-   Puede tener el valor **null**.
-   Puede cambiar de **null a** **non-null** durante la llamada. Cuando el valor cambia a un valor distinto de **NULL,** se asigna nueva memoria a la devolución.
-   Puede cambiar de no **NULL** a **NULL** durante la llamada. Cuando el valor cambia a **NULL,** la aplicación es responsable de liberar la memoria.
-   El valor puede cambiar de un valor distinto de **NULL** a otro.
-   No se puede acceder al almacenamiento al que apunta un puntero único ningún otro puntero o nombre de la operación.
-   Los datos devueltos se escriben en el almacenamiento existente si el puntero no tiene el valor **null**.

En el ejemplo siguiente se muestra cómo definir un puntero único.

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, unique] char *ach);
}
```

En este ejemplo, el parámetro *ach* es un puntero único a los datos de caracteres que se envían a un servidor para procesarse con la rutina RemoteFn.

 

 