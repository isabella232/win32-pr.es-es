---
description: El método IsActivated de la clase de Win32 \_ TPM indica si el dispositivo está activado.
ms.assetid: 862c386c-c5b5-44d2-89a5-3735b99bf8bc
title: Método IsActivated de la clase Win32_Tpm
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278230"
---
# <a name="isactivated-method-of-the-win32_tpm-class"></a>Método IsActivated de la \_ clase Win32 TPM

El método **IsActivated** de la clase de [**Win32 \_ TPM**](win32-tpm.md) indica si el dispositivo está activado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsActivated(
  [out] boolean IsActivated
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsActivated* \[ enuncia\]
</dt> <dd>

Tipo: **booleano**

Si es **true**, el dispositivo está activado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

A continuación se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

La desactivación es similar a deshabilitada, pero se pueden realizar cambios de estado operativo. Según la especificación de Trusted Computing Group (TCG) v 1.2, solo están disponibles los siguientes comandos cuando el dispositivo está en un estado desactivado.

-   ContinueSelfTest de TPM \_
-   DSAP de TPM \_
-   FlushSpecific de TPM \_
-   GetCapability de TPM \_
-   GetTestResult de TPM \_
-   \_Inicialización de TPM
-   OIAP de TPM \_
-   OSAP de TPM \_
-   OwnerSetDisable de TPM \_
-   \_Restablecimiento de PCR de TPM \_
-   PhysicalDisable de TPM \_
-   PhysicalEnable de TPM \_
-   PhysicalSetDeactivated de TPM \_
-   Restablecimiento de TPM \_
-   \_Savesta TPM
-   SelfTestFull de TPM \_
-   SetCapability de TPM \_
-   SHA1Complete de TPM \_
-   SHA1Start de TPM \_
-   SHA1Update de TPM \_
-   Inicio de TPM \_
-   TakeOwnerShip de TPM \_
-   \_Identificador de finalización de TPM \_

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

 

 
