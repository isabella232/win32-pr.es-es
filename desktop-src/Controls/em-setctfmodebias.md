---
title: Mensaje EM_SETCTFMODEBIAS (RichEdit. h)
description: Establece la diferencia del modo de Text Services Framework (TSF) para un control Rich Edit.
ms.assetid: 17e3aac8-2ba8-4c06-bfd6-e118cfb82529
keywords:
- EM_SETCTFMODEBIAS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b872fa5489c898ec4482ecdc094de7df6e3180be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535061"
---
# <a name="em_setctfmodebias-message"></a>\_Mensaje SETCTFMODEBIAS em

Establece la diferencia del modo de Text Services Framework (TSF) para un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de diferencia del modo. Puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                                                     | Significado                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="CTFMODEBIAS_DEFAULT"></span><span id="ctfmodebias_default"></span><dl> <dt>**\_valor predeterminado de CTFMODEBIAS**</dt> </dl>                                           | No hay ninguna diferencia de modo.<br/>                             |
| <span id="CTFMODEBIAS_FILENAME"></span><span id="ctfmodebias_filename"></span><dl> <dt>**\_nombre de archivo CTFMODEBIAS**</dt> </dl>                                        | La diferencia es con un nombre de archivo.<br/>                         |
| <span id="CTFMODEBIAS_NAME"></span><span id="ctfmodebias_name"></span><dl> <dt>**nombre de CTFMODEBIAS \_**</dt> </dl>                                                    | La diferencia es con un nombre.<br/>                             |
| <span id="CTFMODEBIAS_READING"></span><span id="ctfmodebias_reading"></span><dl> <dt>**lectura de CTFMODEBIAS \_**</dt> </dl>                                           | La diferencia es con la lectura.<br/>                        |
| <span id="CTFMODEBIAS_DATETIME"></span><span id="ctfmodebias_datetime"></span><dl> <dt>**CTFMODEBIAS \_ DateTime**</dt> </dl>                                        | La diferencia es una fecha o una hora.<br/>                     |
| <span id="CTFMODEBIAS_CONVERSATION"></span><span id="ctfmodebias_conversation"></span><dl> <dt>**CTFMODEBIAS \_ Conversation**</dt> </dl>                            | La diferencia es a una conversación.<br/>                     |
| <span id="CTFMODEBIAS_NUMERIC"></span><span id="ctfmodebias_numeric"></span><dl> <dt>**CTFMODEBIAS \_ Numeric**</dt> </dl>                                           | La diferencia es un número.<br/>                           |
| <span id="CTFMODEBIAS_HIRAGANA"></span><span id="ctfmodebias_hiragana"></span><dl> <dt>**CTFMODEBIAS \_ hiragana**</dt> </dl>                                        | La diferencia es con las cadenas hiragana.<br/>                   |
| <span id="CTFMODEBIAS_KATAKANA"></span><span id="ctfmodebias_katakana"></span><dl> <dt>**CTFMODEBIAS \_ katakana**</dt> </dl>                                        | La diferencia es a las cadenas katakana.<br/>                   |
| <span id="CTFMODEBIAS_HANGUL"></span><span id="ctfmodebias_hangul"></span><dl> <dt>**CTFMODEBIAS \_ HANGUL**</dt> </dl>                                              | La diferencia se debe a los caracteres hangul.<br/>                  |
| <span id="CTFMODEBIAS_HALFWIDTHKATAKANA"></span><span id="ctfmodebias_halfwidthkatakana"></span><dl> <dt>**CTFMODEBIAS \_ HALFWIDTHKATAKANA**</dt> </dl>             | La diferencia se debe a las cadenas katakana de ancho medio.<br/>        |
| <span id="CTFMODEBIAS_FULLWIDTHALPHANUMERIC"></span><span id="ctfmodebias_fullwidthalphanumeric"></span><dl> <dt>**CTFMODEBIAS \_ FULLWIDTHALPHANUMERIC**</dt> </dl> | La diferencia se debe a los caracteres alfanuméricos de ancho completo.<br/> |
| <span id="CTFMODEBIAS_HALFWIDTHALPHANUMERIC"></span><span id="ctfmodebias_halfwidthalphanumeric"></span><dl> <dt>**CTFMODEBIAS \_ HALFWIDTHALPHANUMERIC**</dt> </dl> | La diferencia se debe a caracteres alfanuméricos de ancho medio.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, el valor devuelto es el nuevo valor de diferencia del modo TSF. Si no se realiza correctamente, el valor devuelto es el valor de diferencia del modo TSF antiguo.

## <a name="remarks"></a>Observaciones

Cuando una aplicación de Microsoft Rich Edit usa TSF, puede seleccionar la diferencia del modo TSF. Este mensaje establece los criterios por los que aparece una opción alternativa en la parte superior de la lista para la selección.

Para establecer la diferencia de modo para el editor de métodos de entrada (IME), use [**em \_ SETIMEMODEBIAS**](em-setimemodebias.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP1 \[\]<br/>                                  |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_GETCTFMODEBIAS em**](em-getctfmodebias.md)
</dt> <dt>

[**\_SETIMEMODEBIAS em**](em-setimemodebias.md)
</dt> </dl>

 

 





