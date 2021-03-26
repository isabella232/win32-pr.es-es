---
description: Las siguientes funciones se usan con contextos de dispositivo.
ms.assetid: 9ff68d16-0f27-4cc8-932a-b2063cfed135
title: Funciones de contexto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 625b81b999526d84af4b58f2dddbc280643bcd35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811995"
---
# <a name="device-context-functions"></a>Funciones de contexto de dispositivo

Las siguientes funciones se usan con contextos de dispositivo.



| Función                                                   | Descripción                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc)                               | Cancela cualquier operación pendiente en el contexto de dispositivo especificado.                                                                            |
| [**ChangeDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsa)     | Cambia la configuración del dispositivo de pantalla predeterminado al modo gráfico especificado.                                                        |
| [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) | Cambia la configuración del dispositivo de pantalla especificado al modo gráfico especificado.                                                      |
| [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)           | Crea un contexto de dispositivo de memoria compatible con el dispositivo especificado.                                                                     |
| [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)                               | Crea un contexto de dispositivo para un dispositivo con el nombre especificado.                                                                           |
| [**Crear**](/windows/desktop/api/Wingdi/nf-wingdi-createica)                               | Crea un contexto de información para el dispositivo especificado.                                                                                  |
| [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc)                               | Elimina el contexto de dispositivo especificado.                                                                                                     |
| [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject)                       | Elimina un lápiz lógico, un pincel, una fuente, un mapa de bits, una región o una paleta, liberando todos los recursos del sistema asociados al objeto.                  |
| [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa)           | Recupera las capacidades de un controlador de dispositivo de impresora.                                                                                    |
| [**DrawEscape**](/windows/desktop/api/Wingdi/nf-wingdi-drawescape)                           | Proporciona funciones de dibujo de la pantalla de vídeo especificada que no están directamente disponibles a través de la interfaz de dispositivo gráfico.       |
| [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa)           | Recupera información acerca de los dispositivos de pantalla de un sistema.                                                                              |
| [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa)         | Recupera información sobre uno de los modos gráficos para un dispositivo de pantalla.                                                               |
| [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa)     | Recupera información sobre uno de los modos gráficos para un dispositivo de pantalla.                                                               |
| [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects)                         | Enumera los lápices o pinceles disponibles para el contexto de dispositivo especificado.                                                                |
| [**EnumObjectsProc**](/windows/win32/api/wingdi/nc-wingdi-gobjenumproc)                 | Función de devolución de llamada definida por la aplicación que se usa con la función [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) .                                       |
| [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject)               | Recupera un identificador de un objeto del tipo especificado que se ha seleccionado en el contexto de dispositivo especificado.                           |
| [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)                                     | Recupera un identificador de un contexto de dispositivo de pantalla para el área de cliente de una ventana especificada o para toda la pantalla.                        |
| [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)                 | Recupera el color de pincel actual para el contexto de dispositivo especificado.                                                                       |
| [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)                                 | Recupera un identificador de un contexto de dispositivo de pantalla para el área de cliente de una ventana especificada o para toda la pantalla.                        |
| [**GetDCOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getdcorgex)                           | Recupera el origen de traducción final para un contexto de dispositivo especificado.                                                                    |
| [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)                     | Recupera el color actual del lápiz para el contexto de dispositivo especificado.                                                                         |
| [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps)                     | Recupera información específica del dispositivo para el dispositivo especificado.                                                                           |
| [**GetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout)                             | Recupera el diseño de un contexto de dispositivo.                                                                                                 |
| [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject)                             | Recupera información para el objeto Graphics especificado.                                                                                  |
| [**GetObjectType**](/windows/desktop/api/Wingdi/nf-wingdi-getobjecttype)                     | Recupera el tipo del objeto especificado.                                                                                               |
| [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject)                   | Recupera un identificador de uno de los lápices, pinceles, fuentes o paletas de acciones.                                                                 |
| [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc)                             | Libera un contexto de dispositivo y lo libera para que lo usen otras aplicaciones.                                                                      |
| [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)                                 | Actualiza el contexto de dispositivo de impresora o de trazador especificado usando la información especificada.                                                  |
| [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)                             | Restaura el contexto de un dispositivo al estado especificado.                                                                                         |
| [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc)                                   | Guarda el estado actual del contexto de dispositivo especificado copiando los datos que describen los objetos y modos gráficos seleccionados en una pila de contexto. |
| [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)                       | Selecciona un objeto en el contexto de dispositivo especificado.                                                                                      |
| [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | Establece el color del pincel de contexto del dispositivo actual en el valor de color especificado.                                                                 |
| [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)                     | Establece el color del lápiz de contexto del dispositivo actual en el valor de color especificado.                                                                   |
| [**SetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout)                             | Establece el diseño de un contexto de dispositivo.                                                                                                     |
| [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc)                       | Devuelve un identificador a la ventana asociada a un contexto de dispositivo.                                                                          |



 

 

 
