---
title: Mensaje EM_GETLANGOPTIONS (RichEdit. h)
description: Obtiene la configuración de opciones de un control Rich Edit para la compatibilidad con el editor de métodos de entrada (IME) y el idioma asiático.
ms.assetid: 9fd9d27c-7713-454e-b49f-8ecdba848d2e
keywords:
- EM_GETLANGOPTIONS controles de mensajes de Windows
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
ms.openlocfilehash: a27254ccb10093059eb9161410f4e25efdc59306
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905040"
---
# <a name="em_getlangoptions-message"></a>\_Mensaje GETLANGOPTIONS em

Obtiene la configuración de opciones de un control Rich Edit para la compatibilidad con el editor de métodos de entrada (IME) y el idioma asiático.

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

Devuelve la configuración de idioma IME y asiático, que puede ser cero o más de los valores siguientes.



| Código devuelto                                                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**AUTOFUENTE IMF \_**</dt> </dl>                    | Si se establece esta marca, el control cambia automáticamente las fuentes cuando el usuario cambia explícitamente a otra distribución del teclado. Resulta útil desactivar la **\_ AUTOFUENTE IMF** para fuentes Unicode universales. Esta opción está activada de forma predeterminada (1).<br/>                                                                                                                                                                     |
| <dl> <dt>**AUTOFONTSIZEADJUST de IMF \_**</dt> </dl>          | Si se establece esta marca, el control escala los tamaños de fuente enlazados a fuentes del tamaño del punto de inserción según el script. Por ejemplo, las fuentes asiáticas son ligeramente mayores que las occidentales. Esta opción está activada de forma predeterminada (1).<br/>                                                                                                                                                                                              |
| <dl> <dt>**autokeyboard de IMF \_**</dt> </dl>                | Si se establece esta marca, el control cambia automáticamente la distribución del teclado cuando el usuario cambia explícitamente a una fuente diferente o cuando el usuario cambia explícitamente el punto de inserción a una nueva ubicación en el texto. Se activará automáticamente para los controles bidireccionales. Para todos los demás controles, está desactivado de forma predeterminada. Esta opción está desactivada de forma predeterminada (0).<br/>                                 |
| <dl> <dt>**DISABLEAUTOBIDIAUTOKEYBOARD de IMF \_**</dt> </dl> | **Windows 8**: si se establece esta marca, el control usa la lógica neutra de idioma para la conmutación automática de teclado. Esta opción está desactivada de forma predeterminada (0).<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**DUALFONT de IMF \_**</dt> </dl>                    | Si se establece esta marca, el control utiliza el modo de fuente dual. Se usa para la compatibilidad con idiomas asiáticos. El control usa una fuente de inglés para el texto ASCII y una fuente asiática para el texto asiático. Esta opción está activada de forma predeterminada (1).<br/>                                                                                                                                                                                                   |
| <dl> <dt>**IMEALWAYSSENDNOTIFY de IMF \_**</dt> </dl>         | Esta marca controla cómo el control Rich Edit notifica al cliente durante la composición del IME: <br/> 0: no hay ninguna notificación [en el \_ cambio](en-change.md) o [en \_ SELCHANGE](en-selchange.md) durante el estado indeterminado. Envía una notificación cuando entra en la cadena final. Este es el valor predeterminado.<br/> 1: enviar eventos in [ \_ Change](en-change.md) y [en \_ SELCHANGE](en-selchange.md) durante un estado indeterminado.<br/> |
| <dl> <dt>**IMECANCELCOMPLETE de IMF \_**</dt> </dl>           | Esta marca determina el modo en que el control utiliza la cadena de composición de un IME si el usuario lo cancela. Si se establece este marcador, el control descarta la cadena de composición. Si no se establece este marcador, el control utiliza la cadena de la composición como la cadena del resultado. Esta opción está desactivada de forma predeterminada (0).<br/>                                                                                                              |
| <dl> <dt>**NOIMPLICITLANG de IMF \_**</dt> </dl>              | **Windows 8**: si se establece esta marca, deshabilite la entrada del teclado de marca con el idioma del teclado y asegúrese de que los IDss de idiomas de Asia no oriental son compatibles con el repertorio de caracteres. Esta opción está desactivada de forma predeterminada (0). <br/>                                                                                                                                                                             |
| <dl> <dt>**NOKBDLIDFIXUP de IMF \_**</dt> </dl>               | **Windows 8**: si se establece esta marca, el control Rich Edit deshabilita el idioma del teclado en un control vacío. Esta opción está desactivada de forma predeterminada (0).<br/>                                                                                                                                                                                                                                                       |
| <dl> <dt>**\_revisión ortográfica de IMF**</dt> </dl>               | **Windows 8**: si se establece esta marca, el control Rich Edit activa la revisión ortográfica. Esta opción está desactivada de forma predeterminada (0). <br/>                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**TKBAUTOCORRECTION de IMF \_**</dt> </dl>           | **Windows 8**: si se establece esta marca, habilite la función de Autocorrección de teclado táctil. Esta opción está desactivada de forma predeterminada (0). <br/>                                                                                                                                                                                                                                                                                                  |
| <dl> <dt>**TKBPREDICTION de IMF \_**</dt> </dl>               | **Windows 10**: se omite.<br/> **Windows 8**: si se establece esta marca, el control Rich Edit habilita la predicción de teclado táctil. Esta opción está desactivada de forma predeterminada (0). <br/>                                                                                                                                                                                                                                        |
| <dl> <dt>**UIFONTS de IMF \_**</dt> </dl>                     | Usar fuentes predeterminadas de la interfaz de usuario. Esta opción está desactivada de forma predeterminada (0).<br/>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Observaciones

La marca de **\_ AUTOFUENTE IMF** está establecida de forma predeterminada. Las **marcas \_ autokeyboard** y **IMF \_ IMECANCELCOMPLETE** de IMF están desactivadas de forma predeterminada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_SETLANGOPTIONS em**](em-setlangoptions.md)
</dt> <dt>

[**\_SETLIMITTEXT em**](em-setlimittext.md)
</dt> </dl>

 

 





