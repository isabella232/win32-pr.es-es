---
description: Un proveedor de servicios multimedia (MSP) permite que una aplicación controle los medios de un mecanismo de transporte determinado.
ms.assetid: f886380f-d970-4511-bf71-fb1eb767e4f4
title: Proveedores de servicios multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd78f5ff4a13da4365f99bd2cb539738b6f3fd6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689640"
---
# <a name="media-service-providers"></a>Proveedores de servicios multimedia

## <a name="purpose"></a>Propósito

Un proveedor de servicios multimedia (MSP) permite que una aplicación controle los medios de un mecanismo de transporte determinado. Un MSP siempre se empareja con un proveedor de servicios de telefonía (TSP).

La interfaz del proveedor de servicios multimedia (MSPI) es un conjunto de interfaces y métodos implementados por un MSP para permitir un control de la aplicación sobre el transporte multimedia durante una sesión de comunicaciones. Un MSP controla los mecanismos específicos del dispositivo y específicos del protocolo necesarios para activar estos controles y se comunica con su TSP emparejado o con una aplicación mediante el uso de los métodos proporcionados en MSPI.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Es necesario estar familiarizado con COM. La experiencia de desarrollo con las telecomunicaciones y otras aplicaciones de telefonía es útil, pero no es necesario.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

MSPI permite el desarrollo de proveedores de servicios multimedia para determinados protocolos o dispositivos que se ejecutan en sistemas operativos Windows Server 2003, Windows XP y Windows 2000.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                       | Descripción                                                           |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Información general](about-the-media-service-provider-msp-.md)<br/>            | Información general sobre la arquitectura y los componentes de MSP.<br/> |
| [Referencia](media-service-provider-interface-mspi-reference.md)<br/> | Documentación de las interfaces MSPI.<br/>                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción a la telefonía de Microsoft](microsoft-telephony-overview.md)
</dt> <dt>

[TAPI 3,1](tapi-3-1-start-page.md)
</dt> <dt>

[Proveedores de servicios de telefonía](./telephony-service-providers-start-page.md)
</dt> </dl>

 

