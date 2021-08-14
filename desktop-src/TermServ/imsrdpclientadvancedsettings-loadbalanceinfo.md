---
title: Propiedad IMsRdpClientAdvancedSettings LoadBalanceInfo
description: Especifica la cookie de equilibrio de carga que se colocará en el paquete de solicitud de conexión X.224 en la secuencia de conexión del protocolo de servidor de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto).
ms.assetid: 25f12a2e-00a2-42a8-afd3-81efcd94da94
ms.tgt_platform: multiple
keywords:
- Propiedad LoadBalanceInfo Servicios de Escritorio remoto
- Propiedad LoadBalanceInfo Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings
- Interfaz IMsRdpClientAdvancedSettings Servicios de Escritorio remoto , propiedad LoadBalanceInfo
- Interfaz de propiedad LoadBalanceInfo Servicios de Escritorio remoto , IMsRdpClientAdvancedSettings2
- Interfaz IMsRdpClientAdvancedSettings2 Servicios de Escritorio remoto , propiedad LoadBalanceInfo
- Propiedad LoadBalanceInfo Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings3
- Interfaz IMsRdpClientAdvancedSettings3 Servicios de Escritorio remoto , propiedad LoadBalanceInfo
- Propiedad LoadBalanceInfo Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings4
- Interfaz IMsRdpClientAdvancedSettings4 Servicios de Escritorio remoto , propiedad LoadBalanceInfo
- Propiedad LoadBalanceInfo Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings5
- Interfaz IMsRdpClientAdvancedSettings5 Servicios de Escritorio remoto , propiedad LoadBalanceInfo
- Propiedad LoadBalanceInfo Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings6
- Interfaz IMsRdpClientAdvancedSettings6 Servicios de Escritorio remoto , propiedad LoadBalanceInfo
- Propiedad LoadBalanceInfo Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings7
- Interfaz IMsRdpClientAdvancedSettings7 Servicios de Escritorio remoto , propiedad LoadBalanceInfo
- Propiedad LoadBalanceInfo Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings8
- Interfaz IMsRdpClientAdvancedSettings8 Servicios de Escritorio remoto , propiedad LoadBalanceInfo
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.LoadBalanceInfo
- IMsRdpClientAdvancedSettings.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.put_LoadBalanceInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efe7ca9b9ed68f3327779177e706ee5a943c9e6580e2b789e2b96e74ee9f0b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353044"
---
# <a name="imsrdpclientadvancedsettingsloadbalanceinfo-property"></a>Propiedad IMsRdpClientAdvancedSettings::LoadBalanceInfo

Especifica la cookie de equilibrio de carga que se colocará en el paquete de solicitud de conexión X.224 en la secuencia de conexión del protocolo de servidor de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_LoadBalanceInfo(
  [in]  BSTR newLBInfo
);

HRESULT get_LoadBalanceInfo(
  [out] BSTR *pLBInfo
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a la nueva cookie. Para más información, consulte la sección comentarios.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Comentarios

Los enrutadores de equilibrio de carga usan la información de equilibrio de carga para elegir el mejor servidor para el cliente cuando se usan granjas de servidores host de sesión de Escritorio remoto. El propio servidor host de sesión de Escritorio remoto no usa esta información y la descartará.

La cookie usa la siguiente sintaxis, que distingue mayúsculas de minúsculas:

**Cookie: msts=**_IpAddressAndPortNumber_*_\\ r \\ n_*

Donde *IpAddressAndPortNumber es* la dirección IP y el número de puerto, en orden de bytes de red.

Por ejemplo, la cookie usada para acceder a la dirección IP de 172.31.249.216, el número de puerto 3389 es el siguiente:

**Cookie: msts=3640205228.15629.0000 \\ r \\ n**

Los cuatro últimos ceros son opcionales y están reservados. El separador decimal final es necesario, al igual que el retorno de carro final y el recorrido de línea. La longitud de la cadena, en caracteres, debe ser un múltiplo par de 2, por lo que debe agregar un espacio si es necesario.

Si no se proporciona ninguna cookie, el valor predeterminado **es Cookie: mstshash=**_UserName_*_\\ r \\ n_*.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                        |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                  |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





