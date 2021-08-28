---
title: Depuración de asignaciones de memoria
description: Depuración de asignaciones de memoria
ms.assetid: 522adb1f-0e3e-4dfb-8836-f539a79a3d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae81b3376b2ffee17ce747197eb57fecbdae18e086d5252dd5f4721975181885
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993455"
---
# <a name="debugging-memory-allocations"></a>Depuración de asignaciones de memoria

COM proporciona la [**interfaz IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) que los desarrolladores pueden usar para depurar sus asignaciones de memoria. Para cada método de [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc), hay dos métodos en **IMallocSpy,** un método "pre" y un método "post". Después de que un desarrollador lo implementa y lo publica en el sistema, el sistema llama al método "pre" de **IMallocSpy** justo antes del método **IMalloc** correspondiente, lo que permite eficazmente que el código de depuración "spy" en la operación de asignación y llama al método "post" para liberar el spy.

Por ejemplo, cuando COM detecta que la siguiente llamada es una llamada a [**IMalloc::Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc), llama a [**IMallocSpy::P reAlloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc), ejecutando las operaciones de depuración que el desarrollador desea durante la ejecución de **Alloc** y, a continuación, cuando se devuelve la llamada a **Alloc,** llama a [**IMallocSpy::P ostAlloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) para liberar el spy y devolver el control al código.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de la asignación de memoria](managing-memory-allocation.md)
</dt> </dl>

 

 