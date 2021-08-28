---
description: La operación de transferencia permite a una aplicación enviar una sesión de comunicaciones conectada actualmente a una dirección diferente.
ms.assetid: b1027f09-74e1-4da8-b718-bb55a56dda1d
title: Transferencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87bb527ad8e0a26ba5e4da341eb15509e8af05e7950d82de92be839e70370c79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119514545"
---
# <a name="transfer"></a>Transferencia

La operación de transferencia permite a una aplicación enviar una sesión de comunicaciones conectada actualmente a una dirección diferente.

TAPI proporciona dos mecanismos para transferir una sesión actual a una dirección diferente. *La transferencia invidente* permite transferir una sesión existente a una dirección de destino especificada en una fase. *La transferencia* de consulta requiere la existencia de una sesión de consulta además de la sesión actual para configurar la transferencia y, a continuación, la finalización de la transferencia. La elección entre estos dos tipos se basa con frecuencia en las funcionalidades del proveedor de servicios porque algunos proveedores de servicios no admiten la transferencia invidente. En algunos casos, las necesidades de la aplicación pueden hacer que la transferencia consultiva sea el método preferido, incluso cuando es posible la transferencia invidente.

La operación de transferencia invidente es básicamente la misma en TAPI 2 y TAPI 3, pero la transferencia consultiva sigue patrones ligeramente diferentes.

**TAPI 2.x:** La transferencia consultiva comienza con la invocación de [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer), que coloca la llamada existente en espera de consulta e identifica esta llamada como el destino de la siguiente solicitud de finalización de transferencia. La **función lineSetupTransfer** también asigna una llamada de consulta que se puede usar para establecer la llamada de consulta con la parte a la que se transferirá la llamada. La aplicación puede marcar la extensión de la parte de destino en la llamada de consulta (mediante [**lineDial**](/windows/win32/api/tapi/nf-tapi-linedial)), o puede quitar y desasignar la llamada de consulta y, en su lugar, activar una llamada retenida existente (mediante [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold)), si es compatible con el modificador . Mientras la llamada inicial está en espera de consulta y la llamada de consulta está activa, la aplicación puede alternar entre estas llamadas mediante [**lineSwapHold**](/windows/win32/api/tapi/nf-tapi-lineswaphold).

**TAPI 2.x:** Las aplicaciones completan la transferencia consultiva [**mediante lineCompleteTransfer.**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer) Ambas llamadas revertirán al *estado de inactividad.*

Las aplicaciones pueden usar la característica de "transferencia en un paso" de muchos PBX (una pulsación de un solo botón para establecer una transferencia de consulta) estableciendo el parámetro *lpCallParams* en el miembro **LINECALLPARAMFLAGS \_ ONESTEPTRANSFER** de las constantes [LINECALLPARAMFLAGS \_](./linecallparamflags--constants.md) al llamar a [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer).

**TAPI 3.x:** La transferencia consultiva comienza con [**el uso de ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) para crear una llamada de consulta a la nueva dirección de destino. A continuación, se llama a [**ITBasicCallControl::Transfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer) en el objeto de llamada original mediante un puntero al nuevo objeto de llamada de consulta como parámetro. Al [**llamar a ITBasicCallControl::Finish en**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish) el objeto de llamada de consulta, se completa la transferencia.

La aplicación debe liberar recursos de sesión después de la finalización correcta de una operación de transferencia.

No todos los proveedores de servicios admiten el uso de esta operación.

**TAPI 2.x:** Vea [**lineBlindTransfer**](/windows/win32/api/tapi/nf-tapi-lineblindtransfer), [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer), [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer).

**TAPI 3.x:** Vea [**ITBasicCallControl::BlindTransfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-blindtransfer), [**ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall), [**ITBasicCallControl::Transfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer), [**ITBasicCallControl::Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish).

 

 
