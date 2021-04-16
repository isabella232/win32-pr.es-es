---
description: Para evitar que las llamadas no pertenecientes estén en el sistema de telefonía, TAPI quita las llamadas que se han señalado desde un proveedor de servicios si no puede identificar que una aplicación sea el propietario inicial de la llamada.
ms.assetid: 6aa9ceb8-4dc7-46b9-979c-bf59a92cdf27
title: Llamadas no propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf07f4d109eb83fb8666728d71c1e129d6cb499
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677419"
---
# <a name="unowned-calls"></a>Llamadas no propiedad

Para evitar que las llamadas no pertenecientes estén en el sistema de telefonía, TAPI quita las llamadas que se han señalado desde un proveedor de servicios si no puede identificar que una aplicación sea el propietario inicial de la llamada. En la versión 2,0 de TAPI y versiones posteriores, TAPI llama a la función [**\_ LineDrop de TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) para quitar la llamada.

El proveedor de servicios puede conocer de antemano si hay o no una aplicación disponible para tomar posesión de una nueva llamada. TAPI siempre informa al proveedor de servicios de los tipos de medios para los que hay una aplicación disponible mediante la función [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) .

Por ejemplo, si un proveedor de servicios determina que hay una llamada activa en la línea que tiene el \_ modo LINEMEDIAMODE INTERACTIVEVOICE, debe comprobar la detección de medios predeterminada antes de generar los mensajes [**\_ NEWCALL**](line-newcall.md) de línea y [**\_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) . Si la detección de medios predeterminada muestra que ninguna aplicación está buscando una \_ llamada a LINEMEDIAMODE INTERACTIVEVOICE, el proveedor de servicios no debe enviar los mensajes porque TAPI lo quitará inmediatamente.

 

 
