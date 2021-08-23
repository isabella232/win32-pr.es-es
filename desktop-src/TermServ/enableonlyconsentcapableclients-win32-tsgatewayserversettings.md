---
title: Método EnableOnlyConsentCapableClients de la Win32_TSGatewayServerSettings clase
description: Establece la propiedad OnlyConsentCapableClients.
ms.assetid: abc91ea8-0f3c-4b7c-9091-3c8193e610da
ms.tgt_platform: multiple
keywords:
- Método EnableOnlyConsentCapableClients Servicios de Escritorio remoto
- Método EnableOnlyConsentCapableClients Servicios de Escritorio remoto , Win32_TSGatewayServerSettings clase
- Win32_TSGatewayServerSettings clase Servicios de Escritorio remoto , método EnableOnlyConsentCapableClients
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableOnlyConsentCapableClients
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 254eaa15a899eb5612658a4a9ed9b3a7677ca928e202cf5ddebd653d703e31da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059633"
---
# <a name="enableonlyconsentcapableclients-method-of-the-win32_tsgatewayserversettings-class"></a>Método EnableOnlyConsentCapableClients de la clase \_ TSGatewayServerSettings de Win32

Establece la **propiedad OnlyConsentCapableClients.**

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnableOnlyConsentCapableClients(
  [in] boolean OnlyConsentCapableClients
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OnlyConsentCapableClients* \[ En\]
</dt> <dd>

Tipo: **booleano**

Especifica el nuevo valor para la **propiedad OnlyConsentCapableClients.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

 

