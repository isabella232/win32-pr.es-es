---
description: Establece los tipos de direcciones de red que acepta un control de dirección de red especificado.
title: NCM_SETALLOWTYPE mensaje (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FD998452-047A-4aea-A08E-8F6F8C30115B
api_name:
- NCM_SETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d3fc6b8ceb848d4738ff2d77b4441a29354bf09248e0de88008072dbf867e8a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719929"
---
# <a name="ncm_setallowtype-message"></a>Mensaje \_ NCM SETALLOWTYPE

Establece los tipos de direcciones de red que acepta un control de dirección de red especificado.


```C++
NCM_SETALLOWTYPE

    wParam = (WPARAM) (DWORD) addrMask;

    lParam = 0;            

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*addrMask* \[ En\]
</dt> <dd>Especifica los tipos de direcciones de red como una o varias de las <a href="net-string.md">**constantes \_ DE NET STRING.**</a></dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un valor de error en caso contrario.

## <a name="remarks"></a>Comentarios

El conjunto de máscaras es el criterio que se usa para validar una dirección de red en el [**mensaje \_ GETADDRESS de NCM.**](ncm-getaddress.md)

Use este mensaje solo para un control de direcciones de red. Para crear instancias, use la clase **msctls \_ netaddress** definida en Shellapi.h. Llame [**a InitNetworkAddressControl en**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) tiempo de ejecución antes de enviar este mensaje. Esto inicializa la biblioteca de controles comunes que contiene el control de direcciones de red.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**NCM \_ GETALLOWTYPE**](ncm-getallowtype.md)
</dt> <dt>

[**NetAddr \_ SetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)
</dt> </dl>

 

 




