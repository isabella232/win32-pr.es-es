---
description: Los siguientes son métodos MSPI estándar que todos los MSP deben implementar. La documentación principal de estos métodos existe en la sección referencia de la interfaz del proveedor de servicios multimedia (MSPI).
ms.assetid: 22d4828e-f439-44ca-aa6c-f7f18c5fd64f
title: Métodos CMSPAddress MSPI implementados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed19bbacc13990d052c35bda68f97db80ff68ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688415"
---
# <a name="cmspaddress-mspi-methods-implemented"></a>Métodos CMSPAddress MSPI implementados

Los siguientes son métodos MSPI estándar que todos los MSP deben implementar. La documentación principal de estos métodos existe en la sección referencia de la [interfaz del proveedor de servicios multimedia (MSPI)](media-service-provider-interface-mspi-reference.md) .



| Métodos CMSPAddress                                                                          | Descripción                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Inicialización**](/windows/desktop/api/msp/nf-msp-itmspaddress-initialize)                                                | (Interfaz [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)) Lo llama TAPI3 cuando se crea por primera vez este MSP.                                                                                                                                                                                                                                                                                                   |
| [**Apagado**](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdown)                                                    | (Interfaz [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)) Lo llama TAPI3 cuando esta dirección no está en uso más.                                                                                                                                                                                                                                                                                         |
| [**ReceiveTSPData**](/windows/desktop/api/msp/nf-msp-itmspaddress-receivetspdata)                                        | (Interfaz [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)) Lo llama TAPI3 cuando el TSP envía datos a este objeto de dirección MSP.                                                                                                                                                                                                                                                                               |
| [**GetEvent**](/windows/desktop/api/msp/nf-msp-itmspaddress-getevent)                                                    | (Interfaz [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)) Llamado por TAPI3 para obtener información detallada sobre un evento.                                                                                                                                                                                                                                                                                       |
| [**obtener \_ StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals)                        | (Interfaz [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Contenedor de automatización OLE para la función auxiliar [**GetStaticTerminals**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals).                                                                                                                                                                                                                            |
| [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals)               | (Interfaz [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Contenedor de enumeración para la función auxiliar [**GetStaticTerminals**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals).                                                                                                                                                                                                                               |
| [**obtener \_ DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses)          | (Interfaz [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Contenedor de automatización OLE para la función auxiliar [**GetDynamicTerminalClasses**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses).                                                                                                                                                                                                              |
| [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) | (Interfaz [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Contenedor de enumeración para la función auxiliar [**GetDynamicTerminalClasses**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses).                                                                                                                                                                                                                 |
| [**CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)                                   | (Interfaz [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) La aplicación llama a este método para crear un terminal dinámico. Programa un elemento de trabajo en el subproceso de trabajo de MSP, que, cuando se ejecuta, pide al administrador de Terminal Server que cree un terminal dinámico. La clase derivada puede invalidar este método para tener su propia forma de crear un terminal dinámico.                                |
| [**GetDefaultStaticTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-getdefaultstaticterminal)               | (Interfaz [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) La aplicación llama a este método para obtener el terminal estático predeterminado para un tipo y dirección especificados. Actualiza la lista de terminales predeterminada (si es necesario) y devuelve el puntero de interfaz. La clase derivada puede invalidar este método para tener su propia forma de decidir qué terminal es el predeterminado. Bloquea las listas de terminales. |



 

 

 
