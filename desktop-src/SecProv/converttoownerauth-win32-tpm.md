---
description: Convierte una entrada de frase de contraseña proporcionada por el usuario en una autorización de propietario de 20 bytes que se puede usar para interactuar con el TPM. Los métodos como TakeOwnership y ResetAuthLockOut requieren el valor de autorización de propietario resultante.
ms.assetid: 69eed934-1668-495a-b5b7-cd4a87df1ab3
title: Método ConvertToOwnerAuth de la Win32_Tpm clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ConvertToOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 88d1b0f2056d6a10ac623421a7fe261acb832657d08c030ab3247f0acf1a0629
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004653"
---
# <a name="converttoownerauth-method-of-the-win32_tpm-class"></a>Método ConvertToOwnerAuth de la clase Tpm de \_ Win32

El **método ConvertToOwnerAuth** de la clase [**\_ Tpm de Win32**](win32-tpm.md) convierte una entrada de frase de contraseña proporcionada por el usuario en una autorización de propietario de 20 bytes que se puede usar para interactuar con el TPM. Métodos como [**TakeOwnership**](takeownership-win32-tpm.md) y [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) requieren el valor de autorización de propietario resultante.

El proceso de conversión sigue las especificaciones de [la Trusted Computing Group](https://www.trustedcomputinggroup.org/).

## <a name="syntax"></a>Sintaxis


```mof
uint32 ConvertToOwnerAuth(
  [in]  string OwnerPassPhrase,
  [out] string OwnerAuth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OwnerPassPhrase* \[ En\]
</dt> <dd>

Tipo: **cadena**

Cadena que se convertirá en un valor de autorización de propietario. La cadena puede contener cualquier número de caracteres alfanuméricos.

</dd> <dt>

*OwnerAuth* \[ out\]
</dt> <dd>

Tipo: **cadena**

Cadena derivada del parámetro *OwnerPassPhrase.* Este valor es un valor binario de 20 bytes codificado en una cadena terminada en **null** de 28 bytes base64.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

En las tablas siguientes se enumeran algunos de los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Una cadena con codificación UNICODE UTF-16LE se convierte en el valor de autorización del propietario de TPM de 20 bytes tomando el hash SHA-1 de la representación binaria de la cadena. La **terminación** null de la cadena Unicode no se incluye en el hash. No se usa sal en el hash SHA-1.

Por ejemplo, para convertir la frase de contraseña del propietario de TPM "1Sample" en un valor de autorización de propietario de TPM, el hash SHA-1 se toma de la siguiente secuencia de bytes:

`0x31 0x00 0x53 0x00 0x61 0x00 0x6D 0x00 0x70 0x00 0x6C 0x00 0x65 0x00`

Para convertir una frase de contraseña de longitud cero en un valor de autorización de propietario, se toma el hash SHA-1 de la secuencia de bytes **NULL.**

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
</dt> <dt>

[**TakeOwnership**](takeownership-win32-tpm.md)
</dt> </dl>

 

 
