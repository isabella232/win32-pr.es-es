---
description: Indica si se requiere la confirmación de un usuario físicamente presente para una operación de presencia física determinada.
ms.assetid: 1CE558B7-EB6F-42CB-B52B-2A0101E90BD5
title: Win32_Tpm::GetPhysicalPresenceConfirmationStatus (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceConfirmationStatus
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8e48fc7506b6b8ba8218d23bdeba75e960f2e3beca68c3d0a95b2aa4ea3c05e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890870"
---
# <a name="win32_tpmgetphysicalpresenceconfirmationstatus-method"></a>Método \_ Tpm::GetPhysicalPresenceConfirmationStatus de Win32

Indica si se requiere la confirmación de un usuario físicamente presente para una operación de presencia física determinada.

Los administradores locales solo pueden acceder a este método.

## <a name="syntax"></a>Sintaxis


```C++
uint32 GetPhysicalPresenceConfirmationStatus(
  [in]  uint32 Operation,
  [out] uint32 ConfirmationStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Operación* \[ En\]
</dt> <dd>

Valor entero que especifica la operación de TPM solicitada que requiere presencia física. También se admiten comandos específicos del proveedor.

El *parámetro Operation* puede constar de los siguientes valores.



| Valor                                                                                                                               | Significado                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>1</dt> </dl>                                                        | Habilitar<br/>                                        |
| <dl> <dt>2</dt> </dl>                                                        | Deshabilitar<br/>                                       |
| <dl> <dt>3</dt> </dl>                                                        | Activar<br/>                                      |
| <dl> <dt>4</dt> </dl>                                                        | Desactivación<br/>                                    |
| <dl> <dt>5</dt> </dl>                                                        | Borrar<br/>                                         |
| <dl> <dt>6</dt> </dl>                                                        | Habilitar y activar<br/>                             |
| <dl> <dt>7</dt> </dl>                                                        | Desactivar y deshabilitar<br/>                          |
| <dl> <dt>8</dt> </dl>                                                        | SetOwnerInstall \_ True<br/>                         |
| <dl> <dt>9</dt> </dl>                                                        | SetOwnerInstall \_ False<br/>                        |
| <dl> <dt>10</dt> </dl>                                                       | Habilitar + Activar + SetOwnerInstall \_ True<br/>     |
| <dl> <dt>11</dt> </dl>                                                       | SetOwnerInstall \_ False + Desactivar + Deshabilitar<br/> |
| <dl> <dt></dt><dt>12</dt> </dl> | Presencia física diferidaacownedFieldUpgrade<br/> |
| <dl> <dt></dt><dt>14</dt> </dl> | Borrar + Habilitar + Activar<br/>                     |
| <dl> <dt>15</dt> </dl>                                                       | SetNo PPPProvision \_ False<br/>                      |
| <dl> <dt>16</dt> </dl>                                                       | SetNo PPPProvision \_ True<br/>                       |
| <dl> <dt>17</dt> </dl>                                                       | SetNo PPPClear \_ False<br/>                          |
| <dl> <dt>18</dt> </dl>                                                       | SetNo PPPClear \_ True<br/>                           |
| <dl> <dt>19</dt> </dl>                                                       | SetNo PPPMaintenance \_ False<br/>                    |
| <dl> <dt>20</dt> </dl>                                                       | SetNo PPPMaintenance \_ True<br/>                     |
| <dl> <dt>21</dt> </dl>                                                       | Habilitar + Activar + Borrar<br/>                     |
| <dl> <dt>22</dt> </dl>                                                       | Habilitar + Activar + Borrar + Habilitar + Activar<br/> |



 

</dd> <dt>

*ConfirmationStatus* \[ out\]
</dt> <dd>

Devuelve el estado de confirmación del comando de presencia física.

El *parámetro ConfirmationStatus* puede constar de los siguientes valores.



| Valor                                                                        | Significado                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | No implementado<br/>                                             |
| <dl> <dt>1</dt> </dl> | Solo BIOS.<br/>                                                  |
| <dl> <dt>2</dt> </dl> | Bloqueado para el sistema operativo por la configuración del BIOS.<br/> |
| <dl> <dt>3</dt> </dl> | Usuario permitido y físicamente presente requerido.<br/>               |
| <dl> <dt>4</dt> </dl> | Usuario permitido y físicamente presente no requerido<br/>            |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de [TPM.](../tbs/tbs-return-codes.md)

A continuación se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                      |
| Espacio de nombres<br/>                | \\\\.\\ root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Tpm de \_ Win32**](win32-tpm.md)
</dt> </dl>

 

 
