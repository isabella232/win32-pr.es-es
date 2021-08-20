---
description: Los siguientes son métodos MSPI estándar que todos los MSP deben implementar. La documentación principal de estos métodos existe en la sección Referencia de la interfaz del proveedor de servicios multimedia (MSPI).
ms.assetid: 22d4828e-f439-44ca-aa6c-f7f18c5fd64f
title: Métodos MSPI de CMSPAddress implementados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181a94cf7b1bdb1a2b73d9b976f5111639d331dd73f6f57f5cc1f3b0a43110c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117947457"
---
# <a name="cmspaddress-mspi-methods-implemented"></a>Métodos MSPI de CMSPAddress implementados

Los siguientes son métodos MSPI estándar que todos los MSP deben implementar. La documentación principal de estos métodos existe en la sección Referencia de la interfaz del proveedor de servicios multimedia [(MSPI).](media-service-provider-interface-mspi-reference.md)



| Métodos CMSPAddress                                                                          | Descripción                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Inicialización**](/windows/desktop/api/msp/nf-msp-itmspaddress-initialize)                                                | (Interfaz [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)) TapI3 lo llama cuando se crea este MSP por primera vez.                                                                                                                                                                                                                                                                                                   |
| [**Apagado**](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdown)                                                    | (Interfaz [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)) Lo llama TAPI3 cuando esta dirección ya no está en uso.                                                                                                                                                                                                                                                                                         |
| [**ReceiveTSPData**](/windows/desktop/api/msp/nf-msp-itmspaddress-receivetspdata)                                        | (Interfaz [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)) Lo llama TAPI3 cuando el TSP envía datos a este objeto de dirección MSP.                                                                                                                                                                                                                                                                               |
| [**GetEvent**](/windows/desktop/api/msp/nf-msp-itmspaddress-getevent)                                                    | (Interfaz [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)) TapI3 lo llama para obtener información detallada sobre un evento.                                                                                                                                                                                                                                                                                       |
| [**get \_ StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals)                        | (Interfaz [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Contenedor de AUTOMATIZACIÓN OLE para la función auxiliar [**GetStaticTerminals**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals).                                                                                                                                                                                                                            |
| [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals)               | (Interfaz [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Contenedor de enumeración para la función auxiliar [**GetStaticTerminals**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals).                                                                                                                                                                                                                               |
| [**get \_ DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses)          | (Interfaz [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Contenedor de AUTOMATIZACIÓN OLE para la función auxiliar [**GetDynamicTerminalClasses**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses).                                                                                                                                                                                                              |
| [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) | (Interfaz [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Contenedor de enumeración para la función auxiliar [**GetDynamicTerminalClasses**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses).                                                                                                                                                                                                                 |
| [**CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)                                   | (Interfaz [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) La aplicación llama a este método para crear un terminal dinámico. Programa un elemento de trabajo en el subproceso de trabajo del MSP, que, cuando se ejecuta, solicita al Administrador de terminales que cree un terminal dinámico. La clase derivada puede invalidar este método para tener su propia manera de crear un terminal dinámico.                                |
| [**GetDefaultStaticTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-getdefaultstaticterminal)               | (Interfaz [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) La aplicación llama a este método para obtener el terminal estático predeterminado para un tipo y una dirección especificados. Actualiza la lista de terminales predeterminada (si es necesario) y devuelve el puntero de interfaz. La clase derivada puede invalidar este método para tener su propia manera de decidir qué terminal es el valor predeterminado. Bloquea las listas de terminales. |



 

 

 
