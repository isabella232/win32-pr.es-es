---
title: Mensaje de EM_SETWORDBREAKPROC (Winuser. h)
description: Reemplaza la función de ajuste de la configuración predeterminada de un control de edición por una función de ajuste de la aplicación definida por la aplicación. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: e5029b75-5f35-43a5-876d-24e81605bb49
keywords:
- EM_SETWORDBREAKPROC controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e85335562c9e9881093d89293e7e2ace9cf43b0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534360"
---
# <a name="em_setwordbreakproc-message"></a>\_Mensaje SETWORDBREAKPROC em

Reemplaza la función de ajuste de la configuración predeterminada de un control de edición por una función de ajuste de la aplicación definida por la aplicación. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

La dirección de la función de ajuste de la aplicación definida por la aplicación. Para obtener más información sobre las líneas de interrupción, vea la descripción de la función de devolución de llamada [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una función WordWrap examina un búfer de texto que contiene el texto que se va a enviar a la pantalla, buscando la primera palabra que no cabe en la línea de pantalla actual. La función WordWrap coloca esta palabra al principio de la línea siguiente en la pantalla.

Una función WordWrap define el punto en el que el sistema debe dividir una línea de texto para los controles de edición de varias líneas, normalmente en un carácter de espacio que separa dos palabras. Un control de edición multilínea o de una sola línea podría llamar a esta función cuando el usuario presiona las teclas de dirección en combinación con la tecla CTRL para desplace el símbolo de intercalación a la palabra siguiente o a la palabra anterior. La función WordWrap predeterminada divide una línea de texto en un carácter de espacio. La función definida por la aplicación puede definir que el ajuste de velocidad se produzca en un guion o un carácter distinto del carácter de espacio.

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

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

[*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[**\_FMTLINES em**](em-fmtlines.md)
</dt> <dt>

[**\_GETWORDBREAKPROC em**](em-getwordbreakproc.md)
</dt> </dl>

 

