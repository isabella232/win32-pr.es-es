---
title: Asignación de memoria en COM
description: .
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62227f78287f184b019eee3e498ec8a25f25a03c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105685706"
---
# <a name="memory-allocation-in-com"></a>Asignación de memoria en COM

A veces, un método asigna un búfer de memoria en el montón y devuelve la dirección del búfer al llamador. COM define un par de funciones para asignar y liberar memoria en el montón.

-   La función [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) asigna un bloque de memoria.
-   La función [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) libera un bloque de memoria que se asignó con [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).

Vimos un ejemplo de este patrón en el [ejemplo de cuadro de diálogo Abrir](example--the-open-dialog-box.md):


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



El método [**getDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) asigna memoria para una cadena. Internamente, el método llama a [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) para asignar la cadena. Cuando el método devuelve, *pszFilePath* apunta a la ubicación de memoria del nuevo búfer. El autor de la llamada es responsable de llamar a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar memoria.

¿Por qué COM define sus propias funciones de asignación de memoria? Una razón es proporcionar una capa de abstracción sobre el asignador del montón. De lo contrario, algunos métodos podrían llamar a **malloc** mientras que otros llamados **New**. Después, el programa tendría que llamar a **Free** en algunos casos y **eliminar** en otros, y realizar un seguimiento de todo lo haría rápidamente. Las funciones de asignación COM crean un enfoque uniforme.

Otro aspecto que se debe tener en cuenta es el hecho de que COM es un estándar *binario* , por lo que no está asociado a un lenguaje de programación determinado. Por lo tanto, COM no puede depender de ninguna forma específica del lenguaje de asignación de memoria.

## <a name="next"></a>Siguientes

[Prácticas de codificación COM](com-coding-practices.md)

 

 