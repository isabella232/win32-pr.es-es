---
title: CB_ADDSTRING mensaje (Winuser.h)
description: Agrega una cadena al cuadro de lista de un cuadro combinado. Si el cuadro combinado no tiene el estilo SORT de \_ CBS, la cadena se agrega al final de la lista. De lo contrario, la cadena se inserta en la lista y la lista se ordena.
ms.assetid: 201bcb7b-e7d1-41e6-8eb7-a5864b659a52
keywords:
- CB_ADDSTRING controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda16367ec24e869f6cb664e89751d7a13efec3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173974"
---
# <a name="cb_addstring-message"></a>Mensaje \_ ADDSTRING de CB

Agrega una cadena al cuadro de lista de un cuadro combinado. Si el cuadro combinado no tiene el estilo [**\_ SORT de CBS,**](combo-box-styles.md) la cadena se agrega al final de la lista. De lo contrario, la cadena se inserta en la lista y la lista se ordena.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero **LPCTSTR** a la cadena terminada en NULL que se va a agregar. Si crea el cuadro combinado con un estilo dibujado por el propietario pero sin el estilo [**\_ HASSTRINGS de CBS,**](combo-box-styles.md) el valor del parámetro *lParam* se almacena como datos de elemento en lugar de la cadena a la que apuntaría de otro modo. Los datos del elemento se pueden recuperar o modificar enviando el mensaje [**CB \_ GETITEMDATA**](cb-getitemdata.md) o [**CB \_ SETITEMDATA.**](cb-setitemdata.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el índice de base cero de la cadena del cuadro de lista del cuadro combinado. Si se produce un error, el valor devuelto es CB \_ ERR. Si no hay suficiente espacio disponible para almacenar la nueva cadena, es CB \_ ERRSPACE.

## <a name="remarks"></a>Observaciones

Si crea un cuadro combinado dibujado por el propietario con el estilo SORT de [**CBS \_**](combo-box-styles.md) pero sin el estilo [**\_ HASSTRINGS de CBS,**](combo-box-styles.md) el mensaje [**\_ COMPAREITEM**](wm-compareitem.md) de WM se envía una o varias veces al propietario del cuadro combinado para que el nuevo elemento se pueda colocar correctamente en la lista.

Para insertar una cadena en una ubicación específica de la lista, use el [**mensaje \_ INSERTSTRING de CB.**](cb-insertstring.md)

Si el cuadro combinado tiene el estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) y agrega una cadena más ancha que el cuadro combinado, envíe un mensaje [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) para asegurarse de que aparece la barra de desplazamiento horizontal.

**Comclt32.dll versión 5.0 o posterior:** Si [**se establece \_ CBS LOWERCASE**](combo-box-styles.md) o [**CBS \_ UPPERCASE,**](combo-box-styles.md) la versión Unicode de **CB \_ ADDSTRING** modifica la cadena. Si usa memoria global de solo lectura, esto hace que se produce un error en la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ DIR**](cb-dir.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> <dt>

[**COMPAREITEM de WM \_**](wm-compareitem.md)
</dt> </dl>

 

