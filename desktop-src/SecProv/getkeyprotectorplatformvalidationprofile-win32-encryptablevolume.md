---
description: Recupera el perfil de validación de plataforma para un protector de clave determinado del tipo adecuado.
ms.assetid: 45fa6ba7-169c-4753-8586-0029a7650acc
title: Método GetKeyProtectorPlatformValidationProfile de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorPlatformValidationProfile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b9b951d3ce9eab52687730831f7052942fcbec93
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270783"
---
# <a name="getkeyprotectorplatformvalidationprofile-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyProtectorPlatformValidationProfile de la clase EncryptableVolume de Win32 \_

El **método GetKeyProtectorPlatformValidationProfile** recupera el perfil de validación de la plataforma para un protector de clave determinado del tipo adecuado.

El identificador del protector de clave debe hacer referencia a un protector de clave de tipo "TPM", "TPM y PIN", "TPM y PIN y clave de inicio" o "TPM y clave de inicio".

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetKeyProtectorPlatformValidationProfile(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PlatformValidationProfile[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ En\]
</dt> <dd>

Tipo: **cadena**

Identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.

</dd> <dt>

*PlatformValidationProfile* \[ out\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Matriz de enteros que especifica cómo el hardware de seguridad Módulo de plataforma segura (TPM) del equipo protege la clave de cifrado del volumen de disco.



| Value                                                                         | Significado                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Raíz principal de confianza de las extensiones de medida (CRTM), BIOS y plataforma<br/> |
| <dl> <dt>1</dt> </dl>  | Configuración y datos de plataforma y placa base<br/>                         |
| <dl> <dt>2</dt> </dl>  | Código ROM de opción<br/>                                                         |
| <dl> <dt>3</dt> </dl>  | Configuración y datos de ROM de opción<br/>                                       |
| <dl> <dt>4</dt> </dl>  | Código de registro de arranque maestro (MBR)<br/>                                           |
| <dl> <dt>5</dt> </dl>  | Tabla de particiones de registro de arranque maestro (MBR)<br/>                                |
| <dl> <dt>6</dt> </dl>  | Eventos de transición y reactivación de estado<br/>                                        |
| <dl> <dt>7</dt> </dl>  | Equipo Manufacturer-Specific<br/>                                          |
| <dl> <dt>8</dt> </dl>  | Sector de arranque NTFS<br/>                                                        |
| <dl> <dt>9</dt> </dl>  | Bloque de arranque NTFS<br/>                                                         |
| <dl> <dt>10</dt> </dl> | Administrador de arranque<br/>                                                            |
| <dl> <dt>11</dt> </dl> | BitLocker Access Control<br/>                                                |
| <dl> <dt>12</dt> </dl> | Definido para su uso por el sistema operativo estático<br/>                          |
| <dl> <dt>13</dt> </dl> | Definido para su uso por el sistema operativo estático<br/>                          |
| <dl> <dt>14</dt> </dl> | Definido para su uso por el sistema operativo estático<br/>                          |
| <dl> <dt>15</dt> </dl> | Definido para su uso por el sistema operativo estático<br/>                          |
| <dl> <dt>16</dt> </dl> | Se usa para la depuración<br/>                                                      |
| <dl> <dt>17</dt> </dl> | CRTM dinámico<br/>                                                            |
| <dl> <dt>18</dt> </dl> | Plataforma definida<br/>                                                        |
| <dl> <dt>19</dt> </dl> | Usado por un sistema operativo de confianza<br/>                                      |
| <dl> <dt>20</dt> </dl> | Usado por un sistema operativo de confianza<br/>                                      |
| <dl> <dt>21</dt> </dl> | Usado por un sistema operativo de confianza<br/>                                      |
| <dl> <dt>22</dt> </dl> | Usado por un sistema operativo de confianza<br/>                                      |
| <dl> <dt>23</dt> </dl> | Compatibilidad con aplicaciones<br/>                                                     |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                  | Descripción                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                  | Método realizado correctamente.<br/>                                                                                                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | El *parámetro VolumeKeyProtectorID* no hace referencia a un protector de clave del tipo "TPM", "TPM y PIN", "TPM y PIN y clave de inicio" o "TPM y clave de inicio".<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker.<br/>                                                                                  |



 

## <a name="remarks"></a>Observaciones

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista \[ Ultimate\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
