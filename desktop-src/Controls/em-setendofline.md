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
ms.openlocfilehash: 5990b247757fc8e3cd39ab38edf5b88ca8ac62f74e402aac3899d51e3156231f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437595"
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
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**EC \_ ENDOFLINE \_ CRLF**</dt> </dl>                                        | Establece el carácter de fin de línea que se usa para los nuevos linebreaks en retorno de carro seguido de linefeed (CRLF).<br/> |
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

## <a name="remarks"></a>Comentarios

Cuando el juego de caracteres de fin de línea es **EC \_ ENDOFLINE \_ DETECTFROMCONTENT,** el control de edición solo detectará los caracteres de fin de línea admitidos según su estilo de ventana extendido, vea Editar estilos extendidos de [control](edit-control-window-extended-styles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio 1809 \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2019 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ GETENDOFLINE*](em-getendofline.md)
</dt> </dl>

 

 





