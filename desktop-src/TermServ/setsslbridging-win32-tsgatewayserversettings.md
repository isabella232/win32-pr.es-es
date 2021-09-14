---
title: Método SetSslBridging de la Win32_TSGatewayServerSettings clase
description: Establece el tipo de puente SSL que va a usar el servidor Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).
ms.assetid: 11885b8b-491e-4d90-b4d4-f0a0fbe68cb1
ms.tgt_platform: multiple
keywords:
- Método SetSslBridging Servicios de Escritorio remoto
- Método SetSslBridging Servicios de Escritorio remoto , Win32_TSGatewayServerSettings clase
- Win32_TSGatewayServerSettings clase Servicios de Escritorio remoto , método SetSslBridging
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetSslBridging
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77181fb8d8661ec7ea7dc0ce70532281fb9c1bde
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374423"
---
# <a name="setsslbridging-method-of-the-win32_tsgatewayserversettings-class"></a>Método SetSslBridging de la clase \_ TSGatewayServerSettings de Win32

Establece el tipo de puente SSL que va a usar el servidor Escritorio remoto Gateway (puerta de enlace de Escritorio remoto). Este valor se almacena en la **propiedad SslBridging.**

> [!IMPORTANT]
> Cuando se cambia el tipo de puente SSL con este método, se debe reiniciar el servicio puerta de enlace de Escritorio remoto para que este cambio suba efecto.

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetSslBridging(
  [in] uint32 SslBridging
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SslBridging* \[ En\]
</dt> <dd>

Tipo: **uint32**

Especifica el nuevo valor de puente SSL. Puede ser uno de los siguientes valores.

<dt>

0
</dt> <dd>

Sin protocolo de puente SSL.

</dd> <dt>

1
</dt> <dd>

Protocolo de puente HTTPS a HTTP.

</dd> <dt>

2
</dt> <dd>

Protocolo de puente https a HTTPS.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Observaciones

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                        |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TSGatewayServerSettings de Win32 \_**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

