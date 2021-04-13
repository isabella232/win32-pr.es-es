---
title: Método SetUserAuthenticationRequired de la clase Win32_TSGeneralSetting
description: Habilita o deshabilita el requisito de que los usuarios se deben autenticar en el momento de la conexión estableciendo el valor de la propiedad UserAuthenticationRequired.
ms.assetid: a0581326-fecc-4d23-87bf-3696c93366e8
ms.tgt_platform: multiple
keywords:
- Método SetUserAuthenticationRequired Servicios de Escritorio remoto
- Método SetUserAuthenticationRequired Servicios de Escritorio remoto, clase Win32_TSGeneralSetting
- Win32_TSGeneralSetting de clase Servicios de Escritorio remoto, método SetUserAuthenticationRequired
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetUserAuthenticationRequired
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c0eb711d2146130ff0fd879953fc71fcba965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359824"
---
# <a name="setuserauthenticationrequired-method-of-the-win32_tsgeneralsetting-class"></a>Método SetUserAuthenticationRequired de la \_ clase TSGeneralSetting de Win32

Habilita o deshabilita el requisito de que los usuarios se deben autenticar en el momento de la conexión estableciendo el valor de la propiedad **UserAuthenticationRequired** en la clase [**\_ TSGeneralSetting de Win32**](win32-tsgeneralsetting.md) . Si **es true**, lo que significa habilitado, **UserAuthenticationRequired** requiere autenticación de usuario en el momento de la conexión para aumentar la protección del servidor frente a ataques de red. Solo los clientes Protocolo de escritorio remoto (RDP) que admiten la versión 6,0 o posterior de RDP pueden conectarse. Para evitar interrupciones para los usuarios remotos, se recomienda que implemente los clientes RDP que admitan la versión de protocolo adecuada antes de habilitar la propiedad.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetUserAuthenticationRequired(
  [in] uint32 UserAuthenticationRequired
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*UserAuthenticationRequired* \[ de\]
</dt> <dd>

Indica si se requiere la autenticación del usuario.

<dt>

0 (0X0)
</dt> <dd>

Deshabilitar requisito de que el usuario debe estar autenticado

</dd> <dt>

1 (0x1)
</dt> <dd>

Habilita el requisito de que el usuario debe estar autenticado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md)
</dt> </dl>

 

