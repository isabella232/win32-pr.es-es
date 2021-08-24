---
description: Cada presentación física se representa mediante un identificador de monitor de tipo HMONITOR.
ms.assetid: c43c1401-52d3-485e-a418-205df5737040
title: HMONITOR y el contexto del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afb727457c388710b19d8f22bef8f65d76e9d8c5c27b0ec7dfcbf55a4acea3b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558755"
---
# <a name="hmonitor-and-the-device-context"></a>HMONITOR y el contexto del dispositivo

Cada presentación física se representa mediante un identificador de monitor de tipo **HMONITOR**. Se garantiza **que un HMONITOR** válido no sea NULL. Una pantalla física tiene el mismo **HMONITOR** siempre que sea parte del escritorio. Cuando se **envía un mensaje \_ DISPLAYCHANGE** de WM, se puede quitar cualquier monitor del escritorio y, por tanto, **su HMONITOR** deja de ser válido o cambia su configuración. Por lo tanto, una aplicación debe comprobar si **todos los HMONITORS** son válidos cuando se envía este mensaje.

Cualquier función que devuelve un contexto de dispositivo de presentación (DC) normalmente devuelve un controlador de dominio para el monitor principal. Para obtener el controlador de dominio de otro monitor, use la [**función EnumDisplayMonitors.**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) O bien, puede usar el nombre del dispositivo de la [**función GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) para crear un controlador de dominio con [**CreateDC.**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) Sin embargo, si la función, como [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) o [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), obtiene un controlador de dominio para una ventana que abarca más de una pantalla, el controlador de dominio también abarcará las dos pantallas.

 

 



