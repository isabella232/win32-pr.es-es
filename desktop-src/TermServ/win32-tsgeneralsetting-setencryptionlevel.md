---
title: SetEncryptionLevel method of the Win32_TSGeneralSetting class (Establecer el método SetEncryptionLevel de la clase Win32_TSGeneralSetting)
description: El método SetEncryptionLevel establece el nivel de cifrado.
ms.assetid: 1822c4dc-bce6-489f-b21e-f96faffd2fa5
ms.tgt_platform: multiple
keywords:
- Método SetEncryptionLevel Servicios de Escritorio remoto
- Método SetEncryptionLevel Servicios de Escritorio remoto , Win32_TSGeneralSetting clase
- Win32_TSGeneralSetting clase Servicios de Escritorio remoto método , SetEncryptionLevel
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetEncryptionLevel
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54aacf931a66d6d4bdd4daa24a6432e4caa7fb01695aebbe4324b17ab5f2bed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348847"
---
# <a name="setencryptionlevel-method-of-the-win32_tsgeneralsetting-class"></a>Método SetEncryptionLevel de la clase \_ TSGeneralSetting de Win32

El **método SetEncryptionLevel** establece el nivel de cifrado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetEncryptionLevel(
  [in] uint32 MinEncryptionLevel
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MinEncryptionLevel* \[ En\]
</dt> <dd>

Nivel de cifrado mínimo que se establecerá.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Bajo nivel de cifrado. Solo los datos enviados desde el cliente al servidor se cifran mediante el cifrado de 56 bits. Tenga en cuenta que los datos enviados desde el servidor al cliente no están cifrados.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Nivel de cifrado compatible con el cliente. Todos los datos enviados de cliente a servidor y de servidor a cliente se cifran con el nivel máximo de clave admitido por el cliente.

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Alto nivel de cifrado. Todos los datos enviados de cliente a servidor y de servidor a cliente se cifran mediante un cifrado seguro de 128 bits. Los clientes que no admiten este nivel de cifrado no se pueden conectar.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Cifrado compatible con FIPS. Todos los datos enviados de cliente a servidor y de servidor a cliente se cifran y descifran con los algoritmos de cifrado Estándar federal de procesamiento de información (FIPS) mediante los módulos criptográficos de Microsoft. FIPS es un estándar denominado "Requisitos de seguridad para módulos criptográficos". FIPS 140-1 (1994) y FIPS 140-2 (2001) describen los requisitos gubernamentales para los módulos criptográficos de hardware y software que se usan en la administración gubernamental de Estados Unidos.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve Correcto si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_TSGeneralSetting de Win32**](win32-tsgeneralsetting.md)
</dt> </dl>

 

