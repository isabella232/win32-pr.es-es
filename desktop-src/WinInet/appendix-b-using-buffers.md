---
title: Usar búferes de cadena
description: Las funciones que devuelven cadenas contienen un parámetro de entrada, Lpszbuffer se, y un parámetro de tamaño, lpdwBufferLength. Aunque Lpszbuffer se puede ser NULL, lpdwBufferLength debe ser un puntero válido a una variable DWORD.
ms.assetid: ae7f84ba-15d4-483b-bdda-0042854f9e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 309d887458521b99069b381f8bf6650ebeda488a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792723"
---
# <a name="using-string-buffers"></a>Usar búferes de cadena

Las funciones que devuelven cadenas contienen un parámetro de entrada, *lpszbuffer se*, y un parámetro de tamaño, *lpdwBufferLength*. Aunque *lpszbuffer se* puede ser **null**, *lpdwBufferLength* debe ser un puntero válido a una variable **DWORD** . Si el búfer de entrada al que apunta *lpszbuffer se* es **null** o demasiado pequeño para contener la cadena de salida, se produce un error en la función y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un **error de \_ \_ búfer insuficiente**. La variable a la que apunta *lpdwBufferLength* contiene un número que representa el número de bytes que requiere la función para devolver la cadena solicitada, incluido el terminador **null** . La aplicación debe asignar un búfer de este tamaño, establecer la variable a la que apunta *lpdwBufferLength* en este valor y volver a enviar la solicitud. Si el tamaño del búfer es suficiente para recibir la cadena solicitada, la cadena se copia en el búfer de salida con un terminador **null** y la función devuelve una indicación de éxito. La variable a la que apunta *lpdwBufferLength* ahora contiene el número de caracteres almacenados en el búfer, sin incluir el terminador **null** .

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 