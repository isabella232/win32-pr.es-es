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
ms.openlocfilehash: 5d93cb3cff575c18764e352da54a717d7c557001
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361051"
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

## <a name="remarks"></a>Observaciones

La máscara devuelta es el criterio utilizado para validar una dirección de red en el [**mensaje \_ GETADDRESS de NCM.**](ncm-getaddress.md)

Use este mensaje solo para un control de direcciones de red. Para crear una instancia, use la **clase msctls \_ netaddress** definida en Shellapi.h. Llame [**a InitNetworkAddressControl en**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) tiempo de ejecución antes de enviar este mensaje. Esto inicializa la biblioteca de controles comunes que contiene el control de direcciones de red.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md)
</dt> <dt>

[**NetAddr \_ GetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)
</dt> </dl>

 

 




