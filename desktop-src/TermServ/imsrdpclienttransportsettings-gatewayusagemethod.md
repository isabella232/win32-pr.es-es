---
title: Propiedad IMsRdpClientTransportSettings GatewayUsageMethod
description: Especifica cuándo se debe usar un servidor Escritorio remoto gateway (puerta de enlace de Escritorio remoto).
ms.assetid: 0644c413-9ff7-42c1-a38e-e1ce546972ff
ms.tgt_platform: multiple
keywords:
- Propiedad GatewayUsageMethod Servicios de Escritorio remoto
- Propiedad GatewayUsageMethod Servicios de Escritorio remoto , interfaz IMsRdpClientTransportSettings
- Interfaz IMsRdpClientTransportSettings Servicios de Escritorio remoto , propiedad GatewayUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUsageMethod
- IMsRdpClientTransportSettings.get_GatewayUsageMethod
- IMsRdpClientTransportSettings.put_GatewayUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f07bc10c67d01f957e588d1b50085e57b0fa10b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886033"
---
# <a name="imsrdpclienttransportsettingsgatewayusagemethod-property"></a>Propiedad IMsRdpClientTransportSettings::GatewayUsageMethod

Especifica cuándo se debe usar un servidor Escritorio remoto gateway (puerta de enlace de Escritorio remoto).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_GatewayUsageMethod(
  [in]  ULONG ulProxyMethod
);

HRESULT get_GatewayUsageMethod(
  [out] ULONG *pulProxyUsageMethod
);
```



## <a name="property-value"></a>Valor de propiedad

Variable **ULONG que** especifica el método de uso del servidor de puerta de enlace de Escritorio remoto. Este parámetro puede ser uno de los valores siguientes.

<dt>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC \_ MODO \_ PROXY \_ NINGUNO \_ DIRECTO** (0 (0x0))


</dt> <dd>

No use un servidor de puerta de enlace de Escritorio remoto. En la interfaz Conexión a Escritorio remoto cliente de escritorio remoto (RDC), la casilla Omitir servidor de puerta de enlace de Escritorio remoto para **direcciones locales** está desactivada.

</dd> <dt>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC \_ MODO \_ PROXY \_ DIRECTO** (1 (0x1))


</dt> <dd>

Use siempre un servidor de puerta de enlace de Escritorio remoto. En la interfaz de usuario del cliente RDC, la casilla Omitir servidor de puerta de enlace de Escritorio remoto para **direcciones locales** está desactivada.

</dd> <dt>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC \_ DETECCIÓN \_ DEL \_ MODO PROXY** (2 (0x2))


</dt> <dd>

Use un servidor de puerta de enlace de Escritorio remoto si no se puede realizar una conexión directa con el servidor host de sesión de Escritorio remoto. En la interfaz de usuario del cliente RDC, la casilla Omitir servidor de puerta de enlace de Escritorio remoto para **direcciones locales** está activada.

</dd> <dt>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC \_ MODO \_ PROXY \_ PREDETERMINADO** (3 (0x3))


</dt> <dd>

Use la configuración predeterminada del servidor de puerta de enlace de Escritorio remoto.

</dd> <dt>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC \_ MODO PROXY \_ \_ NINGUNA \_ DETECCIÓN** (4 (0x4))


</dt> <dd>

No use un servidor de puerta de enlace de Escritorio remoto. En la interfaz de usuario del cliente RDC, la casilla Omitir servidor de puerta de enlace de Escritorio remoto para **direcciones locales** está activada.

</dd> </dl>

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings se define como 720298C0-A099-46f5-9F82-96921BAE4701<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





