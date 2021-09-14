---
title: CB_GETLBTEXT mensaje (Winuser.h)
description: Obtiene una cadena de la lista de un cuadro combinado.
ms.assetid: f84e302a-65bb-45c8-958b-1cb438fb5a7a
keywords:
- CB_GETLBTEXT controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_GETLBTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d26a964b463daedab1ad5d9f50888b3e0c1e0db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174198"
---
# <a name="cb_getlbtext-message"></a>Mensaje \_ GETLBTEXT de CB

Obtiene una cadena de la lista de un cuadro combinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la cadena que se recuperará.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al búfer que recibe la cadena. El búfer debe tener espacio suficiente para la cadena y un carácter nulo de terminación. Puede enviar un mensaje [**\_ CB GETLBTEXTLEN**](cb-getlbtextlen.md) antes del mensaje **\_ GETLBTEXT de CB** para recuperar la longitud, en **TCHAR,** de la cadena. Si es una cadena ANSI, este es el número de bytes, pero si es una cadena Unicode, es el número de caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es la longitud de la cadena, en **TCHAR,** sin incluir el carácter nulo final. Si *wParam no* especifica un índice válido, el valor devuelto es CB \_ ERR.

## <a name="remarks"></a>Observaciones

**Advertencia de seguridad:** El uso incorrecto de este mensaje puede poner en peligro la seguridad del programa. Este mensaje no proporciona una manera de conocer el tamaño del búfer. Si usa este mensaje, primero llame a [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) para obtener el número de caracteres necesarios y, a continuación, llame al mensaje para recuperar la cadena. Debe revisar consideraciones [de seguridad: Microsoft Windows antes](sec-comctls.md) de continuar.

Si crea el cuadro combinado con un estilo dibujado por el propietario pero sin el estilo [**\_ HASSTRINGS de CBS,**](combo-box-styles.md) el búfer al que apunta *lParam* recibe los datos asociados al elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md)
</dt> </dl>

 

 





