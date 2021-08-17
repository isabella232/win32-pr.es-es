---
title: Asignación de memoria en COM
description: Asignación de memoria en COM
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a38477f0db860cf768493417470f2da3395e814bc106cf85f975ed11ba2c0b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979985"
---
# <a name="memory-allocation-in-com"></a>Asignación de memoria en COM

A veces, un método asigna un búfer de memoria en el montón y devuelve la dirección del búfer al autor de la llamada. COM define un par de funciones para asignar y liberar memoria en el montón.

-   La [**función CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) asigna un bloque de memoria.
-   La [**función CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) libera un bloque de memoria que se asignó [**con CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).

Vimos un ejemplo de este patrón en el ejemplo [de cuadro de diálogo Abrir](example--the-open-dialog-box.md):


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



El [**método GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) asigna memoria para una cadena. Internamente, el método llama [**a CoTaskMemAlloc para**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) asignar la cadena. Cuando el método vuelve, *pszFilePath* apunta a la ubicación de memoria del nuevo búfer. El autor de la llamada es responsable de [**llamar a CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria.

¿Por qué COM define sus propias funciones de asignación de memoria? Una razón es proporcionar una capa de abstracción sobre el asignador del montón. De lo contrario, algunos métodos podrían llamar **a malloc** mientras que otros **llamaron a new**. A continuación, el programa tendría  que llamar a **free** en algunos casos y eliminar en otros, y realizar un seguimiento de todo esto rápidamente resultaría imposible. Las funciones de asignación COM crean un enfoque uniforme.

Otra consideración es el hecho de que COM es *un estándar* binario, por lo que no está vinculado a un lenguaje de programación determinado. Por lo tanto, COM no puede basarse en ninguna forma específica del lenguaje de asignación de memoria.

## <a name="next"></a>Siguientes

[Prácticas de codificación COM](com-coding-practices.md)

 

 
