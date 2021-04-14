---
title: Depurar asignaciones de memoria
description: Depurar asignaciones de memoria
ms.assetid: 522adb1f-0e3e-4dfb-8836-f539a79a3d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb6a7dbe313cfe571fa6b4d244df35407fa331e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359437"
---
# <a name="debugging-memory-allocations"></a>Depurar asignaciones de memoria

COM proporciona la interfaz [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) para que los desarrolladores puedan usar para depurar las asignaciones de memoria. Para cada método de [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc), hay dos métodos en **IMallocSpy**, un método "pre" y un método "post". Después de que un desarrollador lo implemente y lo publique en el sistema, el sistema llama al método "pre" de **IMallocSpy** justo antes del método **IMalloc** correspondiente, permitiendo de forma eficaz el código de depuración a "Spy" en la operación de asignación y llama al método "post" para liberar el espía.

Por ejemplo, cuando COM detecta que la siguiente llamada es una llamada a [**IMalloc:: Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc), llama a [**IMallocSpy::P realloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc), ejecuta las operaciones de depuración que el desarrollador desea durante la ejecución de la **asignación** y, a continuación, cuando la llamada de **asignación** vuelve, llama a [**IMallocSpy::P ostalloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) para liberar el Spy y devolver el control al código.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrar la asignación de memoria](managing-memory-allocation.md)
</dt> </dl>

 

 