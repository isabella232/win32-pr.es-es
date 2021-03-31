---
description: El método IsSrkAuthCompatible de la clase de Win32 \_ TPM indica si la autorización de la clave raíz de almacenamiento (SRK) es compatible con el valor esperado por Windows Vista.
ms.assetid: ce6d05b8-673a-40ab-a1d7-3fedfd099306
title: Método IsSrkAuthCompatible de la clase Win32_Tpm
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911574"
---
# <a name="issrkauthcompatible-method-of-the-win32_tpm-class"></a>Método IsSrkAuthCompatible de la \_ clase Win32 TPM

El método **IsSrkAuthCompatible** de la clase de [**Win32 \_ TPM**](win32-tpm.md) indica si la autorización de la clave raíz de almacenamiento (SRK) es compatible con el valor esperado por Windows Vista.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsSrkAuthCompatible(
  [out] boolean IsSrkAuthCompatible
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsSrkAuthCompatible* \[ enuncia\]
</dt> <dd>

Tipo: **booleano**

Si **es true**, el valor de autorización de la SRK tiene un valor de cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

A continuación se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

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
</dt> </dl>

 

 
