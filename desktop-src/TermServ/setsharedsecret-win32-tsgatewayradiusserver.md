---
title: Método SetSharedSecret de la clase Win32_TSGatewayRADIUSServer
description: Establece la propiedad SharedSecret de este servidor Servicio de autenticación remota telefónica de usuario (RADIUS).
ms.assetid: b4f7afb7-862f-4c30-b60a-aa6a8dbbe3e9
ms.tgt_platform: multiple
keywords:
- Método SetSharedSecret Servicios de Escritorio remoto
- Método SetSharedSecret Servicios de Escritorio remoto, clase Win32_TSGatewayRADIUSServer
- Win32_TSGatewayRADIUSServer de clase Servicios de Escritorio remoto, método SetSharedSecret
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.SetSharedSecret
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f17e22061467194bdb09fc3f2c6105706f58e587
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802924"
---
# <a name="setsharedsecret-method-of-the-win32_tsgatewayradiusserver-class"></a>Método SetSharedSecret de la \_ clase TSGatewayRADIUSServer de Win32

Establece la propiedad **SharedSecret** de este servidor servicio de autenticación remota telefónica de usuario (RADIUS).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetSharedSecret(
  [in] string SharedSecret
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SharedSecret* \[ de\]
</dt> <dd>

Nuevo secreto compartido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Para llamar a este método, debe ser miembro del grupo administradores.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

