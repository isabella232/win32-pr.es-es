---
description: Restablece el valor Storage autorización de clave raíz (SRK) para que sea compatible con el sistema operativo.
ms.assetid: af008733-b43c-4017-9e79-bdd98f2e20b6
title: Método ResetSrkAuth de la Win32_Tpm clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetSrkAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 01f7536833529fd0d425f6064cfcdab11ac99c9cf1d6ab6ae7daf0c8b995d566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004303"
---
# <a name="resetsrkauth-method-of-the-win32_tpm-class"></a>Método ResetSrkAuth de la clase Tpm de \_ Win32

El **método ResetSrkAuth** de la clase [**\_ Tpm de Win32**](win32-tpm.md) restablece el valor de autorización Storage Root Key (SRK) para que sea compatible con el sistema operativo.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ResetSrkAuth(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OwnerAuth* \[ in, opcional\]
</dt> <dd>

Tipo: **cadena**

Cadena que identifica al propietario del TPM. Esta cadena debe ser una cadena terminada en NULL codificada en base64 que contenga exactamente 20 bytes de datos binarios. Use el [**método ConvertToOwnerAuth para**](converttoownerauth-win32-tpm.md) traducir una frase de contraseña a este formato esperado. El *parámetro OwnerAuth* se lee del Registro si no se proporciona ninguno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                                                         | Descripción                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                         | Método realizado correctamente.<br/>                                                                                                                                                |
| <dl> <dt> **TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>             | El valor de autorización de propietario proporcionado no puede satisfacer la solicitud.<br/>                                                                                                        |
| <dl> <dt>**TPM \_ E \_ DEFENDER \_ LOCK \_ RUNNING**</dt> <dt>2150107139 (0x80280803)</dt> </dl> | El TPM está en defensa frente a ataques de diccionario y está en un período de tiempo de espera. Para obtener más información, vea el [**método ResetAuthLockOut.**](resetauthlockout-win32-tpm.md)<br/> |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                      |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tpm de \_ Win32**](win32-tpm.md)
</dt> </dl>

 

 
