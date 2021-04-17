---
description: Protege la clave de cifrado del volumen mediante un identificador de seguridad Active Directory (SID).
ms.assetid: 881EEAF2-49C5-4BBD-B2AA-5E30B61E7D3A
title: Método ProtectKeyWithAdSid de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0279a6edc8aaa275fdf75a855452d987de802d86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688015"
---
# <a name="protectkeywithadsid-method-of-the-win32_encryptablevolume-class"></a>Método ProtectKeyWithAdSid de la \_ clase EncryptableVolume de Win32

El método **ProtectKeyWithAdSid** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) protege la clave de cifrado del volumen mediante el uso de un identificador de seguridad Active Directory (SID).

## <a name="syntax"></a>Sintaxis


```mof
uint32 ProtectKeyWithAdSid(
  [in, optional] string FriendlyName,
  [in]           string SidString,
  [in]           uint32 Flags,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FriendlyName* \[ en, opcional\]
</dt> <dd>

Cadena que especifica un identificador asignado por el usuario para este protector de clave. Si no se especifica este parámetro, se utiliza un valor en blanco.

</dd> <dt>

*SidString* \[ de\]
</dt> <dd>

Cadena que contiene la Active Directory SID usada para proteger la clave de cifrado.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Marcas que cambian el comportamiento de la función. Puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <dt>**FVE \_ Marca de DPAPI \_ ng \_ \_ ninguno**</dt> <dt>0x0000</dt> </dl>                                                                   | Ningún efecto.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <dt>**FVE \_ \_ \_ Desbloqueo de la marca de DPAPI ng \_ \_ como \_ \_ cuenta de servicio**</dt> <dt>0x0001</dt> </dl> | Especifica que el protector basado en SID se protegió en una cuenta de servicio. Si se especifica esta marca, el llamador debe asegurarse de que se ejecuta como la cuenta de servicio adecuada antes de llamar a [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (por ejemplo, mediante la eliminación temporal de la suplantación).<br/> |



 

</dd> <dt>

*VolumeKeyProtectorID* \[ enuncia\]
</dt> <dd>

Un identificador único asociado al protector creado. Puede usar esta cadena para administrar el protector de clave.

Si la unidad admite el cifrado de hardware y BitLocker no ha tomado propiedad de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos de cada banda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md)

De forma predeterminada, no se puede Agregar una cuenta de Active Directory o un protector de grupo de forma remota. Debe habilitar la delegación restringida en el controlador de dominio y el equipo de origen. En el controlador de dominio, realice los pasos siguientes:

1.  Abrir Administrador de servidores
2.  Seleccionar equipos en roles de Active Directory
3.  Seleccione el equipo cliente de destino y haga clic con el botón secundario en
4.  Seleccione la pestaña delegación
5.  Seleccione el botón de radio "confiar en este equipo para la delegación solo a los servicios especificados"
6.  Seleccione el botón de radio "usar solo Kerberos"
7.  Haga clic en Agregar
8.  Selección de "usuarios o equipos"
9.  Seleccionar host/como el nombre de entidad de seguridad de servicio

Realice los pasos del 3 al 9 en el equipo de origen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones Windows 8 Enterprise, Windows 8 Pro \[ Desktop\]<br/>                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
