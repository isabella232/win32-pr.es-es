---
description: Habilita el aprovisionamiento automático del TPM si está deshabilitado actualmente.
ms.assetid: 70F56A4C-F936-4CB6-83F6-F3B691F43B98
title: Win32_Tpm::EnableAutoProvisioning (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.EnableAutoProvisioning
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 111073fc6f1a8c047182a33240c1cf1e7f3ed29260e9f7b1a390360dc6538c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891018"
---
# <a name="win32_tpmenableautoprovisioning-method"></a>Método \_ Tpm::EnableAutoProvisioning de Win32

Habilita el aprovisionamiento automático del TPM si está deshabilitado actualmente. La operación no tiene ningún efecto si el aprovisionamiento automático ya está habilitado. De forma predeterminada, el aprovisionamiento automático está habilitado para Windows 8 y Windows Server 2012.

Los administradores locales solo pueden acceder a este método.

## <a name="syntax"></a>Sintaxis


```C++
uint32 EnableAutoProvisioning();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de [TPM.](../tbs/tbs-return-codes.md)

A continuación se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                      |
| Espacio de nombres<br/>                | \\\\.\\ root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Tpm de \_ Win32**](win32-tpm.md)
</dt> </dl>

 

 
