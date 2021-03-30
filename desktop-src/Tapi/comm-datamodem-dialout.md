---
description: COMM/telemodem/de llamadas
ms.assetid: b1cc19d2-4a9f-4d3f-a868-d5928654ad75
title: COMM/telemodem/de llamadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 553e998acdfe77509d62050b825dae6ea88d3b3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002449"
---
# <a name="commdatamodemdialout"></a>COMM/telemodem/de llamadas

La clase de dispositivo **COMM/telemodem/** Calling se compone de los dispositivos de módem que solo se usan para las llamadas salientes. Esta clase reemplaza la clase [**COMM/telemodem**](comm-datamodem.md) en Windows 2000 y sistemas operativos posteriores.

Antes de Windows 2000, el TSP de Unimodem solo admitía la clase de dispositivo [**COMM/telemodem**](comm-datamodem.md) . Un comportamiento inesperado puede producirse cuando una aplicación que marca una llamada saliente cambia la configuración establecida por un servicio que espera una llamada entrante. Las aplicaciones que usan Windows 2000 y los sistemas operativos posteriores deben especificar [**COMM/telemodem/Dialin**](comm-datamodem-dialin.md) o **COMM/telemodem/** telellamada en las llamadas a [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) o [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig). Esto permite a Unimodem mantener una configuración de acceso telefónico independiente de la configuración de acceso telefónico.

Mientras que Unimodem en Windows 2000 y versiones posteriores usan **COMM/telemodem/** interactivación, también puede usarlos otros profesionales en cualquier plataforma. Las aplicaciones que deben ejecutarse en todas las plataformas deben usar primero **COMM/telemodem/** Call en las llamadas a la API que requieren una clase de dispositivo y solo usan [**COMM/telemodem**](comm-datamodem.md) si la API devuelve **LINEERR \_ INVALCALLSTATE**.

El proveedor de servicios Unimodem traduce la clase de dispositivo [**COMM/telemodem**](comm-datamodem.md) en llamadas a [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) y [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) a [**COMM/telemodem/Dialin**](comm-datamodem-dialin.md) o **COMM/telemodem/** dial de la manera siguiente:

-   Windows 2000 y versiones posteriores:
    -   Si se especifica **null** en el parámetro *lpszDeviceClass* en la llamada a [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog), Unimodem supone [**COMM/telemodem/Dialin**](comm-datamodem-dialin.md). Si se especifica [**COMM/telemodem**](comm-datamodem.md) o [**TAPI/line**](tapi-line.md) en la llamada a **lineConfigDialog**, Unimodem lo traduce a **COMM/telemodem/** Caller.
    -   En la llamada a [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) o [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig), [**COMM/telemodem**](comm-datamodem.md) se administra como **COMM/telemodem/** Caller. **Null** indica una clase de dispositivo no válida.
-   Antes de Windows 2000:
    -   Si se especifica **null** o [**TAPI/line**](tapi-line.md) en [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog), Unimodem supone [**COMM/telemodem**](comm-datamodem.md).

La clase **COMM/telemodem/de llamadas** usa las estructuras y configuraciones que se describen en la clase de dispositivo [**COMM/telemodem**](comm-datamodem.md) .

 

 



