---
title: Asignador de memoria OLE
description: Asignador de memoria OLE
ms.assetid: 026c62e5-c296-4059-b028-77c98fdb77ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64fedd610fd8fd6dab0bcd14deb37e04f6df74d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253095"
---
# <a name="the-ole-memory-allocator"></a>Asignador de memoria OLE

La biblioteca COM proporciona una implementación de un asignador de memoria que es seguro para subprocesos. (Es decir, no puede causar problemas en situaciones multiproceso). Siempre que la propiedad de un fragmento de memoria asignado se pasa a través de una interfaz COM o entre un cliente y la biblioteca COM, debe usar este asignador COM para asignar la memoria. La asignación interna a un objeto puede usar cualquier esquema de asignación deseado, pero el asignador de memoria COM es un asignador práctico, eficaz y seguro para subprocesos.

Una llamada a la función de API [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) proporciona un puntero al asignador OLE, que es una implementación de la [**interfaz IMalloc.**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) Sin embargo, es más eficaz llamar a las funciones auxiliares [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**CoTaskMemRealloc y**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc) [**CoTaskMemFree,**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)que encapsulan la obtención de un puntero al asignador de memoria de tareas, la llamada al método **IMalloc correspondiente** y, a continuación, la liberación del puntero al asignador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de la asignación de memoria](managing-memory-allocation.md)
</dt> <dt>

[La biblioteca COM](the-com-library.md)
</dt> </dl>

 

 