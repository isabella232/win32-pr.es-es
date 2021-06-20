---
description: Aprenda a usar microsoft Web Services on Devices API (WSD) API (WSDAPI) para implementar servicios y dispositivos controlados por el cliente, y hosts de dispositivos conformes a DPWS.
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: Desarrollo de aplicaciones WSD en Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 167cd1ad013ea387a6e33b6de449f3f84d49db13
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405788"
---
# <a name="wsd-application-development-on-windows"></a>Desarrollo de aplicaciones WSD en Windows

Microsoft Web Services on Devices API (WSDAPI) admite la implementación de dispositivos y servicios controlados por el cliente, y hosts de dispositivos que se ajustan al perfil de dispositivos para servicios [web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). WSDAPI se puede usar para el desarrollo de implementaciones de cliente y servidor (dispositivo).

A menudo, el código WSDAPI para estas aplicaciones se genera mediante [WsdCodeGen](web-services-for-devices-code-generator.md). Algunas funciones y métodos de WSDAPI están diseñados para ser llamados solo por código generado. La documentación de referencia de API indica cuándo se debe usar o implementar una función o un método solo mediante código generado.

El Windows SDK incluye algunos archivos WSDL de ejemplo, archivos de configuración WsdCodeGen y código generado. Para obtener más información, vea [Ejemplos de WSDAPI.](wsdapi-samples.md)

Si desea enumerar los dispositivos mediante el protocolo WSD y consultar los metadatos del dispositivo WSD, puede usar function [discovery](/previous-versions/windows/desktop/fundisc/fd-portal) API en su lugar.

Si desea implementar un dispositivo WSD que no ejecute Windows, consulte [Desarrollo de dispositivos WSD.](wsd-device-development.md)
