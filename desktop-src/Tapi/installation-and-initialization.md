---
description: La instalación de un nuevo proveedor de servicios es muy específica del dispositivo y del sistema operativo, por lo que los detalles están fuera del ámbito de este SDK.
ms.assetid: 5b48e144-5092-4462-b74c-d3295d23afe1
title: Instalación e inicialización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b15dc5d9d93ce33ac13a04aec3abd7d49fec3ed2ece3cce691d47c0d617bacd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003543"
---
# <a name="installation-and-initialization"></a>Instalación e inicialización

La instalación de un nuevo proveedor de servicios es muy específica del dispositivo y del sistema operativo, por lo que los detalles están fuera del ámbito de este SDK. Por lo general, el objetivo de la instalación es la configuración del proveedor de servicios para el entorno de comunicaciones actual. Esto suele implicar entradas del Registro y la configuración de las dependencias del servicio.

La inicialización de un proveedor de servicios de telefonía comienza con la negociación de versiones. Consulte [Control de versiones de TSPI](tspi-versioning.md) para obtener una explicación de la negociación de versiones y la versión actual.

TAPI llama a [**continuación a TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), que pasa al proveedor un puntero a una función de devolución de llamada que se usa para informar sobre el progreso de las funciones asincrónicas. El TSP devuelve un recuento de dispositivos de línea y teléfono asociados al identificador de dispositivo actual.

Normalmente, el siguiente paso será el inventario de recursos, realizado por TAPI que invoca la línea [**\_ TSPIGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) y [**la línea \_ TSPIGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps). Se espera que el proveedor de servicios rellene los elementos de las estructuras de datos implicadas que pertenecen a las funcionalidades de dispositivo y sesión que admite.

TAPI recopila información de las distintas aplicaciones relacionadas con los requisitos de notificación de eventos e indica al TSP que usa [**\_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) de TSPI que indique qué tipos de medios se deben detectar para una línea y [**\_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) de TSPI para indicar qué eventos de línea y dirección se deben indicar.

 

 
