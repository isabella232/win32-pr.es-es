---
title: Punteros únicos
description: En los programas de C, más de un puntero puede contener la dirección de los datos.
ms.assetid: da4f466d-2c59-4e48-b6c5-1a49b933621a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc8cf9a45965c82416ec838f8598c2796ba621a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077788"
---
# <a name="unique-pointers"></a>Punteros únicos

En los programas de C, más de un puntero puede contener la dirección de los datos. Se dice que los punteros crean un [*alias*](a-glos.md) para los datos. Los alias también se crean cuando los punteros apuntan a variables declaradas. En el fragmento de código siguiente se muestran ambos métodos de alias:


```C++
int iAnInteger=50;

// The next statement makes ipAnIntegerPointer an
// alias for iAnInteger.
int *ipAnIntegerPointer = &iAnInteger;

// This statement creates an alias for ipAnIntegerPointer.
int *ipAnotherIntegerPointer = ipAnIntegerPointer;
```



En un programa de C típico, puede especificar un árbol binario con la siguiente definición:


```C++
typedef struct _treetype 
{
    long               lValue;
    struct _treetype * left;
    struct _treetype * right;
} TREETYPE;

TREETYPE * troot;
```



Más de un puntero puede tener acceso al contenido de un nodo de árbol. Normalmente, esto es correcto para las aplicaciones no distribuidas. Sin embargo, este estilo de programación genera código de compatibilidad con RPC más complicado. Los códigos auxiliares de cliente y servidor requieren el código adicional para administrar los datos y los punteros. El código auxiliar subyacente debe resolver los distintos punteros a las direcciones y determinar qué copia de los datos representan la versión más reciente.

Se puede reducir la cantidad de procesamiento si garantiza que el puntero es la única manera en que la aplicación puede tener acceso a ese área de memoria. El puntero puede seguir teniendo muchas de las características de un puntero de C. Por ejemplo, puede cambiar entre valores **null** y distintos de **null** o permanecer igual. Esto se ilustra en el siguiente ejemplo: El puntero es **null** antes de la llamada y apunta a una cadena válida después de la llamada:

![cambio de puntero entre valores NULL y no NULL](images/prog-a01.png)

De forma predeterminada, el compilador MIDL aplica el \[ [](/windows/desktop/Midl/unique) \] atributo de puntero único a todos los punteros que no son parámetros. Esta configuración predeterminada se puede cambiar con el \[ [atributo \_ default del puntero](/windows/desktop/Midl/pointer-default) \] .

Un puntero único tiene las siguientes características:

-   Puede tener el valor **null**.
-   Puede cambiar de **null** a un valor distinto de **null** durante la llamada. Cuando el valor cambia a no **null**, se asigna una nueva memoria al volver.
-   Puede cambiar de un valor distinto de **null** a **null** durante la llamada. Cuando el valor cambia a **null**, la aplicación es responsable de liberar memoria.
-   El valor puede cambiar de un valor distinto de **null** a otro.
-   No se puede tener acceso al almacenamiento al que apunta un puntero único en ningún otro puntero o nombre de la operación.
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

En este ejemplo, el parámetro *ACH* es un puntero único a los datos de caracteres que se envía a un servidor que se va a procesar con la rutina RemoteFn.

 

 