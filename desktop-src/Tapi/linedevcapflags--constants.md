---
description: Las \_ constantes de marcador de bits LINEDEVCAPFLAGS son una colección de valores booleanos que describen varias funcionalidades de dispositivo de línea.
ms.assetid: 0c537488-9fb9-4961-bd0a-1937aefc0b08
title: Constantes de LINEDEVCAPFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffefca75c00fdf09b1886affbff7f0ea90bab6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681064"
---
# <a name="linedevcapflags_-constants"></a>Constantes de LINEDEVCAPFLAGS \_

Las constantes de marcador de bits **LINEDEVCAPFLAGS \_** son una colección de valores booleanos que describen varias funcionalidades de dispositivo de línea.

<dl> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**LINEDEVCAPFLAGS \_ CALLHUB**
</dt> <dd> <dl> <dt>



Indica si se admiten los concentradores de llamadas en esta línea. Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 3,0 o superior.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**LINEDEVCAPFLAGS \_ CALLHUBTRACKING**
</dt> <dd> <dl> <dt>



Indica si se admite el seguimiento del centro de llamadas en esta línea. Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 3,0 o superior.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**LINEDEVCAPFLAGS \_ CLOSEDROP**
</dt> <dd> <dl> <dt>



Especifica lo que ocurre cuando se cierra una línea abierta mientras la aplicación tiene llamadas activas en la línea. Si **es true**, el proveedor de servicios quita (borra) todas las llamadas activas en la línea cuando la última aplicación que ha abierto la línea la cierra con [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose). Si **es false**, el proveedor de servicios no quita las llamadas activas en estos casos. En su lugar, las llamadas permanecen activas y bajo el control de dispositivos externos. Normalmente, un proveedor de servicios establece este bit en **false** si hay algún otro dispositivo que pueda mantener activa la llamada (por ejemplo, si una línea analógica tiene el equipo y el teléfono conectados ambos) se conectan directamente a ellos en una configuración de línea de entidad, el teléfono OffHook mantendrá la llamada activa automáticamente incluso después de que el equipo se apague.

Las aplicaciones deben comprobar esta marca para determinar si se debe advertir al usuario (con un cuadro de diálogo de aceptar o cancelar) que las llamadas activas se perderán.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**LINEDEVCAPFLAGS \_ CROSSADDRCONF**
</dt> <dd> <dl> <dt>



Especifica si se pueden realizar conferencias en las llamadas en diferentes direcciones de esta línea.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**LINEDEVCAPFLAGS \_ DIALBILLING**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**LINEDEVCAPFLAGS \_ DIALDIALTONE**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**LINEDEVCAPFLAGS \_ DIALQUIET**
</dt> <dd> <dl> <dt>



Estas marcas indican si se admite el modificador de cadena de marcado "$", "@" o "W" para un dispositivo de línea determinado. Es **true** si se admite el modificador; en caso contrario, **false**. El (solicitar al usuario que continúe el marcado) nunca es compatible con un dispositivo de línea. Estas marcas permiten a una aplicación determinar por adelantado qué modificadores darían lugar a la generación de un LINEERR. La aplicación tiene la opción de buscar previamente cadenas marcables para los caracteres no admitidos o de pasar la cadena "sin formato" de [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) directamente al proveedor como parte de funciones como [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) o [**lineales**](/windows/desktop/api/Tapi/nf-tapi-linedial) y permitir que la función genere un error para indicar que el modificador no admitido se produce en primer lugar en la cadena.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**LINEDEVCAPFLAGS \_ HIGHLEVCOMP**
</dt> <dd> <dl> <dt>



Especifica si se admiten elementos de información de compatibilidad de alto nivel en esta línea.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**LINEDEVCAPFLAGS \_ LOWLEVCOMP**
</dt> <dd> <dl> <dt>



Especifica si se admiten elementos de información de compatibilidad de bajo nivel en esta línea.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**LINEDEVCAPFLAGS \_ MEDIACONTROL**
</dt> <dd> <dl> <dt>



Especifica si las operaciones de control de medios están disponibles para las llamadas en esta línea.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**LINEDEVCAPFLAGS \_ MSP**
</dt> <dd> <dl> <dt>



Indica si un proveedor de servicios multimedia (MSP) está asociado a la línea. Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 3,0 o superior.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**LINEDEVCAPFLAGS \_ MULTIPLEADDR**
</dt> <dd> <dl> <dt>



Especifica si [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineal**](/windows/desktop/api/Tapi/nf-tapi-linedial), [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)o [**TSPI es \_**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) capaz de tratar con varias direcciones a la vez (como para multiplexación inversa).


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**LINEDEVCAPFLAGS \_ PRIVATEOBJECTS**
</dt> <dd> <dl> <dt>



Indica si se han implementado [interfaces específicas del proveedor](./provider-specific-interfaces.md) . Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 3,0 o superior.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**Fino**](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)
</dt> </dl>

 

