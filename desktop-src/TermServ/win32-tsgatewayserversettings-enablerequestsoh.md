---
title: Método EnableRequestSOH de la clase Win32_TSGatewayServerSettings
description: EnableRequestSOH ya no está disponible.
ms.assetid: 4feb7530-cced-4ead-a1fb-679b81442bb3
ms.tgt_platform: multiple
keywords:
- Método EnableRequestSOH Servicios de Escritorio remoto
- Método EnableRequestSOH Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método EnableRequestSOH
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableRequestSOH
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90ed6a3929b50d13a27ec559aab534f9e06f738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676914"
---
# <a name="enablerequestsoh-method-of-the-win32_tsgatewayserversettings-class"></a>Método EnableRequestSOH de la \_ clase TSGatewayServerSettings de Win32

\[El método **EnableRequestSOH** ya no está disponible a partir de Windows Server 2016.\]

Habilita o deshabilita las solicitudes de un informe de mantenimiento (SoH).

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnableRequestSOH(
  [in] boolean RequestSOH
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RequestSOH* \[ de\]
</dt> <dd>

Especifique **true** para habilitar la característica o **false** para deshabilitarla.

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
| Fin de compatibilidad de servidor<br/>    | Windows Server 2012 R2<br/>                                                        |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

