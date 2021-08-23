---
description: En este documento se describen las interfaces que proporcionan métodos que permiten a un MSP interactuar con el entorno de telefonía de Microsoft y permitir que una aplicación TAPI 3 use controles multimedia de MSP.
ms.assetid: e67d4941-ce0f-48b9-8099-b62659ad33e0
title: Referencia de la interfaz del proveedor de servicios multimedia (MSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94ce02312a7c94a7bc2b805a6c73c263546d9cb3f21bbe795d92a91b1010a0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404755"
---
# <a name="media-service-provider-interface-mspi-reference"></a>Referencia de la interfaz del proveedor de servicios multimedia (MSPI)

En este documento se describen las interfaces que proporcionan métodos que permiten a un MSP interactuar con el entorno de telefonía de Microsoft y permitir que una aplicación TAPI 3 use los controles multimedia de un MSP.



| Interfaces del proveedor de servicios multimedia      | Descripción                                                                                                                                                                            | ¿Necesario? |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)             | Solo se expone a TAPI. Interfaz msp principal para el archivo DLL de TAPI. TAPI 3 llama **a CoCreateInstance en** esta interfaz para crear el objeto MSP.                                               | Sí       |
| [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                     | Expuesto a aplicaciones. Proporciona métodos que permiten a una aplicación recuperar información de una secuencia, iniciarla, pausar o detenerla, y seleccionar o anular la selección de terminales en una secuencia. | Sí       |
| [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)       | Expuesto a aplicaciones. Proporciona métodos que permiten a una aplicación crear o quitar secuencias.                                                                                       | Sí       |
| [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)               | Expuesto a aplicaciones. Interfaz de enumerador [**para ITStream.**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                                                                                                        | Sí       |
| [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)               | Expuesto a aplicaciones. Proporciona métodos que permiten a una aplicación recuperar información en una subtransmisión, iniciarla, pausar o detenerla, y seleccionar o anular la selección de terminales.          | Opcionales  |
| [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) | Expuesto a aplicaciones. Proporciona métodos que permiten a una aplicación crear o quitar substreams.                                                                                    | Opcionales  |
| [**IEnumSubStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumsubstream)         | Expuesto a aplicaciones. Interfaz de enumerador [**para ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream).                                                                                                  | Opcionales  |
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                 | Expuesto a aplicaciones. Obtiene información sobre el [objeto Terminal](terminal-object.md), como la llamada de terminal y los medios admitidos.                                                    | Sí       |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)   | Expuesto a aplicaciones. Proporciona métodos para consultar los terminales disponibles y crear terminales adicionales.                                                                             | Sí       |
| [**ITTerminalSupport2**](/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport2) | Expuesto a aplicaciones. Recupera información sobre las clases de terminal conectables y las superclases; se deriva de la [**interfaz ITTerminalSupport.**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)           | Sí       |



 

## <a name="media-service-provider-interface-types"></a>Tipos de interfaz del proveedor de Media Service

-   [**EVENTO \_ DE DIRECCIÓN DE \_ MSP**](/windows/win32/api/msp/ne-msp-msp_address_event)
-   [**EVENTO DE \_ LLAMADA \_ DE MSP**](/windows/win32/api/msp/ne-msp-msp_call_event)
-   [**EVENTO \_ DE MSP**](/windows/win32/api/msp/ne-msp-msp_event)
-   [**INFORMACIÓN \_ DE EVENTOS DE \_ MSP**](/windows/win32/api/msp/ns-msp-msp_event_info)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz del proveedor de servicios multimedia (MSPI)](media-service-provider-interface-mspi-.md)
</dt> </dl>

 

 
