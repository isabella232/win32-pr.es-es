---
title: Propiedad IMsRdpClientAdvancedSettings7 NetworkConnectionType
description: Obtiene o establece el tipo de conexión de red utilizado entre el cliente y el servidor. La información del tipo de conexión de red que se pasa al servidor ayuda al servidor a ajustar varios parámetros en función del tipo de conexión de red.
ms.assetid: 4dd4fa17-f121-412d-a30d-1c01f4c892b0
ms.tgt_platform: multiple
keywords:
- Propiedad NetworkConnectionType Servicios de Escritorio remoto
- Propiedad NetworkConnectionType Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings7
- Interfaz IMsRdpClientAdvancedSettings7 Servicios de Escritorio remoto , propiedad NetworkConnectionType
- Propiedad NetworkConnectionType Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings8
- Interfaz IMsRdpClientAdvancedSettings8 Servicios de Escritorio remoto , propiedad NetworkConnectionType
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
ms.openlocfilehash: e331fde1a8f7013c376b99184a90e7b3bb9f599197259b044c4d1cbd38841584
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118352162"
---
# <a name="imsrdpclientadvancedsettings7networkconnectiontype-property"></a>Propiedad IMsRdpClientAdvancedSettings7::NetworkConnectionType

Obtiene o establece el tipo de conexión de red utilizado entre el cliente y el servidor. La información del tipo de conexión de red que se pasa al servidor ayuda al servidor a ajustar varios parámetros en función del tipo de conexión de red.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_NetworkConnectionType(
  [in]          UINT connectionType
);

HRESULT get_NetworkConnectionType(
  [out, retval] UINT *pConnectionType
);
```



## <a name="property-value"></a>Valor de propiedad

Tipo de conexión de red.

<dt>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**CONEXIÓN \_ MÓDEM \_ DE** TIPO (1 (0x1))


</dt> <dd>

Módem (56 Kbps)

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**CONEXIÓN \_ TIPO \_ BANDA \_ ANCHA BAJA** (2 (0x2))


</dt> <dd>

Banda ancha de baja velocidad (de 256 Kbps a 2 Mbps)

</dd> <dt>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**CONEXIÓN \_ TYPE \_ SATELLITE** (3 (0x3))


</dt> <dd>

Satélite (de 2 Mbps a 16 Mbps, con alta latencia)

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**CONEXIÓN \_ TIPO \_ BANDA \_ ANCHA ALTA** (4 (0x4))


</dt> <dd>

Banda ancha de alta velocidad (de 2 Mbps a 10 Mbps)

</dd> <dt>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**CONEXIÓN \_ TYPE \_ WAN** (5 (0x5))


</dt> <dd>

Red de área extensa (WAN) (10 Mbps o superior, con alta latencia)

</dd> <dt>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**CONEXIÓN \_ TYPE \_ LAN** (6 (0x6))


</dt> <dd>

Red de área local (LAN) (10 Mbps o superior)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                             |
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

 

 





