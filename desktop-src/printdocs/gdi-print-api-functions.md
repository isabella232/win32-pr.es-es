---
description: Funciones de la API de impresión de GDI
ms.assetid: cf3f4a61-8858-4c91-a778-d2a65998ef70
title: Funciones de la API de impresión de GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125e5feef16a64433dadd11e830a09241877a453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909374"
---
# <a name="gdi-print-api-functions"></a>Funciones de la API de impresión de GDI

## <a name="in-this-section"></a>En esta sección



| Función                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortDoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc)<br/>                                     | La función [**AbortDoc**](/windows/desktop/api/wingdi/nf-wingdi-abortdoc) detiene el trabajo de impresión actual y borra todo lo dibujado desde la última llamada a la función [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .<br/>                                                                                                                                                                                                 |
| [*AbortProc*](/windows/desktop/api/Wingdi/nc-wingdi-abortproc)<br/>                                     | La función [**AbortProc**](/windows/desktop/api/wingdi/nc-wingdi-abortproc) es una función de devolución de llamada definida por la aplicación que se usa con la función [**SetAbortProc**](/windows/desktop/api/Wingdi/nf-wingdi-setabortproc) . Se llama cuando se va a cancelar un trabajo de impresión durante la puesta en cola. El tipo **ABORTPROC** define un puntero a esta función de devolución de llamada. **AbortProc** es un marcador de posición para el nombre de la función definida por la aplicación.<br/> |
| [**DeviceCapabilities**](/windows/desktop/api/WinGdi/nf-wingdi-devicecapabilitiesa)<br/>                 | La función [**DeviceCapabilities**](/windows/desktop/api/wingdi/nf-wingdi-devicecapabilitiesa) recupera las capacidades de un controlador de impresora.<br/>                                                                                                                                                                                                                                                       |
| [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)<br/>                                         | La función [**EndDoc**](/windows/desktop/api/wingdi/nf-wingdi-enddoc) finaliza un trabajo de impresión.<br/>                                                                                                                                                                                                                                                                                                             |
| [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)<br/>                                       | La función **EndPage** notifica al dispositivo que la aplicación ha terminado de escribir en una página. Esta función se usa normalmente para indicar al controlador de dispositivo que avance a una nueva página.<br/>                                                                                                                                                                             |
| [**Escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape)<br/>                                         | permite a una aplicación tener acceso a las funciones de dispositivo definidas por el sistema que no están disponibles a través de GDI.<br/>                                                                                                                                                                                                                                                         |
| [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)<br/>                                   | La función [**ExtEscape**](/windows/desktop/api/wingdi/nf-wingdi-extescape) permite a una aplicación tener acceso a funciones del dispositivo que no están disponibles a través de GDI.<br/>                                                                                                                                                                                                                                |
| [**IsWindowRedirectedForPrint**](iswindowredirectedforprint.md)<br/> | La función [**IsWindowRedirectedForPrint**](iswindowredirectedforprint.md) determina si la ventana especificada se redirige actualmente para imprimirla.<br/>                                                                                                                                                                                                         |
| [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow)<br/>                               | La función [**PrintWindow**](/windows/desktop/api/winuser/nf-winuser-printwindow) copia una ventana visual en el contexto de dispositivo (DC) especificado, normalmente un DC de impresora.<br/>                                                                                                                                                                                                                              |
| [**SetAbortProc**](/windows/desktop/api/Wingdi/nf-wingdi-setabortproc)<br/>                             | La función [**SetAbortProc**](/windows/desktop/api/wingdi/nf-wingdi-setabortproc) establece la función de anulación definida por la aplicación que permite cancelar un trabajo de impresión durante la puesta en cola.<br/>                                                                                                                                                                                                               |
| [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)<br/>                                     | La función [**StartDoc**](/windows/desktop/api/wingdi/nf-wingdi-startdoca) inicia un trabajo de impresión.<br/>                                                                                                                                                                                                                                                                                                       |
| [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage)<br/>                                   | La función [**StartPage**](/windows/desktop/api/wingdi/nf-wingdi-startpage) prepara el controlador de impresora para aceptar los datos.<br/>                                                                                                                                                                                                                                                                             |



 

 

