---
description: Las \_ constantes de marcador de bits LINETERMMODE describen distintos tipos de eventos en una línea telefónica que se pueden enrutar a un dispositivo terminal.
ms.assetid: 60af1687-8958-4918-be21-a13780c60974
title: Constantes de LINETERMMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e689e2e4e432d6cf804e64babd462e749e7e9e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679404"
---
# <a name="linetermmode_-constants"></a>Constantes de LINETERMMODE \_

Las constantes de marcador de bits **LINETERMMODE \_** describen distintos tipos de eventos en una línea telefónica que se pueden enrutar a un dispositivo terminal.

<dl> <dt>

<span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**botones de LINETERMMODE \_**
</dt> <dd> <dl> <dt>



Se trata de eventos de pulsación de botones enviados desde el terminal a la línea.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**LINETERMMODE \_ Mostrar**
</dt> <dd> <dl> <dt>



Esta es la información que se envía desde la línea al terminal.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**LINETERMMODE \_ conmutador**
</dt> <dd> <dl> <dt>



Se trata de eventos conmutador enviados desde el terminal a la línea.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**\_lámparas LINETERMMODE**
</dt> <dd> <dl> <dt>



Estos son los eventos de lámpara enviados desde la línea al terminal.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**LINETERMMODE \_ MEDIABIDIRECT**
</dt> <dd> <dl> <dt>



Este es el flujo multimedia bidireccional asociado a una llamada en la línea y el terminal. Use este valor cuando el enrutamiento de ambos canales unidireccionales de una secuencia multimedia de una llamada no se puede controlar de forma independiente.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**LINETERMMODE \_ MEDIAFROMLINE**
</dt> <dd> <dl> <dt>



Esta es la secuencia de medios unidireccionales de la línea al terminal asociada a una llamada en la línea. Use este valor cuando el enrutamiento de ambos canales unidireccionales de una secuencia multimedia de una llamada puede controlarse de forma independiente.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**LINETERMMODE \_ MEDIATOLINE**
</dt> <dd> <dl> <dt>



Esta es la secuencia de medios unidireccionales desde el terminal hasta la línea asociada a una llamada en la línea. Use este valor cuando el enrutamiento de ambos canales unidireccionales de una secuencia multimedia de una llamada puede controlarse de forma independiente.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**\_timbre LINETERMMODE**
</dt> <dd> <dl> <dt>



Esta es la información de control de timbre enviada desde el conmutador al terminal.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

Estas constantes describen las clases de secuencias de control e información que se pueden enrutar directamente entre un dispositivo de línea y un dispositivo de terminal (como un conjunto de teléfonos).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




