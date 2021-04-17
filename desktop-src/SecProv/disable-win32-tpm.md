---
description: Permite al propietario del TPM deshabilitar o suspender TPM.
ms.assetid: d910334d-6da6-423d-ae8d-6e86f300dd52
title: Método Disable de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Disable
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 32012c338646ce11c96d2657233642808fdcdaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686660"
---
# <a name="disable-method-of-the-win32_tpm-class"></a>Método Disable de la \_ clase TPM de Win32

El método **Disable** de la clase [**Win32 \_ TPM**](win32-tpm.md) permite que el propietario del TPM deshabilite o suspenda el TPM. Este método suspende BitLocker si la llamada puede hacer que se requiera la recuperación de BitLocker. BitLocker se reanudará automáticamente una vez que se haya aprovisionado TPM.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Disable(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OwnerAuth* \[ en, opcional\]
</dt> <dd>

Tipo: **String**

Cadena que identifica el propietario del TPM. Esta cadena debe ser una cadena codificada en Base64 que contenga exactamente 20 bytes de datos binarios. Use el método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una frase de contraseña a este formato esperado. Si no se proporciona ninguno, se lee el parámetro *OwnerAuth* en el registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                                                         | Descripción                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                         | Método realizado correctamente.<br/>                                                                                                                                                |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>              | El valor de autorización de propietario proporcionado no puede realizar la solicitud.<br/>                                                                                                        |
| <dl> <dt>**TPM \_ E \_ defender \_ LOCK \_ Running**</dt> <dt>2150107139 (0x80280803)</dt> </dl> | El TPM defiende contra los ataques de diccionario y se encuentra en un período de tiempo de espera. Para obtener más información, vea el método [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .<br/> |



 

## <a name="remarks"></a>Observaciones

Para deshabilitar TPM sin tener el valor de autorización de propietario del TPM, use el método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .

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

 

 
