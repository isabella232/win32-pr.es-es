---
description: Crea un par de claves de aprobación de 2048 bits en el TPM.
ms.assetid: 393f0264-d1e9-4a08-bdaa-475b32d93e05
title: Método CreateEndorsementKeyPair de la Win32_Tpm clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.CreateEndorsementKeyPair
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 1df4cb87d88956d9066e8d0d00f56df50b2d18b33ae234f597bb028a2eee5322
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668075"
---
# <a name="createendorsementkeypair-method-of-the-win32_tpm-class"></a>Método CreateEndorsementKeyPair de la clase Tpm de \_ Win32

El **método CreateEndorsementKeyPair** de la clase [**\_ Tpm de Win32**](win32-tpm.md) crea un par de claves de aprobación de 2048 bits en el TPM. El par de claves de aprobación debe estar disponible para que [**el método TakeOwnership**](takeownership-win32-tpm.md) se ejecute correctamente. Puede usar el método [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md) para detectar si la clave de aprobación ya existe en el TPM.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CreateEndorsementKeyPair();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                                                  | Descripción                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                  | Método realizado correctamente.<br/>                          |
| <dl> <dt> **TPM \_ E DISABLED \_ \_ CMD**</dt> <dt>2150105096 (0x80280008)</dt> </dl> | Ya existe un par de claves de aprobación en este TPM.<br/> |



 

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

 

 
