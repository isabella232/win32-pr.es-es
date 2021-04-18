---
description: Indica la acción del usuario que se necesita para realizar la operación de presencia física del Módulo de plataforma segura (TPM). Use el método SetPhysicalPresenceRequest para solicitar una operación.
ms.assetid: abbd9702-c3a7-468a-bc83-2b7739d0b7bf
title: Método GetPhysicalPresenceTransition de la clase Win32_Tpm
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688152"
---
# <a name="getphysicalpresencetransition-method-of-the-win32_tpm-class"></a>Método GetPhysicalPresenceTransition de la \_ clase Win32 TPM

El método **GetPhysicalPresenceTransition** de la clase [**Win32 \_ TPM**](win32-tpm.md) indica la acción del usuario que se necesita para realizar la operación de presencia física del módulo de plataforma segura (TPM). Use el método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) para solicitar una operación. La acción del usuario requerida se establece para el equipo en el momento de la fabricación. Normalmente, es necesario reiniciar el equipo.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetPhysicalPresenceTransition(
  [out] uint32 Transition
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Transición* \[ enuncia\]
</dt> <dd>

Tipo: **UInt32**

Valor entero que especifica la transición necesaria para realizar una operación de presencia física de TPM.



| Value                                                                        | Significado                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | No se necesita ninguna acción del usuario para realizar una operación de presencia física de TPM.<br/>                                                                                                                                                                              |
| <dl> <dt>1</dt> </dl> | Para realizar una operación de presencia física de TPM, el usuario debe apagar el equipo y, a continuación, volver a encenderlo con el botón de encendido. El usuario debe estar presente físicamente en el equipo para aceptar o rechazar el cambio cuando se lo solicite el BIOS.<br/> |
| <dl> <dt>2</dt> </dl> | Para realizar una operación de presencia física de TPM, el usuario debe reiniciar el equipo con un reinicio en caliente. El usuario debe estar presente físicamente en el equipo para aceptar o rechazar el cambio cuando se lo solicite el BIOS.<br/>                              |
| <dl> <dt>3</dt> </dl> | Se desconoce la acción del usuario requerida.<br/>                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                                                      | Descripción                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                      | Método realizado correctamente.<br/>                                                            |
| <dl> <dt>**TPM \_ E \_ PPI \_ ACPI \_ error**</dt> <dt>2150171392 (0x80290300)</dt> </dl> | Error de hardware. Consulte al fabricante del equipo para obtener más información.<br/> |



 

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
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
