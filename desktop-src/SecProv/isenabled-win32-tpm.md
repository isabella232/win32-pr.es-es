---
description: El método IsEnabled de la \_ clase Win32 TPM indica si el dispositivo está habilitado. Este valor se puede cambiar mediante los métodos enable y Disable.
ms.assetid: e1d5513f-33eb-49e3-9582-d6c103ca5d03
title: Método IsEnabled de la clase Win32_Tpm
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
ms.openlocfilehash: d808bb68e53b1a24ff668d1b7a9680b5d57b5e9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686642"
---
# <a name="isenabled-method-of-the-win32_tpm-class"></a>Método IsEnabled de la \_ clase Win32 TPM

El método **IsEnabled** de la clase [**Win32 \_ TPM**](win32-tpm.md) indica si el dispositivo está habilitado. Este valor se puede cambiar mediante los métodos [**enable**](enable-win32-tpm.md) y [**Disable**](disable-win32-tpm.md) .

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsEnabled(
  [out] boolean IsEnabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsEnabled* \[ enuncia\]
</dt> <dd>

Tipo: **booleano**

Si es **true**, el dispositivo está habilitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

A continuación se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Según la especificación de Trusted Computing Group (TCG) v 1.2, solo están disponibles los siguientes comandos cuando el dispositivo está en un estado desactivado.

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
</dt> <dt>

[**Disable**](disable-win32-tpm.md)
</dt> <dt>

[**Habilitar**](enable-win32-tpm.md)
</dt> </dl>

 

 
