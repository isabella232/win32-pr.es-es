---
description: Un proveedor de servicios de telefonía (TSP) es una biblioteca de vínculos dinámicos (DLL) que admite el control de dispositivos de comunicaciones a través de un conjunto de funciones de servicio exportadas.
ms.assetid: 276c27ac-b6ee-42a7-8327-33dfd87e69bd
title: Proveedores de servicios de telefonía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c1e7ff98bfbc898a419e385be07ebdae56d2067061d2ac7951b8c0aff42dcd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872875"
---
# <a name="telephony-service-providers"></a>Proveedores de servicios de telefonía

## <a name="purpose"></a>Propósito

Un proveedor de servicios de telefonía (TSP) es una biblioteca de vínculos dinámicos (DLL) que admite el control de dispositivos de comunicaciones a través de un conjunto de funciones de servicio exportadas. Una aplicación TAPI usa comandos estandarizados, TAPI pasa información al proveedor de servicios de telefonía y el TSP controla los comandos específicos que se deben intercambiar con el dispositivo.

Un TSP debe ajustarse a la interfaz del proveedor de servicios de telefonía (TSPI) para funcionar como proveedor de servicios en el entorno de telefonía de Microsoft. TSPI define las funciones externas expuestas por un proveedor de servicios de telefonía suministrado con equipos de comunicaciones.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Puede escribir aplicaciones habilitadas para TAPI en muchos lenguajes, incluidos Java, Visual Basic y C/C++. La experiencia de desarrollo anterior con telecomunicaciones u otras aplicaciones de telefonía es útil, pero no es necesaria.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

TSPI permite el desarrollo de TSP para todas las versiones de Windows.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                | Descripción                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Información general](about-the-telephony-service-provider-tsp-.md)<br/> | Información general sobre la arquitectura y los componentes de TSPI.<br/> |
| [Referencia](tspi-reference.md)<br/>                           | Documentación de las interfaces TSPI.<br/>                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción a la telefonía de Microsoft](./microsoft-telephony-overview.md)
</dt> <dt>

[Proveedores de servicios multimedia](./media-service-providers-start-page.md)
</dt> <dt>

[TAPI 2.2](./tapi-2-2-start-page.md)
</dt> <dt>

[TAPI 3.1](./tapi-3-1-start-page.md)
</dt> </dl>

 

