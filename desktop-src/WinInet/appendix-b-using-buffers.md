---
title: Uso de búferes de cadena
description: Las funciones que devuelven cadenas contienen un parámetro de entrada, lpszBuffer y un parámetro de tamaño, lpdwBufferLength. Aunque lpszBuffer puede ser NULL, lpdwBufferLength debe ser un puntero válido a una variable DWORD.
ms.assetid: ae7f84ba-15d4-483b-bdda-0042854f9e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 309d887458521b99069b381f8bf6650ebeda488a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568144"
---
# <a name="using-string-buffers"></a>Uso de búferes de cadena

Las funciones que devuelven cadenas contienen un parámetro de entrada, *lpszBuffer* y un parámetro de tamaño, *lpdwBufferLength*. Aunque *lpszBuffer puede* ser **NULL,** *lpdwBufferLength* debe ser un puntero válido a una variable **DWORD.** Si el búfer de entrada al que *apunta lpszBuffer* es **NULL** o es demasiado pequeño para contener la cadena de salida, se produce un error en la función y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve **ERROR INSUFFICIENT \_ \_ BUFFER**. La variable a la que *apunta lpdwBufferLength* contiene un número que representa el número de bytes que requiere la función para devolver la cadena solicitada, incluido el **terminador** nulo. La aplicación debe asignar un búfer de este tamaño, establecer la variable a la que *apunta lpdwBufferLength* en este valor y volver a enviar la solicitud. Si el tamaño del búfer es suficiente para recibir la cadena solicitada, la cadena se copia en el búfer de salida con un **terminador** nulo y la función devuelve una indicación de éxito. La variable a la que *apunta lpdwBufferLength* ahora contiene el número de caracteres almacenados en el búfer, sin incluir **el** terminador nulo.

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para las implementaciones de servidor o los servicios, use [Microsoft Windows SERVICIOS HTTP (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 