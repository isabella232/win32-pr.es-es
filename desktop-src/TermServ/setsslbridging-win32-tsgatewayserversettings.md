---
title: Método SetSslBridging de la clase Win32_TSGatewayServerSettings
description: Establece el tipo de protocolo de puente SSL que va a usar el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 11885b8b-491e-4d90-b4d4-f0a0fbe68cb1
ms.tgt_platform: multiple
keywords:
- Método SetSslBridging Servicios de Escritorio remoto
- Método SetSslBridging Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método SetSslBridging
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422417"
---
# <a name="setsslbridging-method-of-the-win32_tsgatewayserversettings-class"></a>Método SetSslBridging de la \_ clase TSGatewayServerSettings de Win32

Establece el tipo de protocolo de puente SSL que va a usar el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto). Este valor se almacena en la propiedad **SslBridging** .

> [!IMPORTANT]
> Cuando se cambia el tipo de protocolo de puente SSL con este método, el servicio de puerta de enlace de escritorio remoto debe reiniciarse para que este cambio surta efecto.

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetSslBridging(
  [in] uint32 SslBridging
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SslBridging* \[ de\]
</dt> <dd>

Tipo: **UInt32**

Especifica el nuevo valor de protocolo de puente SSL. Puede ser uno de los valores siguientes.

<dt>

0
</dt> <dd>

Sin puentes SSL.

</dd> <dt>

1
</dt> <dd>

Puente de HTTPS a HTTP.

</dd> <dt>

2
</dt> <dd>

Puente de HTTPS a HTTPS.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Para llamar a este método, debe ser miembro del grupo administradores.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                        |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

