---
title: Propiedad NetworkConnectionType de IMsRdpClientAdvancedSettings7
description: Obtiene o establece el tipo de conexión de red utilizado entre el cliente y el servidor. La información del tipo de conexión de red que se pasa al servidor ayuda al servidor a optimizar varios parámetros según el tipo de conexión de red.
ms.assetid: 4dd4fa17-f121-412d-a30d-1c01f4c892b0
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad NetworkConnectionType
- Propiedad NetworkConnectionType Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad NetworkConnectionType
- Propiedad NetworkConnectionType Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad NetworkConnectionType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.NetworkConnectionType
- IMsRdpClientAdvancedSettings7.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings7.put_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.NetworkConnectionType
- IMsRdpClientAdvancedSettings8.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.put_NetworkConnectionType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5df4c1e944920759f56f5d4b493b9cd47e7ebc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686031"
---
# <a name="imsrdpclientadvancedsettings7networkconnectiontype-property"></a>IMsRdpClientAdvancedSettings7:: NetworkConnectionType (propiedad)

Obtiene o establece el tipo de conexión de red utilizado entre el cliente y el servidor. La información del tipo de conexión de red que se pasa al servidor ayuda al servidor a optimizar varios parámetros según el tipo de conexión de red.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_NetworkConnectionType(
  [in]          UINT connectionType
);

HRESULT get_NetworkConnectionType(
  [out, retval] UINT *pConnectionType
);
```



## <a name="property-value"></a>Valor de propiedad

El tipo de conexión de red.

<dt>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**Conexión \_ de \_Módem de tipo** (1 (0x1))


</dt> <dd>

Módem (56 kbps)

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**Conexión \_ de Escriba \_ Broadband \_ Low** (2 (0X2))


</dt> <dd>

Banda ancha de baja velocidad (256 kbps a 2 Mbps)

</dd> <dt>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**Conexión \_ de Escriba \_ Satellite** (3 (0X3))


</dt> <dd>

Satélite (de 2 Mbps a 16 Mbps con latencia alta)

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**Conexión \_ de Escriba \_ banda ancha \_ alta** (4 (0x4))


</dt> <dd>

Banda ancha de alta velocidad (de 2 Mbps a 10 Mbps)

</dd> <dt>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**Conexión \_ de TIPO \_ WAN** (5 (0X5))


</dt> <dd>

Red de área extensa (WAN) (10 Mbps o superior, con latencia alta)

</dd> <dt>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**Conexión \_ de Escriba \_ LAN** (6 (0x6))


</dt> <dd>

Red de área local (LAN) (10 Mbps o superior)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                                |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 se define como 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





