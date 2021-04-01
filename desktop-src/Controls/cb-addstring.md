---
title: Mensaje de CB_ADDSTRING (Winuser. h)
description: Agrega una cadena al cuadro de lista de un cuadro combinado. Si el cuadro combinado no tiene el estilo de \_ ordenación CBS, la cadena se agrega al final de la lista. De lo contrario, la cadena se inserta en la lista y la lista está ordenada.
ms.assetid: 201bcb7b-e7d1-41e6-8eb7-a5864b659a52
keywords:
- CB_ADDSTRING controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996933"
---
# <a name="cb_addstring-message"></a>Mensaje de CB \_ ADDSTRING

Agrega una cadena al cuadro de lista de un cuadro combinado. Si el cuadro combinado no tiene el estilo [**de \_ ordenación CBS**](combo-box-styles.md) , la cadena se agrega al final de la lista. De lo contrario, la cadena se inserta en la lista y la lista está ordenada.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero **LPCTSTR** a la cadena terminada en null que se va a agregar. Si crea el cuadro combinado con un estilo dibujado por el propietario pero sin el estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , el valor del parámetro *lParam* se almacena como datos de elemento en lugar de la cadena a la que apuntaría de otro modo. Los datos de los elementos se pueden recuperar o modificar mediante el envío del mensaje [**CB \_ GETITEMDATA**](cb-getitemdata.md) o [**CB \_ SETITEMDATA**](cb-setitemdata.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el índice de base cero de la cadena en el cuadro de lista del cuadro combinado. Si se produce un error, el valor devuelto es CB \_ error. Si no hay suficiente espacio disponible para almacenar la nueva cadena, es CB \_ ERRSPACE.

## <a name="remarks"></a>Observaciones

Si crea un cuadro combinado dibujado por el propietario con el estilo de [**\_ ordenación CBS**](combo-box-styles.md) pero sin el estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , el mensaje [**\_ COMPAREITEM de WM**](wm-compareitem.md) se envía una o varias veces al propietario del cuadro combinado para que el nuevo elemento se pueda colocar correctamente en la lista.

Para insertar una cadena en una ubicación concreta de la lista, use el mensaje [**CB \_ INSERTSTRING**](cb-insertstring.md) .

Si el cuadro combinado tiene el estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) y agrega una cadena más ancha que el cuadro combinado, envíe un mensaje [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) para asegurarse de que aparezca la barra de desplazamiento horizontal.

**Comclt32.dll versión 5,0 o posterior:** Si se establece [**CBS \_ LOWERCASE**](combo-box-styles.md) o [**CBS \_ Uppercase**](combo-box-styles.md) , la versión Unicode de **CB \_ ADDSTRING** modifica la cadena. Si se usa la memoria global de solo lectura, se produce un error en la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_directorio CB**](cb-dir.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> <dt>

[**COMPAREITEM de WM \_**](wm-compareitem.md)
</dt> </dl>

 

