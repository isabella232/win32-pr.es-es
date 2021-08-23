---
title: Marcas de mensaje de puntero
description: Valores que se usan en varias macros de puntero (vea Macros).
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
ms.openlocfilehash: 70d329c6a48eb92f6f50ff49d5543c2aaf5cfc3ce9ef23b48290c7aa029eecf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602358"
---
# <a name="pointer-message-flags"></a>Marcas de mensaje de puntero

Valores que se usan en varias macros de puntero (vea [Macros](macros.md)).

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



Indica que este puntero sigue existiendo. Cuando no se establece esta marca, indica que el puntero tiene un intervalo de detección izquierdo.

Normalmente, esta marca no se establece solo cuando un puntero que mantiene el puntero deja el intervalo de detección (se establece **POINTER_FLAG_UPDATE)** o cuando un puntero en contacto con una superficie de ventana deja el intervalo de **detección (POINTER_FLAG_UP** está establecido).


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Indica que este puntero está en contacto con la superficie del digitalizador. Cuando no se establece esta marca, indica un puntero que mantiene el puntero.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Indica una acción principal, análoga a un botón izquierdo del mouse hacia abajo.

Un puntero táctil tiene esta marca establecida cuando está en contacto con la superficie del digitalizador.

Un puntero de lápiz tiene esta marca establecida cuando está en contacto con la superficie del digitalizador sin botones presionados.

Un puntero del mouse tiene esta marca establecida cuando el botón izquierdo del mouse está apagado.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Indica una acción secundaria, análoga a un botón derecho del mouse hacia abajo.

Un puntero táctil no usa esta marca.

Un puntero de lápiz tiene esta marca establecida cuando está en contacto con la superficie del digitalizador con el botón de lápiz presionado.

Un puntero del mouse tiene esta marca establecida cuando el botón derecho del mouse está apagado.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Análogo a un botón de rueda del mouse hacia abajo.

Un puntero táctil no usa esta marca.

Un puntero de lápiz no usa esta marca.

Un puntero del mouse tiene esta marca establecida cuando el botón de rueda del mouse está apagado.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Análogo a un primer botón extendido del mouse (XButton1) hacia abajo.

Un puntero táctil no usa esta marca.

Un puntero de lápiz no usa esta marca.

Un puntero del mouse tiene esta marca establecida cuando el primer botón extendido del mouse (XBUTTON1) está apagado.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Similar a un segundo botón extendido del mouse (XButton2) hacia abajo.

Un puntero táctil no usa esta marca.

Un puntero de lápiz no usa esta marca.

Un puntero del mouse tiene esta marca establecida cuando el segundo botón extendido del mouse (XBUTTON2) está apagado.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Indica que este puntero se ha designado como puntero principal. Un puntero principal es un puntero único que puede realizar acciones más allá de las disponibles para los punteros que no son primarios. Por ejemplo, cuando un puntero principal se pone en contacto con la superficie de una ventana, puede proporcionar a la ventana una oportunidad de activarla WM_POINTERACTIVATE mensaje.

El puntero principal se identifica a partir de todas las interacciones del usuario actuales en el sistema (mouse, táctil, lápiz, entre otras). Por lo tanto, es posible que el puntero principal no esté asociado a la aplicación. El primer contacto de una interacción multitáccte se establece como puntero principal. Una vez identificado un puntero principal, todos los contactos deben elevarse antes de que un nuevo contacto se pueda identificar como puntero principal. En el caso de las aplicaciones que no procesan la entrada de puntero, solo los eventos del puntero principal se promueven a eventos del mouse.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



La confianza es una sugerencia del dispositivo de origen sobre si el puntero representa una interacción intencionada o accidental, que es especialmente relevante para los punteros PT_TOUCH donde una interacción accidental (como con la mano) puede desencadenar la entrada. La presencia de esta marca indica que el dispositivo de origen tiene una gran confianza en que esta entrada forma parte de una interacción prevista.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Indica que el puntero sale de forma anómala, como cuando el sistema recibe una entrada no válida para el puntero o cuando un dispositivo con punteros activos sale repentinamente. Si la aplicación que recibe la entrada está en posición de hacerlo, debe tratar la interacción como no completada e invertir los efectos del puntero en cuestión.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

XBUTTON1 y XBUTTON2 son botones adicionales que se usan en muchos dispositivos del mouse. Devuelven los mismos datos que los botones estándar del mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes](constants.md)
</dt> <dt>

[Macros](macros.md)
</dt> </dl>

 

 





