---
description: Recupera los tipos de direcciones de red que acepta un control de dirección de red especificado.
title: NCM_GETALLOWTYPE mensaje (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1B06463F-0CA6-4e8e-BD3B-917562A6A244
api_name:
- NCM_GETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 11b937ca851f00c51090683db4aebfc3db63cbf83efc95bad7a6f456d8f58988
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858814"
---
# <a name="ncm_getallowtype-message"></a>Mensaje \_ GETALLOWTYPE de NCM

Recupera los tipos de direcciones de red que acepta un control de dirección de red especificado.


```C++
NCM_GETALLOWTYPE

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

Devuelve los tipos de direcciones de red permitidos como una o varias de las [**constantes \_ DE NET STRING.**](net-string.md)

## <a name="remarks"></a>Comentarios

La máscara devuelta es el criterio utilizado para validar una dirección de red en el [**mensaje \_ GETADDRESS de NCM.**](ncm-getaddress.md)

Use este mensaje solo para un control de direcciones de red. Para crear una instancia, use la **clase msctls \_ netaddress** definida en Shellapi.h. Llame [**a InitNetworkAddressControl en**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) tiempo de ejecución antes de enviar este mensaje. Esto inicializa la biblioteca de controles comunes que contiene el control de direcciones de red.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md)
</dt> <dt>

[**NetAddr \_ GetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)
</dt> </dl>

 

 




