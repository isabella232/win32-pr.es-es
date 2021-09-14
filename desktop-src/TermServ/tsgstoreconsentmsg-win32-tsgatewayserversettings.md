---
title: Método TSGStoreConsentMsg de la Win32_TSGatewayServerSettings clase
description: Actualiza el mensaje de consentimiento para el servidor de puerta de enlace.
ms.assetid: b3146d87-95af-4b6b-8c02-5ac4748fbe98
ms.tgt_platform: multiple
keywords:
- Método TSGStoreConsentMsg Servicios de Escritorio remoto
- Método TSGStoreConsentMsg Servicios de Escritorio remoto , Win32_TSGatewayServerSettings clase
- Win32_TSGatewayServerSettings clase Servicios de Escritorio remoto , método TSGStoreConsentMsg
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGStoreConsentMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907097739d21e1523aca3b719cdb5f18b6f3fa30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170602"
---
# <a name="tsgstoreconsentmsg-method-of-the-win32_tsgatewayserversettings-class"></a>Método TSGStoreConsentMsg de la clase \_ TSGatewayServerSettings de Win32

Actualiza el mensaje de consentimiento para el servidor de puerta de enlace.

## <a name="syntax"></a>Sintaxis


```mof
uint32 TSGStoreConsentMsg(
  [in] string TSGConMsgText
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TSGConMsgText* \[ En\]
</dt> <dd>

Tipo: **cadena**

Texto del mensaje de consentimiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                        |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

