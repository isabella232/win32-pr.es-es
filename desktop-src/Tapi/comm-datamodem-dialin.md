---
description: comm/datamodem/dialin
ms.assetid: 7330db08-5064-47c9-9d28-c5b2b15c3ac6
title: comm/datamodem/dialin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dee5a6f2de9a18f6b51ebfcfdeeac3b13454b8c90b493e65e5f046aec157c48d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117946654"
---
# <a name="commdatamodemdialin"></a>comm/datamodem/dialin

La **clase de dispositivo comm/datamodem/dialin** consta de dispositivos datamodem que solo se usan para las llamadas entrantes. Esta clase reemplaza la clase [**comm/datamodem**](comm-datamodem.md) en Windows 2000 y sistemas operativos posteriores.

Antes Windows 2000, el TSP unimodem solo era compatible con la clase de dispositivo [**comm/datamodem.**](comm-datamodem.md) Puede producirse un comportamiento inesperado cuando una aplicación que marca una llamada saliente cambia la configuración establecida por un servicio que espera una llamada entrante. Las aplicaciones que usan Windows 2000 y sistemas operativos posteriores deben especificar **comm/datamodem/dialin** o [**comm/datamodem/dialout**](comm-datamodem-dialout.md) en las llamadas a [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) o [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig). Esto permite a Unimodem mantener una configuración de acceso telefónico independiente de la configuración de acceso telefónico.

Aunque **comm/datamodem/dialin** lo usa Unimodem en Windows 2000 y versiones posteriores, también lo pueden usar otros TSP en cualquier plataforma. Las aplicaciones que deben ejecutarse en todas las plataformas deben usar primero **comm/datamodem/dialin** en las llamadas a las API que requieren una clase de dispositivo y usar [**comm/datamodem**](comm-datamodem.md) si la API devuelve **LINEERR \_ INVALCALLSTATE**.

El proveedor de servicios Unimodem traduce la clase de dispositivo [**comm/datamodem**](comm-datamodem.md) en llamadas a [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) y [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) a **comm/datamodem/dialin** o [**comm/datamodem/dialout**](comm-datamodem-dialout.md) como se muestra a continuación:

-   Windows 2000 y versiones posteriores:
    -   Si se especifica **NULL** en el parámetro *lpszDeviceClass* en la llamada a [**lineConfigDialog,**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)Unimodem asume **comm/datamodem/dialin**. Si [**se especifica comm/datamodem**](comm-datamodem.md) o [**tapi/line**](tapi-line.md) en la llamada a **lineConfigDialog,** Unimodem traduce esto a [**comm/datamodem/dialout**](comm-datamodem-dialout.md).
    -   En la llamada a [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) o [**lineGetDevConfig,**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) [**comm/datamodem**](comm-datamodem.md) se controla como [**comm/datamodem/dialout**](comm-datamodem-dialout.md). **NULL** indica una clase de dispositivo no válida.
-   Antes Windows 2000:
    -   Si se **especifica NULL** o [**tapi/line**](tapi-line.md) en [**lineConfigDialog,**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)Unimodem asume [**comm/datamodem**](comm-datamodem.md).

La **clase comm/datamodem/dialin** usa las estructuras y configuraciones descritas en la clase de dispositivo [**comm/datamodem.**](comm-datamodem.md)

 

 



