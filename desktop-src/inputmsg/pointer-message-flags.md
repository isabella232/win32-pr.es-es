---
title: Marcas de mensajes de puntero
description: Valores que se usan en varias macros de puntero (vea macros).
ms.assetid: C3AF232C-A68E-48DA-A8D3-4ECE6F19317A
topic_type:
- apiref
api_name:
- POINTER_MESSAGE_FLAG_NEW
- POINTER_MESSAGE_FLAG_INRANGE
- POINTER_MESSAGE_FLAG_INCONTACT
- POINTER_MESSAGE_FLAG_FIRSTBUTTON
- POINTER_MESSAGE_FLAG_SECONDBUTTON
- POINTER_MESSAGE_FLAG_THIRDBUTTON
- POINTER_MESSAGE_FLAG_FOURTHBUTTON
- POINTER_MESSAGE_FLAG_FIFTHBUTTON
- POINTER_MESSAGE_FLAG_PRIMARY
- POINTER_MESSAGE_FLAG_CONFIDENCE
- POINTER_MESSAGE_FLAG_CANCELED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 853566dc6db7cfafed6a73b9a1ba3032001f02cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105720224"
---
# <a name="pointer-message-flags"></a>Marcas de mensajes de puntero

Valores que se usan en varias macros de puntero (vea [macros](macros.md)).

<dl> <dt>

<span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Indica la llegada de un nuevo puntero.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Indica que este puntero sigue existiendo. Cuando no se establece esta marca, indica que el puntero tiene el intervalo de detección izquierdo.

Normalmente, esta marca no se establece solo cuando un puntero de desplazamiento deja el intervalo de detección (se establece **POINTER_FLAG_UPDATE** ) o cuando un puntero en contacto con una superficie de la ventana deja el intervalo de detección (se establece **POINTER_FLAG_UP** ).


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Indica que este puntero está en contacto con la superficie del digitalizador. Cuando no se establece esta marca, indica un puntero que mantiene el mouse.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Indica una acción principal, análoga a un botón primario del mouse.

Un puntero táctil tiene esta marca establecida cuando está en contacto con la superficie del digitalizador.

Un puntero de pluma tiene esta marca establecida cuando está en contacto con la superficie del digitalizador sin presionar ningún botón.

Un puntero del mouse tiene esta marca establecida cuando el botón primario del mouse está presionado.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Indica una acción secundaria, análoga a un botón secundario del mouse hacia abajo.

Un puntero táctil no usa esta marca.

Un puntero de lápiz tiene esta marca establecida cuando está en contacto con la superficie del digitalizador con el botón de barril del lápiz presionado.

Un puntero del mouse tiene esta marca establecida cuando el botón secundario del mouse está presionado.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Análogo a un botón de rueda del mouse hacia abajo.

Un puntero táctil no usa esta marca.

Un puntero de lápiz no usa esta marca.

Un puntero del mouse tiene esta marca establecida cuando el botón de la rueda del mouse está presionado.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Análogo a un botón de la primera tecla del mouse extendido (XButton1).

Un puntero táctil no usa esta marca.

Un puntero de lápiz no usa esta marca.

Un puntero del mouse tiene esta marca establecida cuando el botón del primer Mouse extendido (XBUTTON1) está inactivo.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Análogo a un segundo botón de mouse extendido (XButton2).

Un puntero táctil no usa esta marca.

Un puntero de lápiz no usa esta marca.

Un puntero del mouse tiene esta marca establecida cuando el botón del segundo Mouse extendido (XBUTTON2) está inactivo.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Indica que este puntero se ha designado como puntero primario. Un puntero primario es un puntero único que puede realizar acciones más allá de las que están disponibles para los punteros no principales. Por ejemplo, cuando un puntero primario establece contacto con la superficie de una ventana, puede proporcionar a la ventana una oportunidad de activar mediante el envío de un mensaje de WM_POINTERACTIVATE.

El puntero principal se identifica a partir de todas las interacciones del usuario actual en el sistema (mouse, táctil, lápiz, etc.). Por lo tanto, es posible que el puntero principal no esté asociado a la aplicación. El primer contacto en una interacción multitáctil se establece como el puntero principal. Una vez que se identifica un puntero principal, todos los contactos deben levantarse antes de que se pueda identificar un nuevo contacto como puntero principal. En el caso de las aplicaciones que no procesan la entrada de puntero, solo los eventos del puntero primario se promueven a los eventos del mouse.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



La confianza es una sugerencia del dispositivo de origen sobre si el puntero representa una interacción intencionada o intencional, que es especialmente relevante para los punteros de PT_TOUCH en los que una interacción accidental (como con la palma de la mano) puede desencadenar la entrada. La presencia de esta marca indica que el dispositivo de origen tiene una alta confianza de que esta entrada forma parte de una interacción prevista.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Indica que el puntero se está desasociando de una manera anómala, como cuando el sistema recibe una entrada no válida para el puntero o cuando un dispositivo con punteros activos se parte repentinamente. Si la aplicación que recibe la entrada está en una posición para hacerlo, debe tratar la interacción como no completada e invertir los efectos del puntero en cuestión.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

XBUTTON1 y XBUTTON2 son botones adicionales que se usan en muchos dispositivos de mouse. Devuelven los mismos datos que los botones estándar del mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes](constants.md)
</dt> <dt>

[Macros](macros.md)
</dt> </dl>

 

 





