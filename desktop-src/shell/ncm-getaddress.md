---
description: Indica si una dirección de red se ajusta a un tipo y formato especificados.
title: NCM_GETADDRESS mensaje (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 733CD62D-614C-4ac2-986D-CCFCFF4B1B4D
api_name:
- NCM_GETADDRESS
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d5effa69a23a61a602efaf1172de09a09889e32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361052"
---
# <a name="ncm_getaddress-message"></a>Mensaje \_ GETADDRESS de NCM

Indica si una dirección de red se ajusta a un tipo y formato especificados.


```C++
NCM_GETADDRESS

    wParam = (WPARAM) (PNC_ADDRESS) pv;

    lParam = 0;            

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*pv* \[ in, out\]
</dt> <dd>Puntero a una estructura <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> para recibir información de dirección de red en formato analizada, si se validan el formato de dirección y el tipo en el control especificado por *hwnd.* La aplicación que realiza la llamada es responsable de asignar la memoria para esta estructura.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores de tipo **HRESULT.**



| Código devuelto                                                                                                | Descripción                                                                                          |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | La aplicación que realiza la llamada no pudo asignar una [**estructura \_ NC ADDRESS.**](/windows/win32/api/shellapi/ns-shellapi-nc_address)<br/> |
| <dl> <dt>**ERROR \_ BÚFER \_ INSUFICIENTE**</dt> </dl> | El búfer de salida es demasiado pequeño para contener la dirección de red analizada.<br/>                           |
| <dl> <dt>**ERROR \_ PARÁMETRO NO \_ VÁLIDO**</dt> </dl>   | La cadena de dirección de red no es de ningún tipo especificado.<br/>                                  |
| <dl> <dt>**ERROR \_ CORRECTO**</dt> </dl>              | La operación se realizó correctamente.<br/>                                                             |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | No hay ninguna dirección en el control de direcciones de red que se va a validar.<br/>                           |



 

## <a name="remarks"></a>Observaciones

Use el **mensaje \_ GETADDRESS** de NCM para validar una dirección de red en un control de dirección de red con una máscara de tipo de dirección de red preestablecida. Para crear una instancia, use la **clase msctls \_ netaddress** definida en Shellapi.h. Llame [**a InitNetworkAddressControl en**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) tiempo de ejecución antes de enviar este mensaje. Esto inicializa la biblioteca de controles comunes que contiene el control de direcciones de red.

Este mensaje obtiene la cadena de dirección de red de un control de direcciones de red, analiza la cadena y comprueba si la cadena coincide con una máscara de tipo de dirección de red. Si la cadena coincide con la máscara, el mensaje devuelve S OK y devuelve la cadena en forma analizada a la aplicación que realiza la llamada (incluido el número de puerto, la longitud del prefijo y otra información de dirección), utilizando la estructura \_ [**NC \_ ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) a la que apunta *pv*. Este mensaje devuelve E INVALIDARG si la aplicación que realiza la llamada no puede asignar la estructura a la \_ que apunta *pv*.

Se analizan las representaciones de las versiones 4 y 6 (v4/v6) de las direcciones de protocolo de Internet (IP) para servicios y redes, así como direcciones de Internet y servicios con nombre que usan el formato sistema de nombres de dominio (DNS). Si la cadena de dirección de red representa un nombre de host con nombre (DNS) o servicio, el valor devuelto en el miembro **PrefixLength** de [**NC \_ ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) es cero.

Establezca la máscara de tipo de dirección de red mediante el [**mensaje \_ NCM SETALLOWTYPE**](ncm-setallowtype.md) antes de enviar la macro **\_ GETADDRESS de NCM.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**NCM \_ GETALLOWTYPE**](ncm-getallowtype.md)
</dt> <dt>

[**NetAddr \_ GetAddress**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)
</dt> </dl>

 

 




