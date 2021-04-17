---
description: La API de servicios Web de Microsoft en dispositivos (WSDAPI) admite la implementación de dispositivos y servicios controlados por el cliente, y los hosts de dispositivo que se ajustan al perfil de dispositivos para servicios web (DPWS).
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: Desarrollo de aplicaciones WSD en Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33976a1903c87ffb6c577cd5a451a3b772a67a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716123"
---
# <a name="wsd-application-development-on-windows"></a>Desarrollo de aplicaciones WSD en Windows

La API de servicios Web de Microsoft en dispositivos (WSDAPI) admite la implementación de dispositivos y servicios controlados por el cliente, y los hosts de dispositivo que se ajustan al [Perfil de dispositivos para servicios web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). WSDAPI se puede usar para el desarrollo de implementaciones de cliente y servidor (dispositivo).

Con bastante frecuencia, el código de WSDAPI para estas aplicaciones se genera mediante [WsdCodeGen](web-services-for-devices-code-generator.md). Algunas funciones y métodos WSDAPI están diseñados para ser llamados únicamente por parte del código generado. La documentación de referencia de la API indica cuándo debe usarse o implementarse una función o un método solo por código generado.

El Windows SDK incluye algunos archivos WSDL de ejemplo, archivos de configuración de WsdCodeGen y código generado. Para obtener más información, vea [ejemplos de WSDAPI](wsdapi-samples.md).

Si desea enumerar los dispositivos con el protocolo WSD y consultar los metadatos del dispositivo WSD, puede usar la API de [detección de funciones](/previous-versions/windows/desktop/fundisc/fd-portal) en su lugar.

Si desea implementar un dispositivo WSD que no ejecuta Windows, consulte el desarrollo de [dispositivos WSD](wsd-device-development.md).
