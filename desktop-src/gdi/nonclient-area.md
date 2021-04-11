---
description: El sistema envía un mensaje de WM \_ NCPAINT a la ventana cuando se debe actualizar una parte del área no cliente de la ventana, como la barra de título, la barra de menús o el marco de la ventana.
ms.assetid: e4dc61f3-6a9f-4ed4-8685-62eb4ceb85f1
title: Área no cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51da31709f5bd9326cc0d05a9e37e2df78bfbb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275992"
---
# <a name="nonclient-area"></a>Área no cliente

El sistema envía un mensaje de [**WM \_ NCPAINT**](wm-ncpaint.md) a la ventana cuando se debe actualizar una parte del área no cliente de la ventana, como la barra de título, la barra de menús o el marco de la ventana. El sistema también puede enviar otros mensajes para dirigir una ventana para actualizar una parte de su área de cliente. por ejemplo, cuando una ventana se activa o inactiva, envía el mensaje [**de \_ NCACTIVATE de WM**](../winmsg/wm-ncactivate.md) para actualizar la barra de título. En general, no se recomienda el procesamiento de estos mensajes para Windows estándar, ya que la aplicación debe ser capaz de dibujar todas las partes necesarias del área no cliente de la ventana. Por esta razón, la mayoría de las aplicaciones pasan estos mensajes a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para el procesamiento predeterminado.

Una aplicación que crea áreas no cliente personalizadas para sus ventanas debe procesar estos mensajes. Al hacerlo, la aplicación debe usar un contexto de dispositivo de ventana para realizar el dibujo en la ventana. El *contexto de dispositivo de ventana* permite que la aplicación dibuje en todas las partes de la ventana, incluido el área no cliente. Una aplicación recupera un contexto de dispositivo de ventana mediante la función [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) y, cuando se completa el dibujo, debe liberar el contexto de dispositivo de ventana mediante la función [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) .

El sistema mantiene una región de actualización para el área no cliente. Cuando una aplicación recibe un mensaje de [**\_ NCPAINT de WM**](wm-ncpaint.md) , el parámetro *wParam* contiene un identificador a una región que define las dimensiones de la región de actualización. La aplicación puede utilizar el identificador para combinar la región de actualización con la región de recorte para el contexto de dispositivo de ventana. El sistema no combina automáticamente la región de actualización al recuperar el contexto de dispositivo de ventana a menos que la aplicación use [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) y especifica el identificador de región y la \_ marca DCX INTERSECTRGN. Si la aplicación no combina la región de actualización, solo se recortan las operaciones de dibujo que, de otro modo, se extienden fuera de la ventana. La aplicación no es responsable de borrar la región de actualización, independientemente de si usa la región.

Si una aplicación procesa el mensaje de [**\_ NCACTIVATE de WM**](../winmsg/wm-ncactivate.md) , después del procesamiento debe devolver **true** para indicar al sistema que complete el cambio de la ventana activa. Si la ventana está minimizada cuando la aplicación recibe el mensaje de **\_ NCACTIVATE de WM** , debe pasar el mensaje a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). En tales casos, la función predeterminada vuelve a dibujar la etiqueta para el icono.

 

 
