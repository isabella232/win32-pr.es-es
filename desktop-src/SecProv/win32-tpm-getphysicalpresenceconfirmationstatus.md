---
description: Indica si se requiere la confirmación de un usuario presente físicamente para una operación de presencia física determinada.
ms.assetid: 1CE558B7-EB6F-42CB-B52B-2A0101E90BD5
title: 'Win32_Tpm:: GetPhysicalPresenceConfirmationStatus (método)'
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
ms.openlocfilehash: 61dc2798973a82cfc75c803f2bf8307c8a43b3c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002336"
---
# <a name="win32_tpmgetphysicalpresenceconfirmationstatus-method"></a>Win32 \_ TPM:: GetPhysicalPresenceConfirmationStatus (método)

Indica si se requiere la confirmación de un usuario presente físicamente para una operación de presencia física determinada.

Este método solo es accesible para los administradores locales.

## <a name="syntax"></a>Sintaxis


```C++
uint32 GetPhysicalPresenceConfirmationStatus(
  [in]  uint32 Operation,
  [out] uint32 ConfirmationStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Operación* \[ de de\]
</dt> <dd>

Valor entero que especifica la operación de TPM solicitada que requiere presencia física. También se admiten comandos específicos del proveedor.

El parámetro de *operación* puede constar de los siguientes valores.



| Value                                                                                                                               | Significado                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>1</dt> </dl>                                                        | Habilitar<br/>                                        |
| <dl> <dt>2</dt> </dl>                                                        | Disable<br/>                                       |
| <dl> <dt>3</dt> </dl>                                                        | Activar<br/>                                      |
| <dl> <dt>4</dt> </dl>                                                        | Desactivación<br/>                                    |
| <dl> <dt>5</dt> </dl>                                                        | Borrar<br/>                                         |
| <dl> <dt>6</dt> </dl>                                                        | Habilitar + activar<br/>                             |
| <dl> <dt>7</dt> </dl>                                                        | Desactivación y deshabilitación<br/>                          |
| <dl> <dt>8</dt> </dl>                                                        | SetOwnerInstall \_ true<br/>                         |
| <dl> <dt>9</dt> </dl>                                                        | SetOwnerInstall \_ false<br/>                        |
| <dl> <dt>10</dt> </dl>                                                       | Habilitar + Activar + SetOwnerInstall \_ true<br/>     |
| <dl> <dt>11</dt> </dl>                                                       | SetOwnerInstall \_ false + desactivar + deshabilitar<br/> |
| <dl> <dt></dt><dt>12</dt> </dl> | PresenceunownedFieldUpgrade físico diferida<br/> |
| <dl> <dt></dt><dt>14</dt> </dl> | Clear + enable + Activate<br/>                     |
| <dl> <dt>15</dt> </dl>                                                       | SetNoPPIProvision \_ false<br/>                      |
| <dl> <dt>16</dt> </dl>                                                       | SetNoPPIProvision \_ true<br/>                       |
| <dl> <dt>17</dt> </dl>                                                       | SetNoPPIClear \_ false<br/>                          |
| <dl> <dt>18</dt> </dl>                                                       | SetNoPPIClear \_ true<br/>                           |
| <dl> <dt>19</dt> </dl>                                                       | SetNoPPIMaintenance \_ false<br/>                    |
| <dl> <dt>20</dt> </dl>                                                       | SetNoPPIMaintenance \_ true<br/>                     |
| <dl> <dt>21</dt> </dl>                                                       | Habilitar + Activar + borrar<br/>                     |
| <dl> <dt>22</dt> </dl>                                                       | Habilitar + Activar + desactivar + habilitar + activar<br/> |



 

</dd> <dt>

*ConfirmationStatus* \[ enuncia\]
</dt> <dd>

Devuelve el estado de confirmación para el comando de presencia física.

El parámetro *ConfirmationStatus* puede constar de los siguientes valores.



| Value                                                                        | Significado                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | No implementado<br/>                                             |
| <dl> <dt>1</dt> </dl> | Solo BIOS.<br/>                                                  |
| <dl> <dt>2</dt> </dl> | Bloqueada para el sistema operativo mediante la configuración del BIOS.<br/> |
| <dl> <dt>3</dt> </dl> | Permitido y presente físicamente el usuario requerido.<br/>               |
| <dl> <dt>4</dt> </dl> | No se requiere el usuario presente y presente físicamente<br/>            |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se pueden devolver todos los errores de TPM, así como los errores específicos de los [servicios base de TPM](../tbs/tbs-return-codes.md) .

A continuación se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                      |
| Espacio de nombres<br/>                | \\\\.\\ \\MicrosoftTpm de \\ seguridad de cimv2 raíz \\<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ TPM. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TPM de Win32 \_**](win32-tpm.md)
</dt> </dl>

 

 
