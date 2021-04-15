---
title: Mensaje de EM_SETENDOFLINE (CommCtrl. h)
description: Establece el carácter de final de línea que se usa cuando se inserta un LineBreak.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- EM_SETENDOFLINE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492461"
---
# <a name="em_setendofline-message"></a>\_Mensaje SETENDOFLINE em

Establece el carácter de final de línea que se usa cuando se inserta un LineBreak.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el carácter de final de línea que se usa cuando se inserta un LineBreak. Puede ser uno de los valores siguientes.


| Value                                                                                                                                                   | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_DETECTFROMCONTENT"></span><span id="ec_endofline_detectfromcontent"></span><dl> <dt>**\_DETECTFROMCONTENT ENDOFLINE \_ EC**</dt> </dl> | Establece el carácter de final de línea usado para New saltos en el carácter utilizado por el documento actual.<br/>  |
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**\_CRLF ENDOFLINE \_ EC**</dt> </dl>                                        | Establece el carácter de final de línea usado para New saltos en el retorno de carro seguido de avance de línea (CRLF).<br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <dt>**EC \_ ENDOFLINE \_ CR**</dt> </dl>                                              | Establece el carácter de final de línea usado para New saltos en el retorno de carro (CR).<br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <dt>**\_ENDOFLINE de \_ LF de EC**</dt> </dl>                                              | Establece el carácter de final de línea usado para New saltos en avance de línea (LF).<br/>                               |

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es distinto de cero.

Si se produce un error en la operación, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Cuando el juego de caracteres de fin de línea es **EC \_ ENDOFLINE \_ DETECTFROMCONTENT**, el control de edición solo detectará los caracteres de fin de línea admitidos según su estilo de ventana extendido, vea [Editar estilos extendidos del control](edit-control-window-extended-styles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 y 1809 \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2019 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETENDOFLINE em*](em-getendofline.md)
</dt> </dl>

 

 





