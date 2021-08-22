---
title: Método SetSecurityLayer de la Win32_TSGeneralSetting clase
description: El método SetSecurityLayer establece la capa de seguridad.
ms.assetid: 3b894494-2180-4f1d-8e67-a66c679d286c
ms.tgt_platform: multiple
keywords:
- Método SetSecurityLayer Servicios de Escritorio remoto
- Método SetSecurityLayer Servicios de Escritorio remoto , Win32_TSGeneralSetting clase
- Win32_TSGeneralSetting clase Servicios de Escritorio remoto , método SetSecurityLayer
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetSecurityLayer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e01f761b63be028e2c507644f160b6742f9d781e517ea03ce549e3ac84419c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513875"
---
# <a name="setsecuritylayer-method-of-the-win32_tsgeneralsetting-class"></a>Método SetSecurityLayer de la clase \_ TSGeneralSetting de Win32

El **método SetSecurityLayer** establece la capa de seguridad.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetSecurityLayer(
  [in] uint32 SecurityLayer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SecurityLayer* \[ En\]
</dt> <dd>

Capa de seguridad que se establecerá. Si el nivel de cifrado actual es 1, un valor de 2 para *SecurityLayer* no es válido.

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Capa de seguridad RDP** (0)


</dt> <dd>

En las comunicaciones entre servidor y cliente se usará el cifrado RDP nativo.

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (1)


</dt> <dd>

Se usará la capa más segura que admita el cliente. Si se admite, se usará SSL (TLS 1.0).

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span id="SSL"></span><span id="ssl"></span>**SSL** (2)


</dt> <dd>

SSL (TLS 1.0) se usará para la autenticación del servidor, así como para cifrar todos los datos transferidos entre el servidor y el cliente. Esta configuración requiere que el servidor tenga un certificado compatible con SSL. Esta configuración no es compatible con un **valor MinEncryptionLevel** de 1.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve Success si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md)
</dt> <dt>

[**SetEncryptionLevel**](win32-tsgeneralsetting-setencryptionlevel.md)
</dt> </dl>

 

