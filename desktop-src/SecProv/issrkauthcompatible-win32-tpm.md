---
description: El método IsSrkAuthCompatible de la clase Tpm de Win32 indica si la autorización de clave raíz de Storage (SRK) es compatible con el valor \_ esperado por Windows Vista.
ms.assetid: ce6d05b8-673a-40ab-a1d7-3fedfd099306
title: Método IsSrkAuthCompatible de la Win32_Tpm clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsSrkAuthCompatible
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: f5250f8d3f9ad38f9d4c46350e06e0fe32f756dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473429"
---
# <a name="issrkauthcompatible-method-of-the-win32_tpm-class"></a>Método IsSrkAuthCompatible de la clase Tpm de \_ Win32

El **método IsSrkAuthCompatible** de la clase Tpm de [**Win32 \_**](win32-tpm.md) indica si la autorización de clave raíz de Storage (SRK) es compatible con el valor esperado por Windows Vista.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsSrkAuthCompatible(
  [out] boolean IsSrkAuthCompatible
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsSrkAuthCompatible* \[ out\]
</dt> <dd>

Tipo: **booleano**

Si **es true,** el valor de autorización de SRK tiene un valor de cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

A continuación se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Managed Object Format (MOF) contienen las definiciones de las clases Windows Management Instrumentation (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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

 

 
