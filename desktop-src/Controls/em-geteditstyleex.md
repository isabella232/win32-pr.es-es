---
title: Mensaje EM_GETEDITSTYLEEX (RichEdit. h)
description: Recupera las marcas de estilo de edición extendida actual.
ms.assetid: 3E81F7BB-404D-4465-982A-3CF6FD9359DA
keywords:
- EM_GETEDITSTYLEEX controles de mensajes de Windows
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
ms.openlocfilehash: bb4077abaedd0c5ec720603d6b23e77950fd5307
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905300"
---
# <a name="em_geteditstyleex-message"></a>\_Mensaje GETEDITSTYLEEX em

Recupera las marcas de estilo de edición extendida actual.


```C++
#define EM_GETEDITSTYLEEX       (WM_USER + 276)
```



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

Devuelve las marcas de estilo de edición extendida, que pueden incluir uno o varios de los valores siguientes.



| Código devuelto                                                                                                | Descripción                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SES \_ ex \_ HANDLEFRIENDLYURL**</dt> </dl>  | Mostrar los vínculos de nombre descriptivo con el mismo color de texto y subrayado como vínculos automáticos, siempre que el formato temporal sea t Used o use el texto Autocolor (valor predeterminado: 0).<br/>                                                                       |
| <dl> <dt>**SES \_ ex \_ multitoque**</dt> </dl>         | Habilite la compatibilidad con Touch en Rich Edit. Esto incluye la selección, la posición del símbolo de intercalación y la invocación del menú contextual. Cuando no se establece esta marca, el toque se emula mediante comandos del mouse, que no tienen en cuenta los detalles del modo táctil (valor predeterminado: 0). <br/>      |
| <dl> <dt>**SES \_ ex \_ NOACETATESELECTION**</dt> </dl> | Muestra el texto seleccionado con el texto de selección clásico de Windows y los colores de fondo en lugar del color de acetato de fondo (valor predeterminado: 0). <br/>                                                                                                               |
| <dl> <dt>**SES \_ = \_ nomath**</dt> </dl>             | Deshabilitar la inserción de zonas matemáticas (valor predeterminado: 1). Para habilitar la edición y visualización de matemáticas, envíe el mensaje [**em \_ SETEDITSTYLEEX**](em-seteditstyleex.md) con *wParam* establecido en 0 y *lParam* establecido en **SES @ \_ \_ nomath**. <br/>                              |
| <dl> <dt>**SES, \_ ex \_ importante**</dt> </dl>            | Deshabilitar la inserción de tablas. El [**mensaje \_ INSERTTABLE em**](em-inserttable.md) devuelve **e \_ FAIL** y las tablas RTF se omiten (valor predeterminado: 0). <br/>                                                                                                  |
| <dl> <dt>**SES \_ ex \_ USESINGLELINE**</dt> </dl>      | Permite que un control multilínea actúe como un control de una sola línea con la capacidad de desplazarse verticalmente cuando el alto de una sola línea es mayor que el alto de la ventana (valor predeterminado: 0). <br/>                                                                   |
| <dl> <dt>**HIDETEMPFORMAT de SES \_**</dt> </dl>         | Oculte el formato temporal que se crea cuando se llama a [**ITextFont. Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) con **tomApplyTmp**. Por ejemplo, los comprobadores ortográficos usan este formato para mostrar un subrayado ondulado en palabras posiblemente mal escritas.<br/> |
| <dl> <dt>**SES \_ ex \_ USEMOUSEWPARAM**</dt> </dl>     | Use *wParam* al controlar el mensaje de [**\_ MOUSEMOVE de WM**](/windows/desktop/inputdev/wm-mousemove) y no llame a [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).<br/>                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETEDITSTYLEEX em**](em-seteditstyleex.md)
</dt> </dl>

 

