---
title: Stub-Allocated búferes
description: En lugar de forzar una llamada distinta para cada nodo del árbol o gráfico, puede dirigir los códigos auxiliares para calcular el tamaño de los datos y asignar y liberar memoria haciendo que una sola llamada al usuario midl asigne o al usuario medio sea \_ \_ \_ \_ libre.
ms.assetid: 9911649d-00e8-47d8-b512-7d9b185d1e09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956acf6452c1a4e7d04afcd1da263439436e3bad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071409"
---
# <a name="stub-allocated-buffers"></a>Stub-Allocated búferes

En lugar de forzar una llamada distinta para cada nodo del árbol o gráfico, puede dirigir los códigos auxiliares para calcular el tamaño de los datos y para asignar y liberar memoria haciendo una sola llamada a la asignación de usuario de nivel medio o al usuario [medio \_ \_ ](/windows/desktop/Midl/midl-user-free-1)libre. [ \_ \_ ](/windows/desktop/Midl/midl-user-allocate-1) El atributo ACF **\[ allocate (todos los \_ nodos) \]** dirige los códigos auxiliares para asignar o liberar todos los nodos en una sola llamada a las funciones de administración de memoria proporcionadas por el usuario.

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

El atributo ACF **\[ allocate(all \_ nodes) \]** aplicado a este tipo de datos aparece en la **declaración typedef** de ACF como:

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes)] P_TREE_TYPE;
```

El **\[ atributo allocate \]** solo se puede aplicar a los tipos de puntero. El **\[ atributo \]** allocate ACF es una extensión de Microsoft para DCE IDL y, como tal, no está disponible si se compila con el modificador MIDL **/osf.** Cuando **\[ se aplica allocate(all \_ nodes) \]** a un tipo de puntero, los códigos auxiliares generados por el compilador MIDL recorren la estructura de datos especificada para determinar el tamaño de asignación. A continuación, los códigos auxiliares hacen una sola llamada para asignar toda la cantidad de memoria necesaria para el gráfico o el árbol. Una aplicación cliente puede liberar memoria de forma mucho más eficaz mediante la realización de una sola llamada a **midl \_ user \_ free**. Sin embargo, el rendimiento del código auxiliar de servidor suele aumentar cuando se usa la asignación de memoria nodo a nodo, ya que los códigos auxiliares del servidor a menudo pueden usar memoria privada que no requiere asignaciones.

Para obtener más información, vea [Asignación y desasignación de nodo](node-by-node-allocation-and-deallocation.md)a nodo.

 

 