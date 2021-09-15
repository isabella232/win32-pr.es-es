---
description: Muestra un mensaje de error en la sugerencia de globo asociada al control de dirección de red.
title: NCM_DISPLAYERRORTIP mensaje (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5ECAB6C3-69FC-4f2a-A9E6-80BC37ED3119
api_name:
- NCM_DISPLAYERRORTIP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8a3968b9001d74721938190369e6b52cf2368835
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574541"
---
# <a name="ncm_displayerrortip-message"></a>Mensaje \_ DISPLAYERRORTIP de NCM

Muestra un mensaje de error en la sugerencia de globo asociada al control de dirección de red.


```C++
NCM_DISPLAYERRORTIP

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este mensaje se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Envíe este mensaje para mostrar un mensaje de error cuando una dirección con tipo en el control no se valide con los tipos de direcciones de red permitidos establecidos con el mensaje [**\_ NCM SETALLOWTYPE.**](ncm-setallowtype.md) Use el [**mensaje \_ GETADDRESS de NCM**](ncm-getaddress.md) para validar la dirección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**NetAddr \_ DisplayErrorTip**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)
</dt> </dl>

 

 




