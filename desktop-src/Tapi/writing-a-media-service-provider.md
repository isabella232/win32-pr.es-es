---
description: Un proveedor de servicios multimedia debe implementar un subconjunto mínimo de interfaces de MSPI ITMSPAddress ITTerminalSupport ITStreamControl e ITStream.
ms.assetid: 59560bdf-953e-48e8-b565-46c3e0123c7e
title: Escritura de un proveedor de Media Service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f99cc8a52b7362caa01d9743fea7fc848faec2ae451b96ec916f4f3aa5c287
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739025"
---
# <a name="writing-a-media-service-provider"></a>Escritura de un proveedor de Media Service

Un proveedor de servicios multimedia debe implementar un subconjunto mínimo de interfaces MSPI: [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport,**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)e [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream). La compatibilidad con substream es opcional. Además, un MSP determinado puede implementar métodos adicionales, como los controles necesarios para hardware especializado.

Los siguientes documentos de material:

-   Las clases base MSP de [TAPI 3,](tapi-3-msp-base-classes.md)que son un conjunto de clases de C++ diseñadas para simplificar la tarea de crear un MSP basado en DirectShow de datos. Las clases base implementan todas las interfaces MSPI de forma genérica. Los distintos MSP pueden invalidar funciones específicas de MSP y proporcionar sus propias implementaciones.
-   TapI [3 Terminal Manager,](tapi-3-terminal-manager.md)que proporciona interfaces y métodos usados por un MSP para controlar terminales.
-   [Terminales conectables,](writing-a-pluggable-terminal.md)que permiten que una aplicación en lugar de un MSP cree terminales. Los desarrolladores que ya tienen experiencia en la escritura de proveedores de servicios serán los creadores principales de terminales conectables. La versión inicial implementada para esta versión está destinada a la conferencia de aplicaciones de servidor que necesitan agregar clientes que no son de Windows o que no son multidifusión a las conferencias de multidifusión SDP/IP de TAPI 3.

 

 
