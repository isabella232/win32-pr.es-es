---
description: Recupera el identificador de seguridad y las marcas utilizadas para proteger una clave.
ms.assetid: 5EF97F44-78FF-4FBF-9142-F2DD0A849057
title: Método GetKeyProtectorAdSidInformation de la clase Win32_EncryptableVolume
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
ms.openlocfilehash: 57e72488a9e53f49383d179b0bcb1a8b9ff1f706
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "105691117"
---
# <a name="getkeyprotectoradsidinformation-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyProtectorAdSidInformation de la \_ clase EncryptableVolume de Win32

El método **GetKeyProtectorAdSidInformation** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) recupera el identificador de seguridad y las marcas utilizadas para proteger una clave.

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

*VolumeKeyProtectorID* \[ de\]
</dt> <dd>

Tipo: **String**

Identificador de cadena que se puede usar para administrar un protector de clave de volumen cifrado.

</dd> <dt>

*SidString* \[ enuncia\]
</dt> <dd>

Tipo: **String**

Cadena que contiene el identificador de seguridad (SID).

</dd> <dt>

*Marcas* \[ de enuncia\]
</dt> <dd>

Tipo: **UInt32**

Marcas que cambian el comportamiento de la función. Puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <dt>**FVE \_ Marca de DPAPI \_ ng \_ \_ ninguno**</dt> <dt>0x0000</dt> </dl>                                                                   | Ningún efecto.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <dt>**FVE \_ \_ \_ Desbloqueo de la marca de DPAPI ng \_ \_ como \_ \_ cuenta de servicio**</dt> <dt>0x0001</dt> </dl> | Especifica que el protector basado en SID se protegió en una cuenta de servicio. Si se especifica esta marca, el llamador debe asegurarse de que se ejecuta como la cuenta de servicio adecuada antes de llamar a [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (por ejemplo, mediante la eliminación temporal de la suplantación).<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

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

 

 
