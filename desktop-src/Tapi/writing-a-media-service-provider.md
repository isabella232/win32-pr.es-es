---
description: Un proveedor de servicios multimedia debe implementar un subconjunto mínimo de interfaces MSPI ITMSPAddress ITTerminalSupport ITStreamControl y ITStream.
ms.assetid: 59560bdf-953e-48e8-b565-46c3e0123c7e
title: Escritura de un proveedor de servicios multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782dddb9a87725bde7c104d459b71204a04de018
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361832"
---
# <a name="writing-a-media-service-provider"></a>Escritura de un proveedor de servicios multimedia

Un proveedor de servicios multimedia debe implementar un subconjunto mínimo de interfaces MSPI: [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)y [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream). La compatibilidad con subsecuencias es opcional. Además, un MSP determinado puede implementar métodos adicionales, como los controles necesarios para el hardware especializado.

Los siguientes documentos materiales:

-   Las [clases base de TAPI 3 MSP](tapi-3-msp-base-classes.md), que son un conjunto de clases de C++ diseñado para simplificar la tarea de crear un MSP basado en DirectShow. Las clases base implementan todas las interfaces de MSPI de forma genérica. Distintos MSP pueden invalidar funciones específicas de MSP y proporcionar sus propias implementaciones.
-   El [Administrador de terminales TAPI 3](tapi-3-terminal-manager.md), que proporciona interfaces y métodos usados por un MSP para controlar los terminales.
-   [Terminales conectables](writing-a-pluggable-terminal.md), que permiten a una aplicación en lugar de a un MSP crear terminales. Los desarrolladores que ya tienen experiencia en escribir proveedores de servicios serán los creadores principales de terminales conectables. La versión inicial implementada para esta versión está destinada a las aplicaciones de servidor de conferencias que necesitan agregar clientes que no son de Windows 2000 o que no son de multidifusión a conferencias de multidifusión SDP/IP de varios usuarios de varias partes.

 

 
