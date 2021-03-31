---
description: Un proveedor de servicios de telefonía (TSP) es una biblioteca de vínculos dinámicos (DLL) que admite el control de los dispositivos de comunicaciones a través de un conjunto de funciones de servicio exportadas.
ms.assetid: 276c27ac-b6ee-42a7-8327-33dfd87e69bd
title: Proveedores de servicios de telefonía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3c8887723cc74a1bf0d77bcdcfd06c8468a4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912762"
---
# <a name="telephony-service-providers"></a>Proveedores de servicios de telefonía

## <a name="purpose"></a>Propósito

Un proveedor de servicios de telefonía (TSP) es una biblioteca de vínculos dinámicos (DLL) que admite el control de los dispositivos de comunicaciones a través de un conjunto de funciones de servicio exportadas. Una aplicación TAPI usa comandos estandarizados, TAPI pasa información al proveedor de servicios de telefonía y el TSP controla los comandos específicos que se deben intercambiar con el dispositivo.

Un TSP debe ajustarse a la interfaz del proveedor de servicios de telefonía (TSPI) para que funcione como un proveedor de servicios en el entorno de telefonía de Microsoft. TSPI define las funciones externas expuestas por un proveedor de servicios de telefonía proporcionado con el equipo de comunicaciones.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Puede escribir aplicaciones habilitadas para TAPI en muchos lenguajes, como Java, Visual Basic y C/C++. La experiencia de desarrollo anterior con las telecomunicaciones u otras aplicaciones de telefonía es útil, pero no es necesario.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

TSPI habilita el desarrollo de profesionales para todas las versiones de Windows.

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

[TAPI 2,2](./tapi-2-2-start-page.md)
</dt> <dt>

[TAPI 3,1](./tapi-3-1-start-page.md)
</dt> </dl>

 

