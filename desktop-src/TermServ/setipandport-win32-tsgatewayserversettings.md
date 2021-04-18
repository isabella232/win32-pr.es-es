---
title: Método SetIPAndPort de la clase Win32_TSGatewayServerSettings
description: Establece la dirección IP de escucha y el número de puerto para el transporte especificado.
ms.assetid: f46f4660-31ce-4513-b93d-acd50b42ae0a
ms.tgt_platform: multiple
keywords:
- Método SetIPAndPort Servicios de Escritorio remoto
- Método SetIPAndPort Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método SetIPAndPort
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
ms.openlocfilehash: 88870cce628a94ca34b38ccf315edc87a1a734b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534072"
---
# <a name="setipandport-method-of-the-win32_tsgatewayserversettings-class"></a>Método SetIPAndPort de la \_ clase TSGatewayServerSettings de Win32

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

*TransportType* \[ de\]
</dt> <dd>

Especifica el tipo de transporte. Debe ser uno de los valores siguientes.

<dt>

0
</dt> <dd>

Transporte RPC a través de HTTP.

</dd> <dt>

1
</dt> <dd>

Transporte HTTP.

</dd> <dt>

2
</dt> <dd>

Transporte UDP.

</dd> </dl> </dd> <dt>

*Dirección IP* \[ de\]
</dt> <dd>

Especifica la dirección IP de escucha, en forma de octeto (por ejemplo, "192.168.1.1").

</dd> <dt>

*Puerto* \[ de de\]
</dt> <dd>

Especifica el número de puerto de escucha.

</dd> <dt>

*OverrideExisting* \[ de\]
</dt> <dd>

Indica si se va a invalidar el enlace IP/puerto existente para HTTP. Este parámetro solo se usa si el parámetro *TransportType* contiene 0 (RPC a través de http) o 1 (http).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                           |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





