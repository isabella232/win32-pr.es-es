---
title: EM_GETEDITSTYLE mensaje (Richedit.h)
description: Recupera las marcas de estilo de edición actuales.
ms.assetid: 568e51a4-0767-4a59-bf34-bc0281b5fe65
keywords:
- EM_GETEDITSTYLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 220138a63628df310e316b6042045b7ca04ccbba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062194"
---
# <a name="em_geteditstyle-message"></a>Mensaje \_ GETEDITSTYLE de EM

Recupera las marcas de estilo de edición actuales.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve las marcas de estilo de edición actuales, que pueden incluir uno o varios de los valores siguientes:




| Código devuelto | Descripción | 
|-------------|-------------|
| <dl><dt><strong>SES_BEEPONMAXTEXT</strong></dt></dl> | Rich Edit llamará al beeper del sistema si el usuario intenta escribir más de los caracteres máximos.<br /> | 
| <dl><dt><strong>SES_BIDI</strong></dt></dl> | Activa el procesamiento bidireccional. Rich Edit activa automáticamente esta opción si alguno de los siguientes estilos de ventana está activo: <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>. Sin embargo, esta configuración es útil para controlar estos estilos de ventana cuando se usa una implementación personalizada de <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>ITextHost</strong></a> (valor predeterminado: 0).<br /> | 
| <dl><dt><strong>SES_CTFALLOWEMBED</strong></dt></dl> | <strong>Windows XP con SP1:</strong>permite insertar objetos incrustados mediante TSF (valor predeterminado: 0).<br /> | 
| <dl><dt><strong>SES_CTFALLOWPROOFING</strong></dt></dl> | <strong>Windows XP con SP1:</strong>permite sugerencias de prueba de TSF (valor predeterminado: 0).<br /> | 
| <dl><dt><strong>SES_CTFALLOWSMARTTAG</strong></dt></dl> | <strong>Windows XP con SP1:</strong>permite sugerencias de SmartTag de TSF (valor predeterminado: 0).<br /> | 
| <dl><dt><strong>SES_CTFNOLOCK</strong></dt></dl> | <strong>Windows 8:</strong>no permitir el acceso de lectura y escritura del bloqueo de TSF. Esto pausa la entrada de TSF. <br /> | 
| <dl><dt><strong>SES_DEFAULTLATINLIGA</strong></dt></dl> | <strong>Windows 8:</strong>las fuentes con una fi ligadura se muestran con características predeterminadas de OpenType, lo que da lugar a una tipografía mejorada (valor predeterminado: 0). <br /> | 
| <dl><dt><strong>SES_DRAFTMODE</strong></dt></dl> | <strong>Windows XP con SP1:</strong>use fuentes en modo borrador para mostrar texto. El modo borrador es una opción de accesibilidad donde el control muestra el texto con una sola fuente; la fuente viene determinada por la configuración del sistema para la fuente utilizada en los cuadros de mensaje. Por ejemplo, los usuarios accesibles pueden leer texto más fácilmente si es uniforme, en lugar de una combinación de fuentes y estilos (valor predeterminado: 0). <br /> | 
| <dl><dt><strong>SES_EMULATE10</strong></dt></dl> | <strong>Windows 8:</strong>emular el comportamiento de RichEdit 1.0. <br /><blockquote>[!Note]<br />Si realmente desea este comportamiento, use el Windows riched32.dll en lugar de riched20.dll o msftedit.dll. Riched32.dll tenía más funcionalidad.</blockquote><br /> | 
| <dl><dt><strong>SES_EMULATESYSEDIT</strong></dt></dl> | Cuando este bit está en estado on, rich edit intenta emular el control de edición del sistema (valor predeterminado: 0).<br /> | 
| <dl><dt><strong>SES_EXTENDBACKCOLOR</strong></dt></dl> | Extiende el color de fondo hasta los bordes del rectángulo del cliente (valor predeterminado: 0).<br /> | 
| <dl><dt><strong>SES_HIDEGRIDLINES</strong></dt></dl> | <strong>Windows XP con SP1:</strong>si el ancho de las líneas de cuadrícula de tabla es cero, no se muestran las líneas de cuadrícula. Esto equivale a la característica ocultar líneas de cuadrícula en el menú de tabla de Word (valor predeterminado: 0).<br /> | 
| <dl><dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt></dl> | <strong>Windows 8:</strong>cuando el cursor esté sobre un vínculo, muestre una información sobre herramientas con la dirección del vínculo de destino (valor predeterminado: 0). <br /> | 
| <dl><dt><strong>SES_LOGICALCARET</strong></dt></dl> | <strong>Windows 8:</strong>proporcione información del elemento de caret lógico en lugar de un mapa de bits de un elemento de caret, como se describe en <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>ITextHost::TxSetCaretPos</strong></a> (valor predeterminado: 0). <br /> | 
| <dl><dt><strong>SES_LOWERCASE</strong></dt></dl> | Convierte todos los caracteres de entrada a minúsculas (valor predeterminado: 0).<br /> | 
| <dl><dt><strong>SES_MAPCPS</strong></dt></dl> | Obsoleto. No debe usarse.<br /> | 
| <dl><dt><strong>SES_MULTISELECT</strong></dt></dl> | <strong>Windows 8:</strong>habilite la selección múltiple con selecciones individuales del mouse realizadas mientras se presiona la tecla Ctrl (valor predeterminado: 0). <br /> | 
| <dl><dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt></dl> | <strong>Windows 8:</strong>no ajustar el alto de línea para el texto de Asia Oriental (valor predeterminado: 0, que ajusta el alto de la línea en un 15 %). <br /> | 
| <dl><dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt></dl> | Envía <a href="en-link.md">EN_LINK</a> notificación de vínculos que no tienen el foco.<br /> | 
| <dl><dt><strong>SES_NOIME</strong></dt></dl> | No permite EME para esta instancia del control de edición enriquecido (valor predeterminado: 0).<br /> | 
| <dl><dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt></dl> | Cuando este bit está en, la edición enriquecte no comprueba la secuencia de texto con tipo. Algunos idiomas (como el tailandés y el tailandés) requieren comprobar el orden de la secuencia de entrada antes de enviarlo a la tienda de respaldo (valor predeterminado: 0).<br /> | 
| <dl><dt><strong>SES_SCROLLONKILLFOCUS</strong></dt></dl> | Cuando se produzca KillFocus, desplácese hasta el principio del texto (posición del carácter igual a 0) (valor predeterminado: 0).<br /> | 
| <dl><dt><strong>SES_SMARTDRAGDROP</strong></dt></dl> | <strong>Windows 8:</strong>agregue o elimine un espacio según el contexto al quitar texto (valor predeterminado: 0). <br /> | 
| <dl><dt><strong>SES_USECRLF</strong></dt></dl> | Obsoleto. No debe usarse.<br /> | 
| <dl><dt><strong>SES_WORDDRAGDROP</strong></dt></dl> | <strong>Windows 8:</strong>si la selección de palabras está activa, asegúrese de que la ubicación de colocación se encuentra en un límite de palabras (valor predeterminado: 0). <br /> | 
| <dl><dt><strong>SES_UPPERCASE</strong></dt></dl> | Convierte todos los caracteres de entrada en mayúsculas (valor predeterminado: 0).<br /> | 
| <dl><dt><strong>SES_USEAIMM</strong></dt></dl> | Usa el componente de método de entrada IMM activo que se incluye con Internet Explorer 4.0 o posterior (valor predeterminado: 0).<br /> | 
| <dl><dt><strong>SES_USEATFONT</strong></dt></dl> | <strong>Windows XP con SP1:</strong>usa una fuente @ diseñada para texto vertical; se usa con el estilo <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> ventana. El nombre de una fuente @ comienza con el símbolo @ , por ejemplo, " @Batang " (valor predeterminado: 0, pero se activa automáticamente para el diseño de texto vertical). <br /> | 
| <dl><dt><strong>SES_USECTF</strong></dt></dl> | <strong>Windows XP con SP1:</strong>activa la compatibilidad con TSF. (valor predeterminado: 0)<br /> | 
| <dl><dt><strong>SES_XLTCRCRLFTOCR</strong></dt></dl> | Activa la traducción de CRCRLF a CR. Cuando este bit está en y se lee un archivo, todas las instancias de CRCRLF se convertirán internamente en CD duros. Esto afectará al ajuste de texto. Tenga en cuenta que si este tipo de archivo se guarda como texto sin formato, las CRR se reemplazarán por CRLF. Este es el .txt estándar para texto sin formato (valor predeterminado: 0, que elimina CRCRLFs en la entrada). <br /> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Rich Edit 3.0<br/>                                                              |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ SETEDITSTYLE**](em-seteditstyle.md)
</dt> </dl>

 

