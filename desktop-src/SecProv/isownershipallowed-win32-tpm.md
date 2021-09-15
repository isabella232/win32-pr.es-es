---
description: El método IsOwnershipAllowed de la clase Tpm de Win32 indica si se permite la capacidad de instalar un \_ propietario para el dispositivo.
ms.assetid: dfeb5afe-4169-470b-b5e4-cf1e5781271e
title: Método IsOwnershipAllowed de la Win32_Tpm clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnershipAllowed
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c818d5a4e4eb16ac637372f0c7ed0f2e9211ef88
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270647"
---
# <a name="isownershipallowed-method-of-the-win32_tpm-class"></a>Método IsOwnershipAllowed de la clase Tpm \_ win32

El **método IsOwnershipAllowed** de la clase [**\_ Tpm de Win32**](win32-tpm.md) indica si se permite la capacidad de instalar un propietario para el dispositivo.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsOwnershipAllowed(
  [out] boolean IsOwnershipAllowed
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsOwnershipAllowed* \[ out\]
</dt> <dd>

Tipo: **booleano**

Si **es true**, se permite la capacidad de instalar un propietario para el dispositivo. Si **es false,** el [**método TakeOwnership**](takeownership-win32-tpm.md) no podrá instalar un propietario para el dispositivo.

Este valor se puede cambiar con el [**método SetPhysicalPresenceRequest.**](setphysicalpresencerequest-win32-tpm.md) El valor se restablece a **true después** de ejecutar el método [**Clear.**](clear-win32-tpm.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

A continuación se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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

 

 
