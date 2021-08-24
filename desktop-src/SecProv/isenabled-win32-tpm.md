---
description: El método IsEnabled de la clase Tpm de Win32 \_ indica si el dispositivo está habilitado. Los métodos Enable y Disable pueden cambiar este valor.
ms.assetid: e1d5513f-33eb-49e3-9582-d6c103ca5d03
title: Método IsEnabled de la Win32_Tpm clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 1d61c96d9c80ae77f9869261905fb93461530b452deaf7a4709b394623a3dfab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667505"
---
# <a name="isenabled-method-of-the-win32_tpm-class"></a>Método IsEnabled de la clase Tpm de \_ Win32

El **método IsEnabled** de la [**clase \_ Tpm de Win32**](win32-tpm.md) indica si el dispositivo está habilitado. Los métodos [**Enable**](enable-win32-tpm.md) y [**Disable**](disable-win32-tpm.md) pueden cambiar este valor.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsEnabled(
  [out] boolean IsEnabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsEnabled* \[ out\]
</dt> <dd>

Tipo: **booleano**

Si **es true,** el dispositivo está habilitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

A continuación se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Según la especificación Trusted Computing Group (TCG) v1.2, solo están disponibles los siguientes comandos cuando el dispositivo está en estado desactivado.

-   TPM \_ ContinueSelfTest
-   TPM \_ DSAP
-   TPM \_ FlushSpecific
-   TPM \_ GetCapability
-   TPM \_ GetTestResult
-   Inicialización de TPM \_
-   TPM \_ OIAP
-   TPM \_ OSAP
-   TPM \_ OwnerSetDisable
-   Restablecimiento \_ de PCR de TPM \_
-   TPM \_ PhysicalDisable
-   Tpm \_ físicoEnable
-   TPM \_ PhysicalSetDeactivated
-   Restablecimiento \_ de TPM
-   TPM \_ SaveState
-   TPM \_ SelfTestFull
-   TPM \_ SetCapability
-   TPM \_ SHA1Complete
-   TPM \_ SHA1Start
-   TPM \_ SHA1Update
-   Inicio de TPM \_
-   TPM \_ TakeOwnership
-   Controlador de \_ terminación de TPM \_

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
</dt> <dt>

[**Deshabilitar**](disable-win32-tpm.md)
</dt> <dt>

[**Habilitar**](enable-win32-tpm.md)
</dt> </dl>

 

 
