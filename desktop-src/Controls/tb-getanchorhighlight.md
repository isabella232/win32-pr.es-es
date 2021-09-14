---
title: TB_GETANCHORHIGHLIGHT mensaje (Commctrl.h)
description: Recupera la configuración de resaltado de delimitador para una barra de herramientas.
ms.assetid: 167d481c-8684-40eb-9323-cfa238be3643
keywords:
- TB_GETANCHORHIGHLIGHT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_GETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bfff5ef1853bbf5657604c673dcc6a9be43af83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166866"
---
# <a name="tb_getanchorhighlight-message"></a>Mensaje \_ DE TB GETANCHORHIGHLIGHT

Recupera la configuración de resaltado de delimitador para una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que indica si se ha establecido el resaltado de delimitadores. Si este valor es distinto de cero, se habilita el resaltado de delimitadores. Si este valor es cero, se deshabilita.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TB \_ SETANCHORHIGHLIGHT**](tb-setanchorhighlight.md)
</dt> </dl>

 

 





