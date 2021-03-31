---
title: Método SetSecurityLayer de la clase Win32_TSGeneralSetting
description: El método SetSecurityLayer establece el nivel de seguridad.
ms.assetid: 3b894494-2180-4f1d-8e67-a66c679d286c
ms.tgt_platform: multiple
keywords:
- Método SetSecurityLayer Servicios de Escritorio remoto
- Método SetSecurityLayer Servicios de Escritorio remoto, clase Win32_TSGeneralSetting
- Win32_TSGeneralSetting de clase Servicios de Escritorio remoto, método SetSecurityLayer
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
ms.openlocfilehash: b5e04c3f7e5a58ec8de345d570e36b35c7eb1e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996491"
---
# <a name="setsecuritylayer-method-of-the-win32_tsgeneralsetting-class"></a>Método SetSecurityLayer de la \_ clase TSGeneralSetting de Win32

El método **SetSecurityLayer** establece el nivel de seguridad.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetSecurityLayer(
  [in] uint32 SecurityLayer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SecurityLayer* \[ de\]
</dt> <dd>

Nivel de seguridad que se va a establecer. Si el nivel de cifrado actual es 1, el valor 2 para *SecurityLayer* no es válido.

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Nivel de seguridad de RDP** (0)


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

SSL (TLS 1,0) se usará para la autenticación del servidor, así como para cifrar todos los datos transferidos entre el servidor y el cliente. Esta configuración requiere que el servidor tenga un certificado compatible con SSL. Esta configuración no es compatible con un valor de **MinEncryptionLevel** de 1.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve SUCCESS si es correcto; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

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
</dt> <dt>

[**SetEncryptionLevel**](win32-tsgeneralsetting-setencryptionlevel.md)
</dt> </dl>

 

