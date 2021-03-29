---
description: Crea un par de claves de aprobación de 2048 bits en el TPM.
ms.assetid: 393f0264-d1e9-4a08-bdaa-475b32d93e05
title: Método CreateEndorsementKeyPair de la clase Win32_Tpm
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
ms.openlocfilehash: 5839dc009d8af420a91f2e7c925f2cac5567d2a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540947"
---
# <a name="createendorsementkeypair-method-of-the-win32_tpm-class"></a>Método CreateEndorsementKeyPair de la \_ clase Win32 TPM

El método **CreateEndorsementKeyPair** de la clase [**Win32 \_ TPM**](win32-tpm.md) crea un par de claves de aprobación de 2048 bits en el TPM. El par de claves de aprobación debe estar disponible para que el método [**TakeOwnerShip**](takeownership-win32-tpm.md) se ejecute correctamente. Puede usar el método [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md) para detectar si la clave de aprobación ya existe en el TPM.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CreateEndorsementKeyPair();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                                                  | Descripción                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                  | Método realizado correctamente.<br/>                          |
| <dl> <dt> **TPM \_ E \_ deshabilitado \_ cmd**</dt> <dt>2150105096 (0x80280008)</dt> </dl> | Ya existe un par de claves de aprobación en este TPM.<br/> |



 

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

 

 
