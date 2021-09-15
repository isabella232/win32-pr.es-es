---
description: El sistema envía un mensaje WM NCPAINT a la ventana cada vez que se debe actualizar una parte del área no cliente de la ventana, como la barra de título, la barra de menús o el marco \_ de ventana.
ms.assetid: e4dc61f3-6a9f-4ed4-8685-62eb4ceb85f1
title: Área no cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51da31709f5bd9326cc0d05a9e37e2df78bfbb4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127475920"
---
# <a name="nonclient-area"></a>Área no cliente

El sistema envía un mensaje [**\_ WM NCPAINT**](wm-ncpaint.md) a la ventana cada vez que se debe actualizar una parte del área no cliente de la ventana, como la barra de título, la barra de menús o el marco de ventana. El sistema también puede enviar otros mensajes para dirigir una ventana para actualizar una parte de su área cliente. Por ejemplo, cuando una ventana se activa o está inactiva, envía el mensaje [**\_ WM NCACTIVATE**](../winmsg/wm-ncactivate.md) para actualizar su barra de título. En general, no se recomienda procesar estos mensajes para ventanas estándar, ya que la aplicación debe poder dibujar todas las partes necesarias del área no cliente para la ventana. Por este motivo, la mayoría de las aplicaciones pasan estos mensajes [**a DefWindowProc para**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) su procesamiento predeterminado.

Una aplicación que crea áreas no cliente personalizadas para sus ventanas debe procesar estos mensajes. Al hacerlo, la aplicación debe usar un contexto de dispositivo de ventana para llevar a cabo el dibujo en la ventana. El *contexto del dispositivo de* ventana permite que la aplicación dibuje en todas las partes de la ventana, incluido el área no cliente. Una aplicación recupera un contexto de dispositivo de ventana mediante la función [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) y, cuando se completa el dibujo, debe liberar el contexto del dispositivo de ventana mediante la [**función ReleaseDC.**](/windows/desktop/api/Winuser/nf-winuser-releasedc)

El sistema mantiene una región de actualización para el área no cliente. Cuando una aplicación recibe un [**mensaje \_ WM NCPAINT,**](wm-ncpaint.md) el parámetro *wParam* contiene un identificador para una región que define las dimensiones de la región de actualización. La aplicación puede usar el identificador para combinar la región de actualización con la región de recorte para el contexto del dispositivo de ventana. El sistema no combina automáticamente la región de actualización al recuperar el contexto del dispositivo de ventana a menos que la aplicación use [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) y especifique tanto el identificador de región como la marca \_ INTERSECTRGN de DCX. Si la aplicación no combina la región de actualización, solo se recortan las operaciones de dibujo que, de lo contrario, se extenderían fuera de la ventana. La aplicación no es responsable de borrar la región de actualización, independientemente de si usa la región.

Si una aplicación procesa el [**mensaje \_ WM NCACTIVATE,**](../winmsg/wm-ncactivate.md) después de procesarlo, debe devolver **TRUE** para dirigir al sistema a completar el cambio de ventana activa. Si la ventana se minimiza cuando la aplicación recibe el mensaje **\_ WM NCACTIVATE,** debe pasar el mensaje [**a DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). En tales casos, la función predeterminada vuelve a dibujar la etiqueta del icono.

 

 
