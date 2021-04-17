---
description: Convierte la entrada de una frase de contraseña proporcionada por el usuario en una autorización de propietario de 20 bytes que se puede usar para interactuar con el TPM. Los métodos como TakeOwnership y ResetAuthLockOut requieren el valor de autorización de propietario resultante.
ms.assetid: 69eed934-1668-495a-b5b7-cd4a87df1ab3
title: Método ConvertToOwnerAuth de la clase Win32_Tpm
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
ms.openlocfilehash: f3de5803d10458156fb453e964d782f7c9760333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687900"
---
# <a name="converttoownerauth-method-of-the-win32_tpm-class"></a>Método ConvertToOwnerAuth de la \_ clase Win32 TPM

El método **ConvertToOwnerAuth** de la clase de [**Win32 \_ TPM**](win32-tpm.md) traduce una entrada de frase de contraseña proporcionada por el usuario en una autorización de propietario de 20 bytes que se puede usar para interactuar con el TPM. Los métodos como [**TakeOwnerShip**](takeownership-win32-tpm.md) y [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) requieren el valor de autorización de propietario resultante.

El proceso de conversión sigue las especificaciones del [Trusted Computing Group](https://www.trustedcomputinggroup.org/).

## <a name="syntax"></a>Sintaxis


```mof
uint32 ConvertToOwnerAuth(
  [in]  string OwnerPassPhrase,
  [out] string OwnerAuth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OwnerPassPhrase* \[ de\]
</dt> <dd>

Tipo: **String**

Cadena que se va a convertir en un valor de autorización de propietario. La cadena puede contener cualquier número de caracteres alfanuméricos.

</dd> <dt>

*OwnerAuth* \[ enuncia\]
</dt> <dd>

Tipo: **String**

Cadena derivada del parámetro *OwnerPassPhrase* . Este valor es un valor binario de 20 bytes codificado en una cadena terminada en **null** de 28 bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

En las tablas siguientes se enumeran algunos de los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Una cadena codificada UTF-16LE de Unicode se convierte en el valor de autorización de propietario de TPM de 20 bytes tomando el hash SHA-1 de la representación binaria de la cadena. La terminación **null** de la cadena Unicode no se incluye en el hash. No se usa ningún valor Salt en el hash SHA-1.

Por ejemplo, para convertir la frase de contraseña de propietario de TPM "1Sample" en un valor de autorización de propietario de TPM, el hash de SHA-1 se toma de la siguiente secuencia de bytes:

`0x31 0x00 0x53 0x00 0x61 0x00 0x6D 0x00 0x70 0x00 0x6C 0x00 0x65 0x00`

Para convertir una frase de contraseña de longitud cero en un valor de autorización de propietario, se toma el hash SHA-1 de la secuencia de bytes **null** .

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                      |
| Espacio de nombres<br/>                | \\MicrosoftTpm de \\ seguridad de cimv2 raíz \\<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ TPM. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TPM de Win32 \_**](win32-tpm.md)
</dt> <dt>

[**TakeOwnership**](takeownership-win32-tpm.md)
</dt> </dl>

 

 
