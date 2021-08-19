---
title: EM_GETEDITSTYLEEX mensaje (Richedit.h)
description: Recupera las marcas de estilo de edición extendida actuales.
ms.assetid: 3E81F7BB-404D-4465-982A-3CF6FD9359DA
keywords:
- EM_GETEDITSTYLEEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3c011a162bbf0a1822e68be6bd60f662551b3a22ecfca62c64ef8d01a605a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049315"
---
# <a name="em_geteditstyleex-message"></a>Mensaje \_ EM GETEDITSTYLEEX

Recupera las marcas de estilo de edición extendida actuales.


```C++
#define EM_GETEDITSTYLEEX       (WM_USER + 276)
```



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

Devuelve las marcas de estilo de edición extendidas, que pueden incluir uno o varios de los valores siguientes.



| Código devuelto                                                                                                | Descripción                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SES \_ EX \_ HANDLEFRIENDLYURL**</dt> </dl>  | Mostrar vínculos de nombre descriptivos con el mismo color de texto y sobrelinear como vínculos automáticos, siempre que no se use el formato temporal o que use el color automático de texto (valor predeterminado: 0).<br/>                                                                       |
| <dl> <dt>**SES \_ EX \_ MULTITOUCH**</dt> </dl>         | Habilite la compatibilidad táctil en Rich Edit. Esto incluye la selección, la selección del elemento de inserción y la invocación del menú contextual. Cuando no se establece esta marca, la función táctil se emula mediante comandos del mouse, que no tienen en cuenta las características específicas del modo táctil (valor predeterminado: 0). <br/>      |
| <dl> <dt>**SES \_ EX \_ NOACETATESELECTION**</dt> </dl> | Muestre el texto seleccionado mediante el texto Windows texto de selección y los colores de fondo en lugar del color de fondo de fondo (valor predeterminado: 0). <br/>                                                                                                               |
| <dl> <dt>**SES \_ EX \_ NOMATH**</dt> </dl>             | Deshabilite la inserción de zonas matemáticas (valor predeterminado: 1). Para habilitar la edición matemática y la visualización, envíe el mensaje [**EM \_ SETEDITSTYLEEX**](em-seteditstyleex.md) con *wParam* establecido en 0 y *lParam* establecido en **SES \_ EX \_ NOMATH**. <br/>                              |
| <dl> <dt>**SES \_ EX \_ NOTABLE**</dt> </dl>            | Deshabilite la inserción de tablas. El [**mensaje EM \_ INSERTTABLE**](em-inserttable.md) devuelve **E \_ FAIL** y se omiten las tablas RTF (valor predeterminado: 0). <br/>                                                                                                  |
| <dl> <dt>**SES \_ EX \_ USESINGLELINE**</dt> </dl>      | Habilite un control de varias líneas para que actúe como un control de una sola línea con la capacidad de desplazarse verticalmente cuando el alto de una sola línea es mayor que el alto de la ventana (valor predeterminado: 0). <br/>                                                                   |
| <dl> <dt>**SES \_ HIDETEMPFORMAT**</dt> </dl>         | Oculte el formato temporal que se crea cuando se llama a [**ITextFont.Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) **con tomApplyTmp**. Por ejemplo, estos formatos los usan los correctores ortográficos para mostrar un subrayado ondulado en palabras posiblemente mal escritas.<br/> |
| <dl> <dt>**SES \_ EX \_ USEMOUSMOUSMOUPARAM**</dt> </dl>     | Use *wParam al* controlar el [**mensaje WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) y no llame a [**GetAsyncKeyState.**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate)<br/>                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ SETEDITSTYLEEX**](em-seteditstyleex.md)
</dt> </dl>

 

