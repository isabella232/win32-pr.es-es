---
title: Mensaje EM_GETEDITSTYLE (RichEdit. h)
description: Recupera las marcas de estilo de edición actuales.
ms.assetid: 568e51a4-0767-4a59-bf34-bc0281b5fe65
keywords:
- EM_GETEDITSTYLE controles de mensajes de Windows
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
ms.openlocfilehash: 9264338ea525cc0165e1ed942d90654b95357b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079487"
---
# <a name="em_geteditstyle-message"></a>\_Mensaje del GETEDITSTYLE em

Recupera las marcas de estilo de edición actuales.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve las marcas de estilo de edición actuales, que pueden incluir uno o varios de los valores siguientes:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Código devuelto</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>SES_BEEPONMAXTEXT</strong></dt> </dl></td>
<td>La edición enriquecida llamará al bip del sistema si el usuario intenta escribir más de los caracteres máximos.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_BIDI</strong></dt> </dl></td>
<td>Activa el procesamiento bidireccional. Esto se activa automáticamente en Rich Edit si alguno de los siguientes estilos de ventana está activo: <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a> <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>. Sin embargo, esta configuración es útil para controlar estos estilos de ventana cuando se usa una implementación personalizada de <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>ITextHost</strong></a> (valor predeterminado: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_CTFALLOWEMBED</strong></dt> </dl></td>
<td><strong>Windows XP con SP1</strong>: permite la inserción de objetos incrustados mediante TSF (valor predeterminado: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_CTFALLOWPROOFING</strong></dt> </dl></td>
<td><strong>Windows XP con SP1</strong>: permite sugerencias de revisión de TSF (valor predeterminado: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </dl></td>
<td><strong>Windows XP con SP1</strong>: permite las sugerencias de interacciones de TSF (valor predeterminado: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_CTFNOLOCK</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: no se permite el acceso de lectura y escritura del bloqueo TSF. Esto detiene la entrada TSF. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: se muestran fuentes con una ligadura Fi con las características OpenType predeterminadas, lo que da como resultado una tipografía mejorada (valor predeterminado: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_DRAFTMODE</strong></dt> </dl></td>
<td><strong>Windows XP con SP1</strong>: usar fuentes en modo de borrador para mostrar texto. El modo borrador es una opción de accesibilidad en la que el control muestra el texto con una sola fuente; la fuente viene determinada por la configuración del sistema para la fuente utilizada en los cuadros de mensaje. Por ejemplo, los usuarios accesibles pueden leer texto más fácilmente si es uniforme, en lugar de una combinación de fuentes y estilos (valor predeterminado: 0). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_EMULATE10</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: emular el comportamiento de RichEdit 1,0. <br/>
<blockquote>
[!Note]<br />
Si realmente desea este comportamiento, use el riched32.dll de Windows en lugar de riched20.dll o msftedit.dll. Riched32.dll tenía más funcionalidad.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_EMULATESYSEDIT</strong></dt> </dl></td>
<td>Cuando este bit está activado, la edición enriquecida intenta emular el control de edición del sistema (valor predeterminado: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </dl></td>
<td>Extiende el color de fondo hasta los bordes del rectángulo del cliente (valor predeterminado: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_HIDEGRIDLINES</strong></dt> </dl></td>
<td><strong>Windows XP con SP1</strong>: Si el ancho de las líneas de cuadrícula de la tabla es cero, no se muestran las líneas de cuadrícula. Esto es equivalente a la característica ocultar líneas de cuadrícula del menú Tabla de Word (valor predeterminado: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: cuando el cursor está sobre un vínculo, se muestra una información sobre herramientas con la dirección del vínculo de destino (valor predeterminado: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_LOGICALCARET</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: proporcione información de símbolo de intercalación lógica en lugar de un mapa de bits de símbolo de intercalación, como se describe en <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>ITextHost:: TxSetCaretPos</strong></a> (valor predeterminado: 0). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_LOWERCASE</strong></dt> </dl></td>
<td>Convierte todos los caracteres de entrada a minúsculas (valor predeterminado: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_MAPCPS</strong></dt> </dl></td>
<td>Obsoleto. No debe usarse.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_MULTISELECT</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: habilitación de la multiselección con selecciones de mouse individuales realizadas mientras se presiona la tecla Ctrl (valor predeterminado: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: no ajuste el alto de línea para el texto asiático oriental (valor predeterminado: 0, que ajusta el alto de línea en un 15%). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </dl></td>
<td>Envía <a href="en-link.md">EN_LINK</a> notificación de los vínculos que no tienen el foco.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_NOIME</strong></dt> </dl></td>
<td>No permite los IME para esta instancia del control Rich Edit (valor predeterminado: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </dl></td>
<td>Cuando este bit está activado, la edición enriquecida no comprueba la secuencia de texto escrito. Algunos lenguajes (como el tailandés y el vietnamita) requieren comprobar el orden de las secuencias de entrada antes de enviarlo a la memoria auxiliar (valor predeterminado: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </dl></td>
<td>Cuando se produce KillFocus, se desplaza al principio del texto (la posición del carácter es igual a 0) (valor predeterminado: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_SMARTDRAGDROP</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: agregar o eliminar un espacio según el contexto al quitar texto (valor predeterminado: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_USECRLF</strong></dt> </dl></td>
<td>Obsoleto. No debe usarse.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_WORDDRAGDROP</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: Si la opción seleccionar palabra está activa, asegúrese de que la ubicación de destino está en un límite de palabras (valor predeterminado: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_UPPERCASE</strong></dt> </dl></td>
<td>Convierte todos los caracteres de entrada a mayúsculas (valor predeterminado: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_USEAIMM</strong></dt> </dl></td>
<td>Usa el componente del método de entrada IMM activo que se incluye con Internet Explorer 4,0 o posterior (valor predeterminado: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_USEATFONT</strong></dt> </dl></td>
<td><strong>Windows XP con SP1</strong>: usa una @ Font, que está diseñada para texto vertical; se usa con el estilo de ventana <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> . El nombre de @ Font comienza con el símbolo @, por ejemplo, &quot; @Batang &quot; (valor predeterminado: 0, pero se activa automáticamente para el diseño de texto vertical). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_USECTF</strong></dt> </dl></td>
<td><strong>Windows XP con SP1</strong>: activa la compatibilidad con TSF. (valor predeterminado: 0)<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </dl></td>
<td>Activa la traducción de CRCRLFs a CRs. Cuando este bit está activado y se lee un archivo en, todas las instancias de CRCRLF se convertirán en un sistema informatizado de modo interno. Esto afectará al ajuste del texto. Tenga en cuenta que si este tipo de archivo se guarda como texto sin formato, el sistema de almacenamiento de archivos de almacenamiento se reemplazará por CRLFs. Este es el estándar. txt para texto sin formato (valor predeterminado: 0, que elimina CRCRLFs en la entrada). <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Edición enriquecida 3,0<br/>                                                              |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETEDITSTYLE em**](em-seteditstyle.md)
</dt> </dl>

 

