---
title: SetEncryptionLevel method of the Win32_TSGeneralSetting class (Establecer el método SetEncryptionLevel de la clase Win32_TSGeneralSetting)
description: El método SetEncryptionLevel establece el nivel de cifrado.
ms.assetid: 1822c4dc-bce6-489f-b21e-f96faffd2fa5
ms.tgt_platform: multiple
keywords:
- Método SetEncryptionLevel Servicios de Escritorio remoto
- Método SetEncryptionLevel Servicios de Escritorio remoto, clase Win32_TSGeneralSetting
- Win32_TSGeneralSetting de clase Servicios de Escritorio remoto, método SetEncryptionLevel
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
ms.openlocfilehash: b1fbe727c75851bb13252d196e1fe7d599f881c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150591"
---
# <a name="setencryptionlevel-method-of-the-win32_tsgeneralsetting-class"></a>Método SetEncryptionLevel de la \_ clase TSGeneralSetting de Win32

El método **SetEncryptionLevel** establece el nivel de cifrado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetEncryptionLevel(
  [in] uint32 MinEncryptionLevel
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MinEncryptionLevel* \[ de\]
</dt> <dd>

Nivel mínimo de cifrado que se va a establecer.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Bajo nivel de cifrado. Solo los datos enviados desde el cliente al servidor se cifran mediante el cifrado de 56 bits. Tenga en cuenta que no se cifran los datos enviados desde el servidor al cliente.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Nivel de cifrado compatible con el cliente. Todos los datos enviados del cliente al servidor y del servidor al cliente se cifran con el nivel de clave máximo admitido por el cliente.

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Alto nivel de cifrado. Todos los datos enviados del cliente al servidor y del servidor al cliente se cifran mediante cifrado de 128 bits seguro. Los clientes que no admiten este nivel de cifrado no se pueden conectar.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Cifrado compatible con FIPS. Todos los datos enviados del cliente al servidor y del servidor al cliente están cifrados y descifrados con los algoritmos de cifrado de Estándar federal de procesamiento de información (FIPS) mediante los módulos criptográficos de Microsoft. FIPS es un estándar titulado "requisitos de seguridad para los módulos criptográficos". FIPS 140-1 (1994) y FIPS 140-2 (2001) describen los requisitos gubernamentales para los módulos criptográficos de hardware y software que se usan en el gobierno de EE. UU.

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
</dt> </dl>

 

