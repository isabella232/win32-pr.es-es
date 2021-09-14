---
title: Método EnableCentralCAP de la Win32_TSGatewayServerSettings clase
description: Controla la propiedad CentralCAPEnabled, que controla las directivas de Servicios de Escritorio remoto de autorización de conexión (RD \ 160; CAP) para el servidor Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).
ms.assetid: 43e476df-714d-43bd-b40f-33511b7757a4
ms.tgt_platform: multiple
keywords:
- Método EnableCentralCAP Servicios de Escritorio remoto
- Método EnableCentralCAP Servicios de Escritorio remoto , Win32_TSGatewayServerSettings clase
- Win32_TSGatewayServerSettings clase Servicios de Escritorio remoto , método EnableCentralCAP
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableCentralCAP
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 933e91a89f9a5afdcd2ae85fa6cb097ef0c29cd2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170633"
---
# <a name="enablecentralcap-method-of-the-win32_tsgatewayserversettings-class"></a>Método EnableCentralCAP de la clase \_ TSGatewayServerSettings de Win32

Controla la **propiedad CentralCAPEnabled,** que controla las directivas Servicios de Escritorio remoto autorización de conexión (CAP de Escritorio remoto) para el servidor Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnableCentralCAP(
  [in] boolean CentralCAPEnabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CentralCAPEnabled* \[ En\]
</dt> <dd>

Si se establece en **True,** se usarán las CA de Escritorio remoto de los servidores CAP de Escritorio remoto centrales. Si se establece en **False**, solo se usarán las directivas del servidor local.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Observaciones

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TSGatewayServerSettings de Win32 \_**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

