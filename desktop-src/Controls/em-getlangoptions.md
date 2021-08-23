---
title: EM_GETLANGOPTIONS mensaje (Richedit.h)
description: Obtiene la configuración de opciones de un control de edición enriquecido para el Editor de métodos de entrada (IME) y la compatibilidad con idiomas asiáticos.
ms.assetid: 9fd9d27c-7713-454e-b49f-8ecdba848d2e
keywords:
- EM_GETLANGOPTIONS controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6e3fa3602259ff0b754c79c69d91048c68c60b2703d4cd06a7da4630fcdf646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800205"
---
# <a name="em_getlangoptions-message"></a>Mensaje \_ EM GETLANGOPTIONS

Obtiene la configuración de opciones de un control de edición enriquecido para el Editor de métodos de entrada (IME) y la compatibilidad con idiomas asiáticos.

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

Devuelve la configuración del IME y del idioma asiático, que puede ser cero o más de los valores siguientes.



| Código devuelto                                                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**AUTOFONT \_ DEL DEPARTAMENTO DE MONETARIOS**</dt> </dl>                    | Si se establece esta marca, el control cambia automáticamente las fuentes cuando el usuario cambia explícitamente a un diseño de teclado diferente. Resulta útil desactivar **EL \_ AUTOFONT DE IMF para** fuentes Unicode universales. Esta opción está activada de forma predeterminada (1).<br/>                                                                                                                                                                     |
| <dl> <dt>**IMF \_ AUTOFONTSIZEADJUST**</dt> </dl>          | Si se establece esta marca, el control escala los tamaños de fuente enlazados a fuentes a partir del tamaño del punto de inserción según el script. Por ejemplo, las fuentes de Asia son ligeramente más grandes que las occidental. Esta opción está activada de forma predeterminada (1).<br/>                                                                                                                                                                                              |
| <dl> <dt>**AUTOKEYBOARD DE FONDO \_ MONETARIO**</dt> </dl>                | Si se establece esta marca, el control cambia automáticamente el diseño del teclado cuando el usuario cambia explícitamente a otra fuente o cuando el usuario cambia explícitamente el punto de inserción a una nueva ubicación del texto. Se activa automáticamente para los controles bidireccionales. Para todos los demás controles, está desactivado de forma predeterminada. Esta opción está desactivada de forma predeterminada (0).<br/>                                 |
| <dl> <dt>**IMF \_ DISABLEAUTOBIDIAUTOKEYBOARD**</dt> </dl> | **Windows 8:** si se establece esta marca, el control usa lógica neutra del lenguaje para el cambio automático de teclado. Esta opción está desactivada de forma predeterminada (0).<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**DUALFONT \_ DEL FONDO MONETARIO**</dt> </dl>                    | Si se establece esta marca, el control usa el modo de fuente dual. Se usa para la compatibilidad con idiomas asiáticos. El control usa una fuente en inglés para texto ASCII y una fuente de Asia para texto asiático. Esta opción está activada de forma predeterminada (1).<br/>                                                                                                                                                                                                   |
| <dl> <dt>**\_IMEALWAYSSENDNOTIFY DE IMEALWAYS**</dt> </dl>         | Esta marca controla cómo el control rich edit notifica al cliente durante la composición de IME: <br/> 0: no hay [ \_ notificaciones EN CHANGE](en-change.md) [o EN \_ SELCHANGE](en-selchange.md) durante un estado indeterminado. Envíe una notificación cuando llegue la cadena final. Este es el valor predeterminado.<br/> 1: Envíe [eventos EN \_ CHANGE](en-change.md) [y EN \_ SELCHANGE](en-selchange.md) durante un estado indeterminado.<br/> |
| <dl> <dt>**\_IMECANCELCOMPLETE DE IMECANCELCOMPLETE**</dt> </dl>           | Esta marca determina cómo el control usa la cadena de composición de un IME si el usuario la cancela. Si se establece este marcador, el control descarta la cadena de composición. Si no se establece este marcador, el control utiliza la cadena de la composición como la cadena del resultado. Esta opción está desactivada de forma predeterminada (0).<br/>                                                                                                              |
| <dl> <dt>**\_NOIMPLICITLANG PARA EL FONDO MONETARIO**</dt> </dl>              | **Windows 8:** si se establece esta marca, deshabilite la marca de entrada de teclado con el idioma del teclado y asegurarse de que los valores de idioma que no son de Asia Oriental sean compatibles con el carácter de carácter. Esta opción está desactivada de forma predeterminada (0). <br/>                                                                                                                                                                             |
| <dl> <dt>**IMF \_ NOKBDLIDFIXUP**</dt> </dl>               | **Windows 8:** si se establece esta marca, el control rich edit deshabilita la marcación del idioma del teclado en un control vacío. Esta opción está desactivada de forma predeterminada (0).<br/>                                                                                                                                                                                                                                                       |
| <dl> <dt>**REVISIÓN \_ ORTOGRÁFICA DEL FONDO MONETARIO**</dt> </dl>               | **Windows 8:** si se establece esta marca, el control rich edit activa la revisión ortográfica. Esta opción está desactivada de forma predeterminada (0). <br/>                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**\_TKBAUTOCORRECTION DEL FONDO MONETARIO**</dt> </dl>           | **Windows 8:** si se establece esta marca, habilite la autocorrección de teclado táctil. Esta opción está desactivada de forma predeterminada (0). <br/>                                                                                                                                                                                                                                                                                                  |
| <dl> <dt>**\_TKBPREDICTION DEL FONDO MONETARIO**</dt> </dl>               | **Windows 10:** omitido.<br/> **Windows 8:** si se establece esta marca, el control rich edit habilita la predicción de teclado táctil. Esta opción está desactivada de forma predeterminada (0). <br/>                                                                                                                                                                                                                                        |
| <dl> <dt>**\_UIFONTS DEL DEPARTAMENTO DE MONETARIOS**</dt> </dl>                     | Use fuentes predeterminadas de la interfaz de usuario. Esta opción está desactivada de forma predeterminada (0).<br/>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Comentarios

La **marca \_ AUTOFONT de IMF** está establecida de forma predeterminada. Las marcas **\_ IMECANCELCOMPLETE y** **\_ AUTOKEYBOARD** de IMF se borran de forma predeterminada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ SETLANGOPTIONS**](em-setlangoptions.md)
</dt> <dt>

[**EM \_ SETLIMITTEXT**](em-setlimittext.md)
</dt> </dl>

 

 





