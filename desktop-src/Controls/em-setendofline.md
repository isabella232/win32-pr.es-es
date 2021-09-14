---
title: EM_SETENDOFLINE mensaje (CommCtrl.h)
description: Establece el carácter de fin de línea que se usa cuando se inserta un linebreak.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- EM_SETENDOFLINE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETENDOFLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 5ee7c500ba3818cad0f5ee74e9994ed8af049ea0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062115"
---
# <a name="em_setendofline-message"></a>Mensaje \_ EM SETENDOFLINE

Establece el carácter de fin de línea que se usa cuando se inserta un linebreak.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el carácter de fin de línea que se usa cuando se inserta un linebreak. Puede ser uno de los siguientes valores.


| Value                                                                                                                                                   | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_DETECTFROMCONTENT"></span><span id="ec_endofline_detectfromcontent"></span><dl> <dt>**EC \_ ENDOFLINE \_ DETECTFROMCONTENT**</dt> </dl> | Establece el carácter de fin de línea utilizado para los nuevos linebreaks en el carácter utilizado por el documento actual.<br/>  |
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**EC \_ ENDOFLINE \_ CRLF**</dt> </dl>                                        | Establece el carácter de fin de línea utilizado para los nuevos linebreaks en retorno de carro seguido de linefeed (CRLF).<br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <dt>**EC \_ ENDOFLINE \_ CR**</dt> </dl>                                              | Establece el carácter de fin de línea que se usa para los nuevos linebreaks en retorno de carro (CR).<br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <dt>**EC \_ ENDOFLINE \_ LF**</dt> </dl>                                              | Establece el carácter de fin de línea que se usa para los nuevos linebreaks en linefeed (LF).<br/>                               |

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es distinto de cero.

Si se produce un error en la operación, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Cuando el juego de caracteres de fin de línea es **EC \_ ENDOFLINE \_ DETECTFROMCONTENT,** el control de edición solo detectará los caracteres de fin de línea admitidos según su estilo de ventana extendido, vea Editar estilos extendidos de [control](edit-control-window-extended-styles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio 1809 \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2019 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ GETENDOFLINE*](em-getendofline.md)
</dt> </dl>

 

 





