---
description: El método IsActivated de la clase Tpm de Win32 \_ indica si el dispositivo está activado.
ms.assetid: 862c386c-c5b5-44d2-89a5-3735b99bf8bc
title: Método IsActivated de la Win32_Tpm clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsActivated
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6482163a27f211b4f4ce24284a8339f2b7254f3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270716"
---
# <a name="isactivated-method-of-the-win32_tpm-class"></a>Método IsActivated de la clase Tpm de \_ Win32

El **método IsActivated** de la [**clase \_ Tpm de Win32**](win32-tpm.md) indica si el dispositivo está activado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsActivated(
  [out] boolean IsActivated
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsActivated* \[ out\]
</dt> <dd>

Tipo: **booleano**

Si **es true,** se activa el dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

A continuación se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

La desactivación es similar a deshabilitada, pero es posible realizar cambios de estado operativo. Según la especificación Trusted Computing Group (TCG) v1.2, solo están disponibles los siguientes comandos cuando el dispositivo está en estado desactivado.

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



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                      |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Tpm de \_ Win32**](win32-tpm.md)
</dt> </dl>

 

 
