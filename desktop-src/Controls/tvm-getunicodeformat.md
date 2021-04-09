---
title: Mensaje de TVM_GETUNICODEFORMAT (commctrl. h)
description: Recupera la marca del formato de caracteres Unicode para el control. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetUnicodeFormat de TreeView.
ms.assetid: d95f61b6-9ec1-4471-b24b-efe141428747
keywords:
- TVM_GETUNICODEFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88478d30e8da98ebf2e2325d6152087a14bc066a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079111"
---
# <a name="tvm_getunicodeformat-message"></a>\_Mensaje de GETUNICODEFORMAT TVM

Recupera la marca del formato de caracteres Unicode para el control. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetUnicodeFormat de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getunicodeformat) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la marca de formato Unicode para el control. Si este valor es distinto de cero, el control utiliza caracteres Unicode. Si este valor es cero, el control usa caracteres ANSI.

## <a name="remarks"></a>Observaciones

Vea la sección Comentarios para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para obtener una descripción de este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ SETUNICODEFORMAT**](tvm-setunicodeformat.md)
</dt> </dl>

 

 





