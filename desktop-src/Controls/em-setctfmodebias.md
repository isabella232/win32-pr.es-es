---
title: EM_SETCTFMODEBIAS mensaje (Richedit.h)
description: Establece el sesgo Text Services Framework modo de Text Services Framework (TSF) para un control de edición enriquecido.
ms.assetid: 17e3aac8-2ba8-4c06-bfd6-e118cfb82529
keywords:
- EM_SETCTFMODEBIAS controles de Windows mensaje
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
ms.openlocfilehash: fd6aa0f10b07092d9637d9e5a993848671ab6aa7e7eb610eca48c3df353c4a0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019513"
---
# <a name="em_setctfmodebias-message"></a>Mensaje \_ EM SETCTFMODEBIAS

Establece el sesgo Text Services Framework modo de Text Services Framework (TSF) para un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de sesgo de modo. Puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                                                     | Significado                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="CTFMODEBIAS_DEFAULT"></span><span id="ctfmodebias_default"></span><dl> <dt>**CTFMODEBIAS \_ PREDETERMINADO**</dt> </dl>                                           | No hay ningún sesgo de modo.<br/>                             |
| <span id="CTFMODEBIAS_FILENAME"></span><span id="ctfmodebias_filename"></span><dl> <dt>**CTFMODEBIAS \_ FILENAME**</dt> </dl>                                        | El sesgo es para un nombre de archivo.<br/>                         |
| <span id="CTFMODEBIAS_NAME"></span><span id="ctfmodebias_name"></span><dl> <dt>**CTFMODEBIAS \_ NAME**</dt> </dl>                                                    | El sesgo es un nombre.<br/>                             |
| <span id="CTFMODEBIAS_READING"></span><span id="ctfmodebias_reading"></span><dl> <dt>**LECTURA DE CTFMODEBIAS \_**</dt> </dl>                                           | El sesgo es para la lectura.<br/>                        |
| <span id="CTFMODEBIAS_DATETIME"></span><span id="ctfmodebias_datetime"></span><dl> <dt>**CTFMODEBIAS \_ DATETIME**</dt> </dl>                                        | El sesgo es una fecha u hora.<br/>                     |
| <span id="CTFMODEBIAS_CONVERSATION"></span><span id="ctfmodebias_conversation"></span><dl> <dt>**CTFMODEBIAS \_ CONVERSATION**</dt> </dl>                            | El sesgo es para una conversación.<br/>                     |
| <span id="CTFMODEBIAS_NUMERIC"></span><span id="ctfmodebias_numeric"></span><dl> <dt>**CTFMODEBIAS \_ NUMERIC**</dt> </dl>                                           | El sesgo es un número.<br/>                           |
| <span id="CTFMODEBIAS_HIRAGANA"></span><span id="ctfmodebias_hiragana"></span><dl> <dt>**CTFMODEBIAS \_ HIRAGANA**</dt> </dl>                                        | El sesgo es para las cadenas hiragana.<br/>                   |
| <span id="CTFMODEBIAS_KATAKANA"></span><span id="ctfmodebias_katakana"></span><dl> <dt>**CTFMODEBIAS \_ KATAKANA**</dt> </dl>                                        | El sesgo es para las cadenas katakana.<br/>                   |
| <span id="CTFMODEBIAS_HANGUL"></span><span id="ctfmodebias_hangul"></span><dl> <dt>**CTFMODEBIAS \_ HANGUL**</dt> </dl>                                              | El sesgo es para los caracteres Hangul.<br/>                  |
| <span id="CTFMODEBIAS_HALFWIDTHKATAKANA"></span><span id="ctfmodebias_halfwidthkatakana"></span><dl> <dt>**CTFMODEBIAS \_ HALFWIDTHAKANA**</dt> </dl>             | El sesgo es para cadenas katakana de ancho medio.<br/>        |
| <span id="CTFMODEBIAS_FULLWIDTHALPHANUMERIC"></span><span id="ctfmodebias_fullwidthalphanumeric"></span><dl> <dt>**CTFMODEBIAS \_ FULLWIDPHANUMERIC**</dt> </dl> | El sesgo es para los caracteres alfanuméricos de ancho completo.<br/> |
| <span id="CTFMODEBIAS_HALFWIDTHALPHANUMERIC"></span><span id="ctfmodebias_halfwidthalphanumeric"></span><dl> <dt>**CTFMODEBIAS \_ HALFWIDPHANUMERIC**</dt> </dl> | El sesgo es para caracteres alfanuméricos de ancho medio.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, el valor devuelto es el nuevo valor de sesgo del modo TSF. Si no se realiza correctamente, el valor devuelto es el valor de sesgo del modo TSF anterior.

## <a name="remarks"></a>Comentarios

Cuando una aplicación de Edición enriquecida de Microsoft usa TSF, puede seleccionar el sesgo del modo TSF. Este mensaje establece los criterios por los que aparece una opción alternativa en la parte superior de la lista para la selección.

Para establecer el sesgo de modo para el Editor de métodos de entrada (IME), use [**EM \_ SETIMEMODEBIAS**](em-setimemodebias.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp1\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ GETCTFMODEBIAS**](em-getctfmodebias.md)
</dt> <dt>

[**EM \_ SETIMEMODEBIAS**](em-setimemodebias.md)
</dt> </dl>

 

 





