---
title: Método EnableTransport de la Win32_TSGatewayServerSettings clase
description: Habilita o deshabilita el transporte especificado.
ms.assetid: 95c599d7-56c3-462a-9c7d-2ecf8fc55da1
ms.tgt_platform: multiple
keywords:
- Método EnableTransport Servicios de Escritorio remoto
- Método EnableTransport Servicios de Escritorio remoto , Win32_TSGatewayServerSettings clase
- Win32_TSGatewayServerSettings clase Servicios de Escritorio remoto método , EnableTransport
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableTransport
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a14e7ee94eb02e1358d66b9965ecc2323d5b773
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891089"
---
# <a name="enabletransport-method-of-the-win32_tsgatewayserversettings-class"></a>Método EnableTransport de la clase \_ TSGatewayServerSettings de Win32

Habilita o deshabilita el transporte especificado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnableTransport(
  [in] uint16  TransportType,
  [in] boolean Enable
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

RPC sobre transporte HTTP.

</dd> <dt>

1
</dt> <dd>

Transporte HTTP.

</dd> <dt>

2
</dt> <dd>

Transporte UDP.

</dd> </dl> </dd> <dt>

*Habilitar* \[ En\]
</dt> <dd>

Especifica si el transporte está habilitado o deshabilitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                           |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TSGatewayServerSettings de Win32 \_**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





