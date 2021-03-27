---
description: Cada pantalla física se representa mediante un identificador de monitor de tipo HMONITOR.
ms.assetid: c43c1401-52d3-485e-a418-205df5737040
title: HMONITOR y el contexto del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da397af45b906a626f79f7b934b78aaad481f9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997357"
---
# <a name="hmonitor-and-the-device-context"></a>HMONITOR y el contexto del dispositivo

Cada pantalla física se representa mediante un identificador de monitor de tipo **HMONITOR**. Se garantiza que un **HMONITOR** válido no es NULL. Una pantalla física tiene el mismo **HMONITOR** siempre que forme parte del escritorio. Cuando se envía un mensaje de **\_ DISPLAYCHANGE de WM** , es posible que se quite cualquier monitor del escritorio y, por tanto, su **HMONITOR** deje de ser válido o se cambiara su configuración. Por lo tanto, una aplicación debe comprobar si todos los **HMONITORS** son válidos cuando se envía este mensaje.

Cualquier función que devuelva un contexto de dispositivo de pantalla (DC) suele devolver un controlador de dominio para el monitor principal. Para obtener el controlador de dominio para otro monitor, utilice la función [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) . O bien, puede usar el nombre del dispositivo de la función [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) para crear un controlador de dominio con [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca). Sin embargo, si la función, como [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) o [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), obtiene un controlador de dominio para una ventana que abarca más de una pantalla, el controlador de dominio también abarcará las dos pantallas.

 

 



