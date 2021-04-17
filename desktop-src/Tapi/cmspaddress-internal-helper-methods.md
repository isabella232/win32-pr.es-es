---
description: La lista siguiente contiene los métodos internos de la dirección CMSP.
ms.assetid: 2016a776-1464-46b5-96b9-b045834f9e38
title: Métodos auxiliares internos de CMSPAddress
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17064d161e2a073addb2e8eef6d9d290b41278b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689556"
---
# <a name="cmspaddress-internal-helper-methods"></a>Métodos auxiliares internos de CMSPAddress



| Métodos auxiliares internos de CMSPAddress                                        | Descripción                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetStaticTerminals**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals)               | Lo llama [**Get \_ StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals) y [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals) para obtener una matriz de terminales estáticas que se pueden usar en esta dirección.                                     |
| [**GetDynamicTerminalClasses**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses) | Lo llama [**Get \_ DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses) y [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) para obtener una matriz de clases de terminal dinámicas que se pueden usar en esta dirección. |
| [**UpdateTerminalList**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-updateterminallist)               | Rellena la lista de terminales estáticas del MSP.                                                                                                                                                                                                                                |
| [**ReceiveTSPAddressData**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-receivetspaddressdata)         | Se llama cuando un mensaje de datos de TSP está diseñado para ser procesado por la dirección en lugar de por una llamada específica.                                                                                                                                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CMSPAddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 
