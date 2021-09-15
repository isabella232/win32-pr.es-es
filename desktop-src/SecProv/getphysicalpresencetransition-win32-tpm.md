---
description: Indica la acción del usuario necesaria para realizar la operación de Módulo de plataforma segura (TPM) física. Use el método SetPhysicalPresenceRequest para solicitar una operación.
ms.assetid: abbd9702-c3a7-468a-bc83-2b7739d0b7bf
title: Método GetPhysicalPresenceTransition de la Win32_Tpm clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceTransition
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 4e6a3ab2295cc26cd439465b569f594dd1e0580a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270727"
---
# <a name="getphysicalpresencetransition-method-of-the-win32_tpm-class"></a>Método GetPhysicalPresenceTransition de la clase Tpm de \_ Win32

El **método GetPhysicalPresenceTransition** de la clase [**\_ Tpm de Win32**](win32-tpm.md) indica la acción del usuario necesaria para realizar la operación de presencia física Módulo de plataforma segura (TPM). Use el [**método SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) para solicitar una operación. La acción de usuario necesaria se establece para el equipo en el momento de la fabricación. Normalmente se necesita reiniciar el equipo.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetPhysicalPresenceTransition(
  [out] uint32 Transition
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Transición* \[ out\]
</dt> <dd>

Tipo: **uint32**

Valor entero que especifica la transición necesaria para realizar una operación de presencia física de TPM.



| Value                                                                        | Significado                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | No se necesita ninguna acción del usuario para realizar una operación de presencia física de TPM.<br/>                                                                                                                                                                              |
| <dl> <dt>1</dt> </dl> | Para realizar una operación de presencia física de TPM, el usuario debe apagar el equipo y volver a encenderlo con el botón de encendido. El usuario debe estar físicamente presente en el equipo para aceptar o rechazar el cambio cuando lo solicite el BIOS.<br/> |
| <dl> <dt>2</dt> </dl> | Para realizar una operación de presencia física de TPM, el usuario debe reiniciar el equipo mediante un reinicio automático. El usuario debe estar físicamente presente en el equipo para aceptar o rechazar el cambio cuando lo solicite el BIOS.<br/>                              |
| <dl> <dt>3</dt> </dl> | Se desconoce la acción de usuario necesaria.<br/>                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                                                      | Descripción                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                      | Método realizado correctamente.<br/>                                                            |
| <dl> <dt>**TPM \_ E \_ PPP \_ ACPI \_ FAILURE**</dt> <dt>2150171392 (0x80290300)</dt> </dl> | Se produjo un error de hardware. Consulte al fabricante del equipo para obtener más información.<br/> |



 

## <a name="remarks"></a>Observaciones

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
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
