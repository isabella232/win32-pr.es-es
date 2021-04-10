---
title: Asignador de memoria OLE
description: Asignador de memoria OLE
ms.assetid: 026c62e5-c296-4059-b028-77c98fdb77ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64fedd610fd8fd6dab0bcd14deb37e04f6df74d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149652"
---
# <a name="the-ole-memory-allocator"></a>Asignador de memoria OLE

La biblioteca COM proporciona una implementación de un asignador de memoria que es segura para subprocesos. (Es decir, no puede producir problemas en situaciones multiproceso). Siempre que la propiedad de un fragmento de memoria asignado se pasa a través de una interfaz COM o entre un cliente y la biblioteca COM, debe utilizar este asignador COM para asignar la memoria. La asignación interna a un objeto puede usar cualquier esquema de asignación deseado, pero el asignador de memoria COM es un asignador práctico, eficaz y seguro para subprocesos.

Una llamada a la función de API [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) proporciona un puntero al asignador OLE, que es una implementación de la interfaz [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) . Sin embargo, es más eficaz llamar a las funciones auxiliares de [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**CoTaskMemRealloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc)y [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree), que encapsulan la obtención de un puntero al asignador de memoria de la tarea, llamando al método **IMalloc** correspondiente y, a continuación, liberando el puntero al asignador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrar la asignación de memoria](managing-memory-allocation.md)
</dt> <dt>

[Biblioteca COM](the-com-library.md)
</dt> </dl>

 

 