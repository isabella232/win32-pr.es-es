---
title: Método SetIPAndPort de la Win32_TSGatewayServerSettings clase
description: Establece la dirección IP de escucha y el número de puerto para el transporte especificado.
ms.assetid: f46f4660-31ce-4513-b93d-acd50b42ae0a
ms.tgt_platform: multiple
keywords:
- Método SetIPAndPort Servicios de Escritorio remoto
- Método SetIPAndPort Servicios de Escritorio remoto , Win32_TSGatewayServerSettings clase
- Win32_TSGatewayServerSettings clase Servicios de Escritorio remoto , método SetIPAndPort
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af40c52523869e07268a26d858e0e70b933431a6583998c9d0041f476678d243
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137978"
---
# <a name="setipandport-method-of-the-win32_tsgatewayserversettings-class"></a>Método SetIPAndPort de la clase \_ TSGatewayServerSettings de Win32

Establece la dirección IP de escucha y el número de puerto para el transporte especificado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetIPAndPort(
  [in] uint16  TransportType,
  [in] string  IPAddress,
  [in] uint16  Port,
  [in] boolean OverrideExisting
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

*IPAddress* \[ En\]
</dt> <dd>

Especifica la dirección IP de escucha, en formato octeto (por ejemplo, "192.168.1.1").

</dd> <dt>

*Puerto* \[ En\]
</dt> <dd>

Especifica el número de puerto de escucha.

</dd> <dt>

*OverrideExisting* \[ En\]
</dt> <dd>

Indica si se debe invalidar el enlace ip/puerto existente para HTTP. Este parámetro solo se usa si el *parámetro TransportType* contiene 0 (RPC sobre HTTP) o 1 (HTTP).

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





