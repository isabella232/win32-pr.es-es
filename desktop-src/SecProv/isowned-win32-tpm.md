---
description: El método IsOwned de la clase Tpm de Win32 \_ indica si el dispositivo tiene un propietario. El método TakeOwnership cambia este valor.
ms.assetid: 04a9394f-98de-43e3-8a19-7a8f409823b8
title: Método IsOwned de la Win32_Tpm clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwned
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 01686f9b93e4dd952ce42b43d58aed9684457fb9dedeb524cea8859e0f44ba4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797115"
---
# <a name="isowned-method-of-the-win32_tpm-class"></a>Método IsOwned de la clase Tpm \_ win32

El **método IsOwned** de la [**clase \_ Tpm win32**](win32-tpm.md) indica si el dispositivo tiene un propietario. El método [**TakeOwnership**](takeownership-win32-tpm.md) cambia este valor.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsOwned(
  [out] boolean IsOwned
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsOwned* \[ out\]
</dt> <dd>

Tipo: **booleano**

Si **es true,** el dispositivo tiene un propietario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

A continuación se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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

 

 
