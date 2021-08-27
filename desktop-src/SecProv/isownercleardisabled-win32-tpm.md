---
description: El método IsOwnerClearDisabled de la clase Tpm de Win32 indica si el propietario del dispositivo tiene restringido borrar \_ el dispositivo.
ms.assetid: 04f98e9b-c1a0-4828-b7cb-67b32d7470ea
title: Método IsOwnerClearDisabled de la Win32_Tpm clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnerClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 639804b21c97a6e445c0eddc9253c46774a4ccd895d58bfe32289432702cbe03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080635"
---
# <a name="isownercleardisabled-method-of-the-win32_tpm-class"></a>Método IsOwnerClearDisabled de la clase Tpm win32 \_

El **método IsOwnerClearDisabled** de la clase [**\_ Tpm de Win32**](win32-tpm.md) indica si el propietario del dispositivo tiene restringido borrar el dispositivo.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsOwnerClearDisabled(
  [out] boolean IsOwnerClearDisabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsOwnerClearDisabled* \[ out\]
</dt> <dd>

Tipo: **booleano**

Si **es true,** el propietario del dispositivo no puede borrar el dispositivo. Solo un usuario físicamente presente puede borrar el dispositivo. Si **es false,** el propietario del dispositivo puede borrar el dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

A continuación se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 
