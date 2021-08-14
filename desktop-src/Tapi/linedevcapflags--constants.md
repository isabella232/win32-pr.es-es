---
description: Las constantes de marca de bits LINEDEVCAPFLAGS son una colección de valores booleanos que \_ describen varias funcionalidades del dispositivo de línea.
ms.assetid: 0c537488-9fb9-4961-bd0a-1937aefc0b08
title: LINEDEVCAPFLAGS_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2d54acf1855bc09d9b2160e1ae681b25ff1de8ce310049fd4aabf4af6f8f2f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761722"
---
# <a name="linedevcapflags_-constants"></a>Constantes LINEDEVCAPFLAGS \_

Las constantes de marca de bits **LINEDEVCAPFLAGS \_** son una colección de valores booleanos que describen varias funcionalidades del dispositivo de línea.

<dl> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**LINEDEVCAPFLAGS \_ CALLHUB**
</dt> <dd> <dl> <dt>



Indica si se admiten centros de llamadas en esta línea. Esta marca solo se expone a las aplicaciones que negocian una versión tapi de la versión 3.0 o posterior.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**LINEDEVCAPFLAGS \_ CALLHUBTRACKING**
</dt> <dd> <dl> <dt>



Indica si se admite el seguimiento del centro de llamadas en esta línea. Esta marca solo se expone a las aplicaciones que negocian una versión tapi de la versión 3.0 o posterior.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**LINEDEVCAPFLAGS \_ CLOSEDROP**
</dt> <dd> <dl> <dt>



Especifica lo que sucede cuando se cierra una línea abierta mientras la aplicación tiene llamadas activas en la línea. Si **es TRUE,** el proveedor de servicios quita (borra) todas las llamadas activas en la línea cuando la última aplicación que ha abierto la línea la cierra [**con lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose). Si **es FALSE,** el proveedor de servicios no quitará las llamadas activas en estos casos. En su lugar, las llamadas permanecen activas y bajo control de dispositivos externos. Normalmente, un proveedor de servicios establece este bit en **FALSE** si hay algún otro dispositivo que pueda mantener activa la llamada; por ejemplo, si una línea análoga tiene el equipo y el teléfono establecidos ambos se conectan directamente a ellos en una configuración de línea de entidad, el teléfono dehook mantendrá activa automáticamente la llamada incluso después de que el equipo se apague.

Las aplicaciones deben comprobar esta marca para determinar si se debe advertir al usuario (con un cuadro de diálogo Aceptar/Cancelar) que se perderán las llamadas activas.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**LINEDEVCAPFLAGS \_ CROSSADDRCONF**
</dt> <dd> <dl> <dt>



Especifica si se pueden conferenciar llamadas en direcciones diferentes de esta línea.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**LINEDEVCAPFLAGS \_ DIALBILLING**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**LINEDEVCAPFLAGS \_ DIALDIALTONE**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**LINEDEVCAPFLAGS \_ DIALQUIET**
</dt> <dd> <dl> <dt>



Estas marcas indican si el modificador de cadena marcable "$", "@" o "W" es compatible con un dispositivo de línea determinado. Es **TRUE si** se admite el modificador ; de lo contrario, **FALSE**. El "?" (pedir al usuario que siga marcando) nunca es compatible con un dispositivo de línea. Estas marcas permiten a una aplicación determinar por adelantado qué modificadores darían lugar a la generación de lineerr. La aplicación tiene la opción de examinar previamente cadenas dialables para caracteres no admitidos o pasar la cadena "sin procesar" de [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) directamente al proveedor como parte de funciones como [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) o [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) y permitir que la función genere un error para que le diga qué modificador no admitido se produce primero en la cadena.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**LINEDEVCAPFLAGS \_ HIGHCOMP**
</dt> <dd> <dl> <dt>



Especifica si se admiten elementos de información de compatibilidad de alto nivel en esta línea.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**LINEDEVCAPFLAGS \_ LOWCOMP**
</dt> <dd> <dl> <dt>



Especifica si se admiten elementos de información de compatibilidad de bajo nivel en esta línea.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**LINEDEVCAPFLAGS \_ MEDIACONTROL**
</dt> <dd> <dl> <dt>



Especifica si las operaciones de control multimedia están disponibles para las llamadas en esta línea.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**LINEDEVCAPFLAGS \_ MSP**
</dt> <dd> <dl> <dt>



Indica si un proveedor de Media Service (MSP) está asociado a la línea. Esta marca solo se expone a las aplicaciones que negocian una versión tapi de la versión 3.0 o posterior.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**LINEDEVCAPFLAGS \_ MULTIPLEADDR**
</dt> <dd> <dl> <dt>



Especifica si [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineDial,**](/windows/desktop/api/Tapi/nf-tapi-linedial) [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)o [**TSPI \_ lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) puede tratar con varias direcciones a la vez (como para la multiplexación inversa).


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**LINEDEVCAPFLAGS \_ PRIVATEOBJECTS**
</dt> <dd> <dl> <dt>



Indica si se [han implementado interfaces](./provider-specific-interfaces.md) específicas del proveedor. Esta marca solo se expone a las aplicaciones que negocian una versión tapi de la versión 3.0 o posterior.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Sin extensibilidad. Los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)
</dt> </dl>

 

