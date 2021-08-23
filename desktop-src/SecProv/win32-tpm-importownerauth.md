---
description: Importa la información de autorización del propietario de un TPM que ya es propiedad del registro del sistema operativo.
ms.assetid: 9611D363-6F10-48B9-B417-97133E975257
title: Win32_Tpm::ImportOwnerAuth (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ImportOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6e7d96a5cadf77e539d703ed95f428fa91535d49d1e7b5581300467782fce0af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004083"
---
# <a name="win32_tpmimportownerauth-method"></a>Método \_ Tpm::ImportOwnerAuth de Win32

Importa la información de autorización del propietario de un TPM que ya es propiedad del registro del sistema operativo. Esta operación validará primero si la información de autorización del propietario proporcionada es correcta. Si es correcto, el método importa esta información al Registro.

Solo los administradores locales pueden acceder a este método.

## <a name="syntax"></a>Sintaxis


```C++
uint32 ImportOwnerAuth(
  [in] STRING OwnerAuth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OwnerAuth* \[ En\]
</dt> <dd>

La información de autorización de propietario válida para el TPM.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de [TPM.](../tbs/tbs-return-codes.md)

A continuación se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método es especialmente útil en escenarios en los que el TPM está en un "estado listo con funcionalidad reducida" y requiere que la importación de la autorización del propietario esté totalmente lista o en escenarios de arranque dual en los que uno de los sistemas operativos posee el TPM y la información de autorización del propietario para TPM no está disponible en el otro sistema operativo.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                      |
| Espacio de nombres<br/>                | \\\\.\\ root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tpm de \_ Win32**](win32-tpm.md)
</dt> </dl>

 

 
