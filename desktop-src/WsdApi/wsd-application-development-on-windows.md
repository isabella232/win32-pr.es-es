---
description: Aprenda a usar microsoft Web Services on Devices API (WSD) API (WSDAPI) para implementar servicios y dispositivos controlados por el cliente, y hosts de dispositivos conformes a DPWS.
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: Desarrollo de aplicaciones WSD en Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3d02810f55cc7ae450323543d7a0ee88f055b247fed589057e7d77710f4f86d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639355"
---
# <a name="wsd-application-development-on-windows"></a>Desarrollo de aplicaciones WSD en Windows

Microsoft Web Services on Devices API (WSDAPI) admite la implementación de servicios y dispositivos controlados por el cliente, y hosts de dispositivos que se ajustan al perfil de dispositivos para servicios [web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). WSDAPI se puede usar para el desarrollo de implementaciones de cliente y servidor (dispositivo).

A menudo, el código WSDAPI para estas aplicaciones se genera mediante [WsdCodeGen](web-services-for-devices-code-generator.md). Algunas funciones y métodos de WSDAPI están diseñados para ser llamados solo por código generado. La documentación de referencia de API indica cuándo se debe usar o implementar una función o un método solo mediante código generado.

El SDK Windows incluye algunos archivos WSDL de ejemplo, archivos de configuración WsdCodeGen y código generado. Para obtener más información, vea [Ejemplos de WSDAPI.](wsdapi-samples.md)

Si desea enumerar los dispositivos mediante el protocolo WSD y consultar los metadatos del dispositivo WSD, puede usar function [discovery](/previous-versions/windows/desktop/fundisc/fd-portal) API en su lugar.

Si desea implementar un dispositivo WSD que no se ejecute Windows, consulte Desarrollo de [dispositivos WSD.](wsd-device-development.md)
