---
title: Búferes Stub-Allocated
description: En lugar de forzar una llamada DISTINCT para cada nodo del árbol o gráfico, puede dirigir el código auxiliar para calcular el tamaño de los datos y asignar y liberar memoria realizando una única llamada a la asignación de usuarios de MIDL o a la versión de \_ \_ usuario de MIDL \_ \_ .
ms.assetid: 9911649d-00e8-47d8-b512-7d9b185d1e09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956acf6452c1a4e7d04afcd1da263439436e3bad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078096"
---
# <a name="stub-allocated-buffers"></a>Búferes Stub-Allocated

En lugar de forzar una llamada DISTINCT para cada nodo del árbol o gráfico, puede dirigir el código auxiliar para calcular el tamaño de los datos y asignar y liberar memoria realizando una única llamada a la [ \_ \_ asignación de usuarios de MIDL](/windows/desktop/Midl/midl-user-allocate-1) o a la versión de [usuario de MIDL \_ \_ ](/windows/desktop/Midl/midl-user-free-1). El atributo ACF **\[ allocate (todos los \_ nodos) \]** dirige el código auxiliar para asignar o liberar todos los nodos en una sola llamada a las funciones de administración de memoria proporcionadas por el usuario.

Por ejemplo, una aplicación RPC podría usar la siguiente estructura de datos de árbol binario:

``` syntax
/* IDL file fragment */
typedef struct _TREE_TYPE 
{
    short sNumber;
    struct _TREE_TYPE * pLeft;
    struct _TREE_TYPE * pRight;
} TREE_TYPE;

typedef TREE_TYPE * P_TREE_TYPE;
```

El atributo ACF **\[ allocate (todos los \_ nodos) \]** aplicado a este tipo de datos aparece en la declaración **typedef** en el ACF como:

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes)] P_TREE_TYPE;
```

El atributo **\[ allocate \]** solo se puede aplicar a los tipos de puntero. El atributo **\[ allocate \]** ACF es una extensión de Microsoft para DCE IDL y, como tal, no está disponible si se compila con el modificador **/OSF** de MIDL. Cuando se aplica la **\[ asignación (todos los \_ nodos) \]** a un tipo de puntero, el código auxiliar generado por el compilador MIDL atraviesa la estructura de datos especificada para determinar el tamaño de asignación. Después, el código auxiliar realiza una llamada única para asignar toda la cantidad de memoria que necesita el gráfico o el árbol. Una aplicación cliente puede liberar memoria de forma mucho más eficaz si realiza una única llamada a la versión **\_ \_ gratuita del usuario de MIDL**. Sin embargo, el rendimiento del código auxiliar del servidor suele aumentar cuando se usa la asignación de memoria de nodo por nodo, ya que el código auxiliar del servidor a menudo puede usar la memoria privada que no requiere asignaciones.

Para obtener más información, consulte [asignación y desasignación de nodo por nodo](node-by-node-allocation-and-deallocation.md).

 

 