---
description: Indica si una dirección de red se ajusta a un tipo y formato especificados.
title: Mensaje de NCM_GETADDRESS (ShellAPI. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984599"
---
# <a name="ncm_getaddress-message"></a>NCM el \_ mensaje GETADDRESS

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

*PV* \[ in, out\]
</dt> <dd>Puntero a una estructura de <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> para recibir información de dirección de red en formato analizado, si se valida el formato de dirección y el tipo del control especificado por *hWnd* . La aplicación que realiza la llamada es responsable de asignar la memoria para esta estructura.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores de tipo **HRESULT**.



| Código devuelto                                                                                                | Descripción                                                                                          |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | La aplicación que realiza la llamada no pudo asignar una estructura de [**\_ direcciones de NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) .<br/> |
| <dl> <dt>**ERROR \_ de \_ búfer insuficiente**</dt> </dl> | El búfer de salida es demasiado pequeño para contener la dirección de red analizada.<br/>                           |
| <dl> <dt>**ERROR \_ de \_ parámetro no válido**</dt> </dl>   | La cadena de dirección de red no es de ningún tipo especificado.<br/>                                  |
| <dl> <dt>**ERROR \_ correcto**</dt> </dl>              | La operación se realizó correctamente.<br/>                                                             |
| <dl> <dt>**S \_ false**</dt> </dl>                    | No hay ninguna dirección en el control de dirección de red para validar.<br/>                           |



 

## <a name="remarks"></a>Observaciones

Use el mensaje de **NCM \_ GETADDRESS** para validar una dirección de red en un control de dirección de red con una máscara de tipo de dirección de red preestablecida. Para crear una instancia de, use la clase **msctls \_ netaddress** definida en ShellAPI. h. Llame a [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) en tiempo de ejecución antes de enviar este mensaje. Esto inicializa la biblioteca de controles comunes que contiene el control de dirección de red.

Este mensaje obtiene la cadena de dirección de red de un control de dirección de red, analiza la cadena y comprueba si la cadena coincide con una máscara de tipo de dirección de red. Si la cadena coincide con la máscara, el mensaje devuelve S \_ OK y devuelve la cadena en forma de análisis a la aplicación que realiza la llamada (incluido el número de puerto, la longitud del prefijo y otra información de dirección), mediante la estructura de la [**\_ dirección de NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) a la que apunta *PV*. Este mensaje devuelve E \_ INVALIDARG si la aplicación que realiza la llamada no puede asignar la estructura a la que apunta *PV*.

Se analizan las representaciones de las versiones 4 y 6 (V4/V6) de la dirección del Protocolo de Internet (IP) para servicios y redes, así como las direcciones de Internet con nombre y los servicios que usan el formato del sistema de nombres de dominio (DNS). Si la cadena de la dirección de red representa un nombre de host (DNS) o servicio con nombre, el valor devuelto en el miembro **PrefixLength** de la [**\_ Dirección NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) es cero.

Establezca la máscara de tipo de dirección de red mediante el mensaje [**\_ SETALLOWTYPE de NCM**](ncm-setallowtype.md) antes de enviar la macro **NCM \_ GETADDRESS** .

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

[**NetAddr \_ GetAddress**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)
</dt> </dl>

 

 




