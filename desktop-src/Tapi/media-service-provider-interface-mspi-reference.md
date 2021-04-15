---
description: En este documento se describen las interfaces que proporcionan métodos que permiten a un MSP interactuar con el entorno de telefonía de Microsoft y permitir que una aplicación TAPI 3 Use un control de medios de MSP.
ms.assetid: e67d4941-ce0f-48b9-8099-b62659ad33e0
title: Referencia de la interfaz del proveedor de servicios multimedia (MSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a30b961fff4d8a9e50fb35573633cc2dc06e370c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689648"
---
# <a name="media-service-provider-interface-mspi-reference"></a>Referencia de la interfaz del proveedor de servicios multimedia (MSPI)

En este documento se describen las interfaces que proporcionan métodos que permiten a un MSP interactuar con el entorno de telefonía de Microsoft y permitir que una aplicación TAPI 3 Use los controles multimedia de MSP.



| Interfaces de la interfaz del proveedor de servicios multimedia      | Descripción                                                                                                                                                                            | ¿Necesario? |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)             | Solo se expone en TAPI. Interfaz principal MSP para la DLL de TAPI. TAPI 3 llama a **CoCreateInstance** en esta interfaz para crear el objeto MSP.                                               | Sí       |
| [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                     | Se expone a las aplicaciones. Proporciona métodos que permiten a una aplicación recuperar información en una secuencia, iniciarla, pausarla o detenerla, y seleccionar o anular la selección de terminales en una secuencia. | Sí       |
| [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)       | Se expone a las aplicaciones. Proporciona métodos que permiten a una aplicación crear o quitar secuencias.                                                                                       | Sí       |
| [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)               | Se expone a las aplicaciones. Interfaz de enumerador para [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).                                                                                                        | Sí       |
| [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)               | Se expone a las aplicaciones. Proporciona métodos que permiten a una aplicación recuperar información en una subsecuencia, iniciarla, pausarla o detenerla, y seleccionar o anular la selección de terminales.          | Opcionales  |
| [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) | Se expone a las aplicaciones. Proporciona métodos que permiten a una aplicación crear o quitar subsecuencias.                                                                                    | Opcionales  |
| [**IEnumSubStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumsubstream)         | Se expone a las aplicaciones. Interfaz de enumerador para [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream).                                                                                                  | Opcionales  |
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                 | Se expone a las aplicaciones. Obtiene información sobre el [objeto terminal](terminal-object.md), como la llamada de terminal y los medios admitidos.                                                    | Sí       |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)   | Se expone a las aplicaciones. Proporciona métodos para consultar los terminales disponibles y crear terminales adicionales.                                                                             | Sí       |
| [**ITTerminalSupport2**](/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport2) | Se expone a las aplicaciones. Recupera información sobre las clases y superclases de terminal conectables. deriva de la interfaz [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) .           | Sí       |



 

## <a name="media-service-provider-interface-types"></a>Tipos de interfaz del proveedor de servicios multimedia

-   [**\_evento de dirección MSP \_**](/windows/win32/api/msp/ne-msp-msp_address_event)
-   [**\_evento de llamada MSP \_**](/windows/win32/api/msp/ne-msp-msp_call_event)
-   [**\_evento MSP**](/windows/win32/api/msp/ne-msp-msp_event)
-   [**\_información del evento MSP \_**](/windows/win32/api/msp/ns-msp-msp_event_info)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz del proveedor de servicios multimedia (MSPI)](media-service-provider-interface-mspi-.md)
</dt> </dl>

 

 
