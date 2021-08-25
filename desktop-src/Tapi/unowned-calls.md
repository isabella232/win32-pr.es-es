---
description: Para evitar que las llamadas sin propietario se encontraran en el sistema de telefonía, TAPI quita las llamadas que se han señalado desde un proveedor de servicios si no puede identificar que una aplicación sea el propietario inicial de la llamada.
ms.assetid: 6aa9ceb8-4dc7-46b9-979c-bf59a92cdf27
title: Llamadas sin sestear
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ea6fffa2ee65f24d73337980e2a8952157aa5d1000e5c657d75af372f26f00d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991655"
---
# <a name="unowned-calls"></a>Llamadas sin sestear

Para evitar que las llamadas sin propietario se encontraran en el sistema de telefonía, TAPI quita las llamadas que se han señalado desde un proveedor de servicios si no puede identificar que una aplicación sea el propietario inicial de la llamada. En TAPI versión 2.0 y posteriores, TAPI llama a la función [**\_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) de TSPI para quitar la llamada.

El proveedor de servicios puede saber de antemano si hay o no una aplicación disponible para tomar posesión de una nueva llamada. TAPI siempre informa al proveedor de servicios de los tipos de medios para los que hay una aplicación disponible mediante la función [**\_ lineSetDefaultMediaDetection de TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection)

Por ejemplo, si un proveedor de servicios determina que hay una llamada activa en la línea que tiene el modo LINEMEDIAMODE INTERACTIVEVOICE, debe comprobar la detección de medios predeterminada antes de generar los mensajes \_ [**LINE \_ NEWCALL**](line-newcall.md) y [**LINE \_ CALLSTATE.**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) Si la detección de medios predeterminada muestra que ninguna aplicación busca una llamada LINEMEDIAMODE INTERACTIVEVOICE, el proveedor de servicios no debe enviar los mensajes porque TAPI la \_ quitará inmediatamente.

 

 
