---
description: Indica si la contraseña numérica cumple los requisitos de formato especiales para este valor de autenticación.
ms.assetid: 3995405f-db4d-4f72-98dc-133a09f9cf65
title: Método IsNumericalPasswordValid de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsNumericalPasswordValid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0aed00554d7a8e284f83659dc92266b1ce5e098f1b102e6444bfc07fd2909066
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739645"
---
# <a name="isnumericalpasswordvalid-method-of-the-win32_encryptablevolume-class"></a>Método IsNumericalPasswordValid de la clase EncryptableVolume de Win32 \_

El **método IsNumericalPasswordValid** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica si la contraseña numérica cumple los requisitos de formato especiales para este valor de autenticación.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsNumericalPasswordValid(
  [in]  string  NumericalPassword,
  [out] boolean IsNumericalPasswordValid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NumericalPassword* \[ En\]
</dt> <dd>

Tipo: **cadena**

Cadena que especifica la contraseña numérica.

La contraseña numérica debe contener 48 dígitos. Estos dígitos se pueden dividir en 8 grupos de 6 dígitos, y el último dígito de cada grupo indica un valor de suma de comprobación para el grupo. Cada grupo de 6 dígitos debe ser divisible por 11 y debe ser menor que 720896. Suponiendo que un grupo de seis dígitos se etiqueta como x1, x2, x3, x4, x5 y x6, el dígito x6 de suma de comprobación se calcula como –x1+x2–x3+x4–x5 mod 11.

Opcionalmente, los grupos de dígitos se pueden separar mediante un espacio o guion. Por lo tanto, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" o "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" también pueden contener contraseñas numéricas válidas.

</dd> <dt>

*IsNumericalPasswordValid* \[ out\]
</dt> <dd>

Tipo: **booleano**

Valor booleano que es true si la contraseña numérica cumple los requisitos de formato especiales para este valor de autenticación; de lo contrario, el valor es false.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows aplicaciones de escritorio de Vista \[ Ultimate\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
