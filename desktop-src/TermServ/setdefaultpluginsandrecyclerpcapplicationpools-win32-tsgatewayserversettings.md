---
title: Método SetDefaultPluginsAndRecycleRpcApplicationPools de la clase Win32_TSGatewayServerSettings
description: Establece los complementos de autenticación y autorización actuales para el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) y recicla los grupos de aplicaciones RPC en IIS.
ms.assetid: 1eac9e42-e533-4020-b2b6-571063f18c3c
ms.tgt_platform: multiple
keywords:
- Método SetDefaultPluginsAndRecycleRpcApplicationPools Servicios de Escritorio remoto
- Método SetDefaultPluginsAndRecycleRpcApplicationPools Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método SetDefaultPluginsAndRecycleRpcApplicationPools
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetDefaultPluginsAndRecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9ead29e987b68ec3f041010be5dde64d8a2b54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996981"
---
# <a name="setdefaultpluginsandrecyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a>Método SetDefaultPluginsAndRecycleRpcApplicationPools de la \_ clase TSGatewayServerSettings de Win32

Establece los complementos de autenticación y autorización actuales para el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) y recicla los grupos de aplicaciones RPC en IIS.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetDefaultPluginsAndRecycleRpcApplicationPools();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Al llamar a este método, se desconectan todas las conexiones existentes.

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

 

