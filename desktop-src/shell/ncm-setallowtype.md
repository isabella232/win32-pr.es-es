---
description: Establece los tipos de dirección de red que acepta un control de dirección de red especificado.
title: Mensaje de NCM_SETALLOWTYPE (ShellAPI. h)
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
ms.openlocfilehash: d9cc822e07022a01439fbe7e41243bd1b78e636b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810940"
---
# <a name="ncm_setallowtype-message"></a>NCM \_ SETALLOWTYPE

Establece los tipos de dirección de red que acepta un control de dirección de red especificado.


```C++
NCM_SETALLOWTYPE

    wParam = (WPARAM) (DWORD) addrMask;

    lParam = 0;            

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*addrMask* \[ de\]
</dt> <dd>Especifica los tipos de dirección de red como una o varias de las constantes de <a href="net-string.md">**\_ cadena**</a> de red.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve \_ si es correcto, o un valor de error en caso contrario.

## <a name="remarks"></a>Observaciones

El conjunto de máscaras es el criterio que se usa para validar una dirección de red en el mensaje de [**NCM \_ GETADDRESS**](ncm-getaddress.md) .

Use este mensaje solo para un control de dirección de red. Para crear una instancia de, use la clase **msctls \_ netaddress** definida en ShellAPI. h. Llame a [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) en tiempo de ejecución antes de enviar este mensaje. Esto inicializa la biblioteca de controles comunes que contiene el control de dirección de red.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>ShellAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**NCM \_ GETALLOWTYPE**](ncm-getallowtype.md)
</dt> <dt>

[**NetAddr \_ SetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)
</dt> </dl>

 

 




