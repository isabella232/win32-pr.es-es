---
description: Protege la clave de cifrado del volumen mediante un Active Directory de seguridad (SID).
ms.assetid: 881EEAF2-49C5-4BBD-B2AA-5E30B61E7D3A
title: Método ProtectKeyWithAdSid de la Win32_EncryptableVolume clase
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
ms.openlocfilehash: f8df8a0ff0bdbf827d4a0deff07ada13e50459a8a4b87f7ab388b01d95892961
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867555"
---
# <a name="protectkeywithadsid-method-of-the-win32_encryptablevolume-class"></a>Método ProtectKeyWithAdSid de la clase EncryptableVolume de Win32 \_

El **método ProtectKeyWithAdSid** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) protege la clave de cifrado del volumen mediante un Active Directory de seguridad (SID).

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

*FriendlyName* \[ in, opcional\]
</dt> <dd>

Cadena que especifica un identificador asignado por el usuario para este protector de clave. Si no se especifica este parámetro, se usa un valor en blanco.

</dd> <dt>

*SidString* \[ En\]
</dt> <dd>

Cadena que contiene el Active Directory sid usado para proteger la clave de cifrado.

</dd> <dt>

*Marcas* \[ En\]
</dt> <dd>

Marcas que cambian el comportamiento de la función. Puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <dt>**FVE \_ DPAPI \_ NG \_ FLAG \_ NONE**</dt> <dt>0x0000</dt> </dl>                                                                   | Ningún efecto.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <dt>**FVE \_ DESBLOQUEO DE \_ LA MARCA DE DPAPI NG \_ COMO CUENTA \_ \_ \_ \_ DE**</dt> <dt>SERVICIO 0x0001</dt> </dl> | Especifica que el protector basado en SID se protegió en una cuenta de servicio. Si se especifica esta marca, el autor de la llamada debe asegurarse de que se ejecuta como la cuenta de servicio adecuada antes de llamar a [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (quitando temporalmente la suplantación, por ejemplo).<br/> |



 

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Identificador único asociado al protector creado. Puede usar esta cadena para administrar el protector de clave.

Si la unidad admite el cifrado de hardware y BitLocker no ha tomado posesión de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos por banda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md)

De forma predeterminada, no puede agregar una cuenta Active Directory o protector de grupo de forma remota. Debe habilitar la delegación restringida en el controlador de dominio y el equipo de origen. En el controlador de dominio, realice los pasos siguientes:

1.  Abrir Administrador de servidores
2.  Selección de equipos en Active Directory roles
3.  Seleccione el equipo cliente de destino y haga clic con el botón derecho.
4.  Seleccione la pestaña Delegación.
5.  Seleccione el botón de radio "Confiar en este equipo para la delegación solo en servicios especificados".
6.  Seleccione el botón de radio "Usar solo Kerberos"
7.  Haga clic en Agregar
8.  Seleccione "Usuarios o equipos".
9.  Seleccione host/ como nombre de entidad de seguridad de servicio.

Realice los pasos del 3 al 9 en el equipo de origen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8 Enterprise, Windows 8 Pro solo aplicaciones \[ de escritorio\]<br/>                                    |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
