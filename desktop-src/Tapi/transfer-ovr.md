---
description: La operación de transferencia permite a una aplicación enviar una sesión de comunicaciones conectada actualmente a una dirección diferente.
ms.assetid: b1027f09-74e1-4da8-b718-bb55a56dda1d
title: Transferencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724b9ade43e41ab95a5baa6dfe7d3269f4e4a174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082697"
---
# <a name="transfer"></a>Transferencia

La operación de transferencia permite a una aplicación enviar una sesión de comunicaciones conectada actualmente a una dirección diferente.

TAPI proporciona dos mecanismos para transferir una sesión actual a una dirección diferente. La *transferencia ciega* permite transferir una sesión existente a una dirección de destino especificada en una fase. La *transferencia de consultas* requiere la existencia de una sesión de consulta además de la sesión actual que se debe configurar para la transferencia y, a continuación, la finalización de la transferencia. La elección entre estos dos tipos suele basarse en las capacidades del proveedor de servicios porque algunos proveedores de servicios no admiten la transferencia ciega. En algunos casos, las necesidades de las aplicaciones pueden hacer que la transferencia Consultiva sea el método preferido incluso cuando sea posible la transferencia ciega.

La operación de transferencia ciega es básicamente la misma en TAPI 2 y TAPI 3, pero la transferencia Consultiva sigue patrones ligeramente diferentes.

**TAPI 2. x:** La transferencia Consultiva comienza con la invocación de [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer), que realiza la llamada existente en la espera de la consulta y identifica esta llamada como el destino de la siguiente solicitud de finalización de transferencia. La función **lineSetupTransfer** también asigna una llamada de consulta que se puede usar para establecer la llamada de consulta con la entidad a la que se transferirá la llamada. La aplicación puede marcar la extensión de la entidad de destino en la llamada de consulta (mediante el uso de [**líneas**](/windows/win32/api/tapi/nf-tapi-linedial)), o puede quitar y desasignar la llamada de consulta y, en su lugar, activar una llamada contenida existente (mediante [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold)), si la admite el modificador. Mientras la llamada inicial está en espera de consulta y la llamada de consulta está activa, la aplicación puede alternar entre estas llamadas mediante [**lineSwapHold**](/windows/win32/api/tapi/nf-tapi-lineswaphold).

**TAPI 2. x:** Las aplicaciones completan la transferencia Consultiva mediante [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer). Ambas llamadas revertirán al estado *inactivo* .

Las aplicaciones pueden usar la característica "transferencia de un paso" de muchas PBX (una sola pulsación de botones para establecer una transferencia de consulta) estableciendo el parámetro *lpCallParams* en el miembro **LINECALLPARAMFLAGS \_ ONESTEPTRANSFER** de las [ \_ constantes LINECALLPARAMFLAGS](./linecallparamflags--constants.md) al llamar a [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer).

**TAPI 3. x:** La transferencia Consultiva comienza con el uso de [**ITAddress:: CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) para crear una llamada de consulta a la nueva dirección de destino. A continuación, se llama a [**ITBasicCallControl:: Transfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer) en el objeto de llamada original mediante un puntero al nuevo objeto de llamada de consulta como parámetro. La llamada a [**ITBasicCallControl:: Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish) en el objeto de llamada de consulta completa la transferencia.

La aplicación debe liberar los recursos de sesión después de la finalización correcta de una operación de transferencia.

No todos los proveedores de servicios admiten el uso de esta operación.

**TAPI 2. x:** Consulte [**lineBlindTransfer**](/windows/win32/api/tapi/nf-tapi-lineblindtransfer), [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer), [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer).

**TAPI 3. x:** Vea [**ITBasicCallControl:: BlindTransfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-blindtransfer), [**ITAddress:: CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall), [**ITBasicCallControl:: Transfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer), [**ITBasicCallControl:: Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish).

 

 
