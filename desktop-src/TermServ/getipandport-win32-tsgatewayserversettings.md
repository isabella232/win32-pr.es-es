---
title: Método GetIPAndPort de la clase Win32_TSGatewayServerSettings
description: Obtiene la dirección IP de escucha y el número de puerto para el transporte especificado.
ms.assetid: e12451c3-2641-49e1-bd35-f7cab37865ae
ms.tgt_platform: multiple
keywords:
- Método GetIPAndPort Servicios de Escritorio remoto
- Método GetIPAndPort Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método GetIPAndPort
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359690"
---
# <a name="getipandport-method-of-the-win32_tsgatewayserversettings-class"></a>Método GetIPAndPort de la \_ clase TSGatewayServerSettings de Win32

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

*Dirección IP* \[ enuncia\]
</dt> <dd>

Una cadena que recibe la dirección IP de escucha, en forma de octeto (por ejemplo, "192.168.1.1").

</dd> <dt>

*Puerto* \[ de enuncia\]
</dt> <dd>

Especifica el número de puerto de escucha.

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

 

 





