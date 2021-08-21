---
description: Las constantes de marca de bits LINETERMMODE describen diferentes tipos de eventos en una línea de teléfono que se pueden \_ enrutar a un dispositivo terminal.
ms.assetid: 60af1687-8958-4918-be21-a13780c60974
title: LINETERMMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411c1dd633ff1bef49e08eb127f4145f81f3d6785d07f3566431fe7b5d7e8fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518815"
---
# <a name="linetermmode_-constants"></a>LineTERMMODE \_ (Constantes)

Las constantes de marca de bits **LINETERMMODE \_** describen diferentes tipos de eventos en una línea de teléfono que se pueden enrutar a un dispositivo terminal.

<dl> <dt>

<span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**BOTONES \_ LINETERMMODE**
</dt> <dd> <dl> <dt>



Se trata de eventos de botón que se envían desde el terminal a la línea.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**LINETERMMODE \_ DISPLAY**
</dt> <dd> <dl> <dt>



Se trata de la información de visualización enviada desde la línea al terminal.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**LINETERMMODE \_ HOOKSWITCH**
</dt> <dd> <dl> <dt>



Se trata de eventos de conmutador de enlace enviados desde el terminal a la línea.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**LINETERMMODE \_ LAMPS**
</dt> <dd> <dl> <dt>



Se trata de eventos de bombilla enviados desde la línea al terminal.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**LINETERMMODE \_ MEDIABIDIRECT**
</dt> <dd> <dl> <dt>



Se trata del flujo multimedia bidireccional asociado a una llamada en la línea y el terminal. Use este valor cuando el enrutamiento de ambos canales unidireccionales de la secuencia multimedia de una llamada no se pueda controlar de forma independiente.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**LINETERMMODE \_ MEDIAFROMLINE**
</dt> <dd> <dl> <dt>



Se trata del flujo multimedia unidireccional desde la línea al terminal asociado a una llamada en la línea. Use este valor cuando el enrutamiento de ambos canales unidireccionales de la secuencia multimedia de una llamada se pueda controlar de forma independiente.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**LINETERMMODE \_ MEDIATOLINE**
</dt> <dd> <dl> <dt>



Se trata del flujo multimedia unidireccional desde el terminal hasta la línea asociada a una llamada en la línea. Use este valor cuando el enrutamiento de ambos canales unidireccionales de la secuencia multimedia de una llamada se pueda controlar de forma independiente.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**LINETERMMODE \_ RINGER**
</dt> <dd> <dl> <dt>



Se trata de información de control de timbre enviada desde el conmutador al terminal.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Sin extensibilidad. Los 32 bits están reservados.

Estas constantes describen las clases de flujos de control e información que se pueden enrutar directamente entre un dispositivo de línea y un dispositivo terminal (por ejemplo, un conjunto de teléfonos).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




