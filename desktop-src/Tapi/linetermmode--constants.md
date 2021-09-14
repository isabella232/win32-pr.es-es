---
description: Las constantes de marca de bits LINETERMMODE describen diferentes tipos de eventos en una línea telefónica que se pueden \_ enrutar a un dispositivo terminal.
ms.assetid: 60af1687-8958-4918-be21-a13780c60974
title: LINETERMMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e689e2e4e432d6cf804e64babd462e749e7e9e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374794"
---
# <a name="linetermmode_-constants"></a>Constantes \_ LINETERMMODE

Las constantes de marca de bits **LINETERMMODE \_** describen diferentes tipos de eventos en una línea telefónica que se pueden enrutar a un dispositivo terminal.

<dl> <dt>

<span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**BOTONES \_ LINETERMMODE**
</dt> <dd> <dl> <dt>



Se trata de eventos de botón que se envían desde el terminal a la línea.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**LINETERMMODE \_ DISPLAY**
</dt> <dd> <dl> <dt>



Esta es la información de presentación enviada desde la línea al terminal.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**LINETERMMODE \_ HOOKSWITCH**
</dt> <dd> <dl> <dt>



Se trata de eventos hookswitch enviados desde el terminal a la línea.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**BOMBILLAS LINETERMMODE \_**
</dt> <dd> <dl> <dt>



Se trata de eventos de bombilla enviados desde la línea al terminal.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**LINETERMMODE \_ MEDIABIDIRECT**
</dt> <dd> <dl> <dt>



Se trata del flujo multimedia bidireccional asociado a una llamada en la línea y el terminal. Use este valor cuando el enrutamiento de ambos canales unidireccionales de la secuencia multimedia de una llamada no se pueda controlar de forma independiente.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**LINETERMMODE \_ MEDIAFROMLINE**
</dt> <dd> <dl> <dt>



Se trata de la secuencia de medios unidireccional desde la línea hasta el terminal asociado a una llamada en la línea. Use este valor cuando el enrutamiento de ambos canales unidireccionales de la secuencia multimedia de una llamada se pueda controlar de forma independiente.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**LINETERMMODE \_ MEDIATOLINE**
</dt> <dd> <dl> <dt>



Se trata de la secuencia de medios unidireccional desde el terminal hasta la línea asociada a una llamada en la línea. Use este valor cuando el enrutamiento de ambos canales unidireccionales de la secuencia multimedia de una llamada se pueda controlar de forma independiente.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**LINETERMMODE \_ RINGER**
</dt> <dd> <dl> <dt>



Esta es la información de control de timbre enviada desde el conmutador al terminal.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Los 32 bits están reservados.

Estas constantes describen las clases de flujos de control e información que se pueden enrutar directamente entre un dispositivo de línea y un dispositivo terminal (por ejemplo, un conjunto de teléfonos).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




