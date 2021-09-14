---
title: Método GetIPAndPort de la Win32_TSGatewayServerSettings clase
description: Obtiene la dirección IP de escucha y el número de puerto para el transporte especificado.
ms.assetid: e12451c3-2641-49e1-bd35-f7cab37865ae
ms.tgt_platform: multiple
keywords:
- Método GetIPAndPort Servicios de Escritorio remoto
- Método GetIPAndPort Servicios de Escritorio remoto , Win32_TSGatewayServerSettings clase
- Win32_TSGatewayServerSettings clase Servicios de Escritorio remoto , método GetIPAndPort
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260cc45961720ae8d175d4df3e84edc7a0c15c13
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968487"
---
# <a name="getipandport-method-of-the-win32_tsgatewayserversettings-class"></a>Método GetIPAndPort de la clase \_ TSGatewayServerSettings de Win32

Obtiene la dirección IP de escucha y el número de puerto para el transporte especificado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetIPAndPort(
  [in]  uint16 TransportType,
  [out] string IPAddress,
  [out] uint16 Port
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TransportType* \[ En\]
</dt> <dd>

Especifica el tipo de transporte. Debe ser uno de los siguientes valores.

<dt>

0
</dt> <dd>

RPC a través del transporte HTTP.

</dd> <dt>

1
</dt> <dd>

Transporte HTTP.

</dd> <dt>

2
</dt> <dd>

Transporte UDP.

</dd> </dl> </dd> <dt>

*IPAddress* \[ out\]
</dt> <dd>

Cadena que recibe la dirección IP de escucha, en formato octeto (por ejemplo, "192.168.1.1").

</dd> <dt>

*Puerto* \[ out\]
</dt> <dd>

Especifica el número de puerto de escucha.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                           |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





