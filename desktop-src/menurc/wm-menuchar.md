---
title: WM_MENUCHAR mensaje (Winuser.h)
description: Se envía cuando un menú está activo y el usuario presiona una tecla que no corresponde a ninguna tecla mnemotécnica o de acelerador. Este mensaje se envía a la ventana que posee el menú.
ms.assetid: de6c91bb-80fd-44b2-8d96-d016477a6547
keywords:
- WM_MENUCHAR menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_MENUCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a278e4a1b4333631741a6a542318a8a55e40b512
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571617"
---
# <a name="wm_menuchar-message"></a>Mensaje \_ MENUCHAR de WM

Se envía cuando un menú está activo y el usuario presiona una tecla que no corresponde a ninguna tecla mnemotécnica o de acelerador. Este mensaje se envía a la ventana que posee el menú.


```C++
#define WM_MENUCHAR                     0x0120
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La palabra de orden bajo especifica el código de carácter que corresponde a la clave que el usuario ha presionado.

La palabra de orden superior especifica el tipo de menú activo. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                 | Significado                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ POPUP**</dt> <dt>0x00000010L</dt> </dl>       | Menú desplegable, submenú o menú contextual.<br/> |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <dt>**MF \_ SYSMENU**</dt> <dt>0x00002000L</dt> </dl> | Menú de la ventana.<br/>                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del menú activo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación que procesa este mensaje debe devolver uno de los siguientes valores en la palabra de orden superior del valor devuelto.



| Código o valor devuelto                                                                                                                                  | Descripción                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MNC \_ CLOSE**</dt> <dt>1</dt> </dl>   | Informa al sistema de que debe cerrar el menú activo.<br/>                                                                                                                      |
| <dl> <dt>**MNC \_ EXECUTE**</dt> <dt>2</dt> </dl> | Informa al sistema de que debe elegir el elemento especificado en la palabra de orden bajo del valor devuelto. La ventana de propietario recibe un [**mensaje \_ WM COMMAND.**](wm-command.md)<br/> |
| <dl> <dt>**MNC \_ IGNORE**</dt> <dt>0</dt> </dl>  | Informa al sistema de que debe descartar el carácter que el usuario presionó y crear un breve pitido en el altavoz del sistema.<br/>                                                       |
| <dl> <dt>**MNC \_ SELECT**</dt> <dt>3</dt> </dl>  | Informa al sistema de que debe seleccionar el elemento especificado en la palabra de orden bajo del valor devuelto. <br/>                                                                       |



 

## <a name="remarks"></a>Observaciones

La palabra de orden bajo se omite si la palabra de orden superior contiene 0 o 1.

Una aplicación debe procesar este mensaje cuando se usa un acelerador para seleccionar un elemento de menú que muestra un mapa de bits.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Conceptual**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

