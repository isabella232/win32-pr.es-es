---
description: Recupera los tipos de dirección de red que un control de dirección de red especificado acepta.
title: Mensaje de NCM_GETALLOWTYPE (ShellAPI. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082235"
---
# <a name="ncm_getallowtype-message"></a>NCM \_ GETALLOWTYPE

Recupera los tipos de dirección de red que un control de dirección de red especificado acepta.


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

Devuelve los tipos de dirección de red permitidos como una o varias de las constantes de [**\_ cadena**](net-string.md) de red.

## <a name="remarks"></a>Observaciones

La máscara devuelta es el criterio que se usa para validar una dirección de red en el mensaje de [**NCM \_ GETADDRESS**](ncm-getaddress.md) .

Use este mensaje solo para un control de dirección de red. Para crear una instancia de, use la clase **msctls \_ netaddress** definida en ShellAPI. h. Llame a [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) en tiempo de ejecución antes de enviar este mensaje. Esto inicializa la biblioteca de controles comunes que contiene el control de dirección de red.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>ShellAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md)
</dt> <dt>

[**NetAddr \_ GetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)
</dt> </dl>

 

 




