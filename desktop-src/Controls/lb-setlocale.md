---
title: Mensaje de LB_SETLOCALE (Winuser. h)
description: Establece la configuración regional actual del cuadro de lista. Puede usar la configuración regional para determinar el criterio de ordenación correcto del texto mostrado (para los cuadros de lista con el \_ estilo de ordenación lbs) y del texto agregado por el mensaje de lb en lb \_ .
ms.assetid: e9503124-de9f-4b92-a59e-ec9320864ae7
keywords:
- LB_SETLOCALE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8ea7bb7b6d19144a84ab166f56cd2c0ad49e05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079656"
---
# <a name="lb_setlocale-message"></a>Mensaje de LB \_ SETLOCALE

Establece la configuración regional actual del cuadro de lista. Puede usar la configuración regional para determinar el criterio de ordenación correcto del texto mostrado (para los cuadros de lista con el estilo de [**\_ ordenación lbs**](list-box-styles.md) ) y del texto agregado por el mensaje de [**lb en lb \_**](lb-addstring.md) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el identificador de configuración regional que el cuadro de lista usará para la ordenación al agregar texto.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el identificador de configuración regional anterior. Si el parámetro *wParam* especifica una configuración regional que no está instalada en el sistema, el valor devuelto es lb \_ Err y la configuración regional del cuadro de lista actual no cambia.

## <a name="remarks"></a>Observaciones

Use la macro [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) para construir un identificador de configuración regional.

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

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**equilibro \_ de lb**](lb-getlocale.md)
</dt> </dl>

 

