---
description: Indica si está habilitado el aprovisionamiento automático del TPM.
ms.assetid: C908673C-8BDB-4541-85C6-65FED1EBB535
title: 'Win32_Tpm:: IsAutoProvisioningEnabled (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsAutoProvisioningEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: cb269247292646464c6126a2588a50d77b19db9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911565"
---
# <a name="win32_tpmisautoprovisioningenabled-method"></a>Win32 \_ TPM:: IsAutoProvisioningEnabled (método)

Indica si está habilitado el aprovisionamiento automático del TPM. De forma predeterminada, el aprovisionamiento automático está habilitado para Windows 8 y Windows Server 2012.

Este método solo es accesible para los administradores locales.

## <a name="syntax"></a>Sintaxis


```C++
uint32 IsAutoProvisioningEnabled(
  [out] BOOL IsAutoProvisioningEnabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsAutoProvisioningEnabled* \[ enuncia\]
</dt> <dd>

Establézcalo en **true** si está habilitado el aprovisionamiento automático de TPM.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se pueden devolver todos los errores de TPM, así como los errores específicos de los [servicios base de TPM](../tbs/tbs-return-codes.md) .

A continuación se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                      |
| Espacio de nombres<br/>                | \\\\.\\ \\MicrosoftTpm de \\ seguridad de cimv2 raíz \\<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ TPM. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TPM de Win32 \_**](win32-tpm.md)
</dt> </dl>

 

 
