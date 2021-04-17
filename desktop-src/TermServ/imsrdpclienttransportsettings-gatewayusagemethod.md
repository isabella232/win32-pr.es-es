---
title: Propiedad GatewayUsageMethod de IMsRdpClientTransportSettings
description: Especifica cuándo se debe usar un servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 0644c413-9ff7-42c1-a38e-e1ce546972ff
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayUsageMethod
- Propiedad GatewayUsageMethod Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings, propiedad GatewayUsageMethod
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676638"
---
# <a name="imsrdpclienttransportsettingsgatewayusagemethod-property"></a>IMsRdpClientTransportSettings:: GatewayUsageMethod (propiedad)

Especifica cuándo se debe usar un servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).

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

Variable **ULong** que especifica el método de uso del servidor de puerta de enlace de escritorio remoto. Este parámetro puede ser uno de los valores siguientes.

<dt>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC \_ \_Modo proxy \_ ninguno \_ directo** (0 (0X0))


</dt> <dd>

No use un servidor de puerta de enlace de escritorio remoto. En la interfaz de usuario del cliente de Conexión a Escritorio remoto (RDC), la casilla **omitir el servidor de puerta de enlace de escritorio remoto para direcciones locales** está desactivada.

</dd> <dt>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC \_ \_Modo proxy \_ directo** (1 (0x1))


</dt> <dd>

Use siempre un servidor de puerta de enlace de escritorio remoto. En la interfaz de usuario del cliente RDC, se desactiva la casilla **omitir el servidor de puerta de enlace de escritorio remoto para direcciones locales** .

</dd> <dt>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC \_ \_ \_ Detección del modo proxy** (2 (0X2))


</dt> <dd>

Use un servidor de puerta de enlace de escritorio remoto si no se puede establecer una conexión directa con el servidor host de sesión de escritorio remoto. En la interfaz de usuario del cliente RDC, se activa la casilla **omitir el servidor de puerta de enlace de escritorio remoto para direcciones locales** .

</dd> <dt>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC \_ \_ \_ Valor predeterminado del modo proxy** (3 (0X3))


</dt> <dd>

Utilice la configuración predeterminada del servidor de puerta de enlace de escritorio remoto.

</dd> <dt>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC \_ No \_ hay \_ ninguna \_ detección de modo proxy** (4 (0x4))


</dt> <dd>

No use un servidor de puerta de enlace de escritorio remoto. En la interfaz de usuario del cliente RDC, se activa la casilla **omitir el servidor de puerta de enlace de escritorio remoto para direcciones locales** .

</dd> </dl>

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ correcto** si se realiza correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings se define como 720298C0-A099-46f5-9F82-96921BAE4701<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





