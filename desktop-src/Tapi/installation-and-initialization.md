---
description: La instalación de un nuevo proveedor de servicios es muy específica del dispositivo y del sistema operativo, por lo que los detalles están fuera del ámbito de este SDK.
ms.assetid: 5b48e144-5092-4462-b74c-d3295d23afe1
title: Instalación e inicialización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4391f8453d17cc70382d3ecb0dff65189b61c310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688416"
---
# <a name="installation-and-initialization"></a>Instalación e inicialización

La instalación de un nuevo proveedor de servicios es muy específica del dispositivo y del sistema operativo, por lo que los detalles están fuera del ámbito de este SDK. En general, el objetivo de la instalación es la configuración del proveedor de servicios para el entorno de comunicaciones actual. Normalmente, esto implica las entradas del registro y la configuración de las dependencias del servicio.

La inicialización de un proveedor de servicios de telefonía comienza con la negociación de la versión. Vea [control de versiones de TSPI](tspi-versioning.md) para obtener una explicación de la negociación de la versión y la versión actual.

A continuación, TAPI llama a [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), que pasa al proveedor un puntero a una función de devolución de llamada que se usa para informar sobre el progreso de las funciones asincrónicas. El TSP devuelve un recuento de dispositivos de línea y teléfono asociados al identificador de dispositivo actual.

Normalmente, el siguiente paso será el inventario de recursos, realizado por TAPI al invocar [**TSPI \_ LineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) y [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps). Se espera que el proveedor de servicios rellene los elementos de las estructuras de datos implicados que pertenecen a las capacidades de sesión y dispositivo que admite.

TAPI recopila información de las distintas aplicaciones relativas a los requisitos de notificación de eventos e indica a TSP que use [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) para indicar qué tipos de medios se deben detectar para una línea y [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) para indicar qué eventos de línea y dirección se deben notificar.

 

 
