---
title: Marcas de puntero
description: Valores que pueden aparecer en el campo pointerFlags de la estructura POINTER_INFO.
ms.assetid: CC3F8E21-F4FF-495C-922E-A3708D3F2093
topic_type:
- apiref
api_name:
- POINTER_FLAG_NONE
- POINTER_FLAG_NEW
- POINTER_FLAG_INRANGE
- POINTER_FLAG_INCONTACT
- POINTER_FLAG_FIRSTBUTTON
- POINTER_FLAG_SECONDBUTTON
- POINTER_FLAG_THIRDBUTTON
- POINTER_FLAG_FOURTHBUTTON
- POINTER_FLAG_FIFTHBUTTON
- POINTER_FLAG_PRIMARY
- POINTER_FLAG_CONFIDENCE
- POINTER_FLAG_CANCELED
- POINTER_FLAG_DOWN
- POINTER_FLAG_UPDATE
- POINTER_FLAG_UP
- POINTER_FLAG_WHEEL
- POINTER_FLAG_HWHEEL
- POINTER_FLAG_CAPTURECHANGED
- POINTER_FLAG_HASTRANSFORM
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 21a4191aa09bcb0cb9fda1a4c9bc011d978e203a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802899"
---
# <a name="pointer-flags"></a>Marcas de puntero

Valores que pueden aparecer en el campo **pointerFlags** de la estructura [**POINTER_INFO**](/previous-versions/windows/desktop/api) .

<dl> <dt>

<span id="POINTER_FLAG_NONE"></span><span id="pointer_flag_none"></span>**POINTER_FLAG_NONE**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Valor predeterminado


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_NEW"></span><span id="pointer_flag_new"></span>**POINTER_FLAG_NEW**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Indica la llegada de un nuevo puntero.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_INRANGE"></span><span id="pointer_flag_inrange"></span>**POINTER_FLAG_INRANGE**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Indica que este puntero sigue existiendo. Cuando no se establece esta marca, indica que el puntero tiene el intervalo de detección izquierdo.

Normalmente, esta marca no se establece solo cuando un puntero de desplazamiento deja el intervalo de detección (se establece **POINTER_FLAG_UPDATE** ) o cuando un puntero en contacto con una superficie de la ventana deja el intervalo de detección (se establece **POINTER_FLAG_UP** ).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_INCONTACT"></span><span id="pointer_flag_incontact"></span>**POINTER_FLAG_INCONTACT**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Indica que este puntero está en contacto con la superficie del digitalizador. Cuando no se establece esta marca, indica un puntero que mantiene el mouse.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_FIRSTBUTTON"></span><span id="pointer_flag_firstbutton"></span>**POINTER_FLAG_FIRSTBUTTON**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Indica una acción principal, análoga a un botón primario del mouse.

Un puntero táctil tiene esta marca establecida cuando está en contacto con la superficie del digitalizador.

Un puntero de pluma tiene esta marca establecida cuando está en contacto con la superficie del digitalizador sin presionar ningún botón.

Un puntero del mouse tiene esta marca establecida cuando el botón primario del mouse está presionado.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_SECONDBUTTON"></span><span id="pointer_flag_secondbutton"></span>**POINTER_FLAG_SECONDBUTTON**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Indica una acción secundaria, análoga a un botón secundario del mouse hacia abajo.

Un puntero táctil no usa esta marca.

Un puntero de lápiz tiene esta marca establecida cuando está en contacto con la superficie del digitalizador con el botón de barril del lápiz presionado.

Un puntero del mouse tiene esta marca establecida cuando el botón secundario del mouse está presionado.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_THIRDBUTTON"></span><span id="pointer_flag_thirdbutton"></span>**POINTER_FLAG_THIRDBUTTON**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Análogo a un botón de rueda del mouse hacia abajo.

Un puntero táctil no usa esta marca.

Un puntero de lápiz no usa esta marca.

Un puntero del mouse tiene esta marca establecida cuando el botón de la rueda del mouse está presionado.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_FOURTHBUTTON"></span><span id="pointer_flag_fourthbutton"></span>**POINTER_FLAG_FOURTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Análogo a un botón de la primera tecla del mouse extendido (XButton1).

Un puntero táctil no usa esta marca.

Un puntero de lápiz no usa esta marca.

Un puntero del mouse tiene esta marca establecida cuando el botón del primer Mouse extendido (XBUTTON1) está inactivo.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_FIFTHBUTTON"></span><span id="pointer_flag_fifthbutton"></span>**POINTER_FLAG_FIFTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Análogo a un segundo botón de mouse extendido (XButton2).

Un puntero táctil no usa esta marca.

Un puntero de lápiz no usa esta marca.

Un puntero del mouse tiene esta marca establecida cuando el botón del segundo Mouse extendido (XBUTTON2) está inactivo.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_PRIMARY"></span><span id="pointer_flag_primary"></span>**POINTER_FLAG_PRIMARY**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Indica que este puntero se ha designado como puntero primario. Un puntero primario es un puntero único que puede realizar acciones más allá de las que están disponibles para los punteros no principales. Por ejemplo, cuando un puntero primario establece contacto con la superficie de una ventana, puede proporcionar a la ventana una oportunidad de activar mediante el envío de un mensaje de [**WM_POINTERACTIVATE**](wm-pointeractivate.md) .

El puntero principal se identifica a partir de todas las interacciones del usuario actual en el sistema (mouse, táctil, lápiz, etc.). Por lo tanto, es posible que el puntero principal no esté asociado a la aplicación. El primer contacto en una interacción multitáctil se establece como el puntero principal. Una vez que se identifica un puntero principal, todos los contactos deben levantarse antes de que se pueda identificar un nuevo contacto como puntero principal. En el caso de las aplicaciones que no procesan la entrada de puntero, solo los eventos del puntero primario se promueven a los eventos del mouse.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_CONFIDENCE"></span><span id="pointer_flag_confidence"></span>**POINTER_FLAG_CONFIDENCE**
</dt> <dd> <dl> <dt>

0x000004000
</dt> <dt>



La confianza es una sugerencia del dispositivo de origen sobre si el puntero representa una interacción intencionada o intencional, que es especialmente relevante para los punteros de PT_TOUCH en los que una interacción accidental (como con la palma de la mano) puede desencadenar la entrada. La presencia de esta marca indica que el dispositivo de origen tiene una alta confianza de que esta entrada forma parte de una interacción prevista.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_CANCELED"></span><span id="pointer_flag_canceled"></span>**POINTER_FLAG_CANCELED**
</dt> <dd> <dl> <dt>

0x000008000
</dt> <dt>



Indica que el puntero se está desasociando de una manera anómala, como cuando el sistema recibe una entrada no válida para el puntero o cuando un dispositivo con punteros activos se parte repentinamente. Si la aplicación que recibe la entrada está en una posición para hacerlo, debe tratar la interacción como no completada e invertir los efectos del puntero en cuestión.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_DOWN"></span><span id="pointer_flag_down"></span>**POINTER_FLAG_DOWN**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Indica que este puntero ha pasado a un estado de inactividad; es decir, se puso en contacto con la superficie del digitalizador.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_UPDATE"></span><span id="pointer_flag_update"></span>**POINTER_FLAG_UPDATE**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Indica que se trata de una actualización simple que no incluye los cambios de estado de puntero.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_UP"></span><span id="pointer_flag_up"></span>**POINTER_FLAG_UP**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Indica que este puntero ha pasado a un estado up; es decir, ha finalizado el contacto con la superficie del digitalizador.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_WHEEL"></span><span id="pointer_flag_wheel"></span>**POINTER_FLAG_WHEEL**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



Indica la entrada asociada a una rueda de puntero. En el caso de los punteros del mouse, es equivalente a la acción de la rueda de desplazamiento del mouse ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_HWHEEL"></span><span id="pointer_flag_hwheel"></span>**POINTER_FLAG_HWHEEL**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Indica la entrada asociada a una rueda h de puntero. En el caso de los punteros del mouse, es equivalente a la acción de la rueda de desplazamiento horizontal del mouse ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_CAPTURECHANGED"></span><span id="pointer_flag_capturechanged"></span>**POINTER_FLAG_CAPTURECHANGED**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



Indica que se ha capturado este puntero (asociado con) a otro elemento y el elemento original ha perdido la captura (vea [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md)).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_HASTRANSFORM"></span><span id="pointer_flag_hastransform"></span>**POINTER_FLAG_HASTRANSFORM**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Indica que este puntero tiene una transformación asociada.


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

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**POINTER_BUTTON_CHANGE_TYPE**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

