---
description: COMM/telemodem/Dialin
ms.assetid: 7330db08-5064-47c9-9d28-c5b2b15c3ac6
title: COMM/telemodem/Dialin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cb66d72b5d9f2c75af361153d46f5cac9abdfd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002450"
---
# <a name="commdatamodemdialin"></a>COMM/telemodem/Dialin

La clase de dispositivo **COMM/telemodem/Dialon** se compone de dispositivos de módem que se usan solo para llamadas entrantes. Esta clase reemplaza la clase [**COMM/telemodem**](comm-datamodem.md) en Windows 2000 y sistemas operativos posteriores.

Antes de Windows 2000, el TSP de Unimodem solo admitía la clase de dispositivo [**COMM/telemodem**](comm-datamodem.md) . Un comportamiento inesperado puede producirse cuando una aplicación que marca una llamada saliente cambia la configuración establecida por un servicio que espera una llamada entrante. Las aplicaciones que usan Windows 2000 y los sistemas operativos posteriores deben especificar **COMM/telemodem/Dialin** o [**COMM/telemodem/**](comm-datamodem-dialout.md) telellamada en las llamadas a [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) o [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig). Esto permite a Unimodem mantener una configuración de acceso telefónico independiente de la configuración de acceso telefónico.

Mientras que Unimodem usa **COMM/telemodem/Dialin** en Windows 2000 y versiones posteriores, otros profesionales también pueden usarlos en cualquier plataforma. Las aplicaciones que deben ejecutarse en todas las plataformas deben usar primero **COMM/telemodem/Dialin** en las llamadas a las API que requieren una clase de dispositivo y solo usan [**COMM/telemodem**](comm-datamodem.md) si la API devuelve **LINEERR \_ INVALCALLSTATE**.

El proveedor de servicios Unimodem traduce la clase de dispositivo [**COMM/telemodem**](comm-datamodem.md) en llamadas a [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) y [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) a **COMM/telemodem/Dialin** o [**COMM/telemodem/**](comm-datamodem-dialout.md) dial de la manera siguiente:

-   Windows 2000 y versiones posteriores:
    -   Si se especifica **null** en el parámetro *lpszDeviceClass* en la llamada a [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog), Unimodem supone **COMM/telemodem/Dialin**. Si se especifica [**COMM/telemodem**](comm-datamodem.md) o [**TAPI/line**](tapi-line.md) en la llamada a **lineConfigDialog**, Unimodem lo traduce a [**COMM/telemodem/**](comm-datamodem-dialout.md)Caller.
    -   En la llamada a [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) o [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig), [**COMM/telemodem**](comm-datamodem.md) se administra como [**COMM/telemodem/**](comm-datamodem-dialout.md)Caller. **Null** indica una clase de dispositivo no válida.
-   Antes de Windows 2000:
    -   Si se especifica **null** o [**TAPI/line**](tapi-line.md) en [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog), Unimodem supone [**COMM/telemodem**](comm-datamodem.md).

La clase **COMM/telemodem/Dialin** usa las estructuras y configuraciones que se describen en la clase de dispositivo [**COMM/telemodem**](comm-datamodem.md) .

 

 



