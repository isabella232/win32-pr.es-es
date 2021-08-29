---
description: Recupera el identificador de seguridad y las marcas que se usan para proteger una clave.
ms.assetid: 5EF97F44-78FF-4FBF-9142-F2DD0A849057
title: Método GetKeyProtectorAdSidInformation de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1bc401f310fec6711c694be49fa001798c6ff92e8083fa1d942c886770c424a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667965"
---
# <a name="getkeyprotectoradsidinformation-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyProtectorAdSidInformation de la clase EncryptableVolume de Win32 \_

El **método GetKeyProtectorAdSidInformation** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) recupera el identificador de seguridad y las marcas que se usan para proteger una clave.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] string SidString,
  [out] uint32 Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ En\]
</dt> <dd>

Tipo: **cadena**

Identificador de cadena que se puede usar para administrar un protector de clave de volumen cifrado.

</dd> <dt>

*SidString* \[ out\]
</dt> <dd>

Tipo: **cadena**

Cadena que contiene el identificador de seguridad (SID).

</dd> <dt>

*Marcas* \[ out\]
</dt> <dd>

Tipo: **uint32**

Marcas que cambian el comportamiento de la función. Puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <dt>**FVE \_ DPAPI \_ NG \_ FLAG \_ NONE**</dt> <dt>0x0000</dt> </dl>                                                                   | Ningún efecto.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <dt>**FVE \_ DPAPI \_ NG \_ FLAG UNLOCK AS SERVICE ACCOUNT \_ \_ \_ \_ 0x0001**</dt> <dt></dt> </dl> | Especifica que el protector basado en SID se protegió en una cuenta de servicio. Si se especifica esta marca, el autor de la llamada debe asegurarse de que se ejecuta como la cuenta de servicio adecuada antes de llamar a [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (quitando temporalmente la suplantación, por ejemplo).<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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

 

 
