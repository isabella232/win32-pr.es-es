---
description: Devuelve los resultados de una operación de presencia física de TPM que se realizó.
ms.assetid: 28d76149-3905-45db-a41e-32fac1603582
title: Método GetPhysicalPresenceResponse de la Win32_Tpm clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceResponse
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5f32379c9e0f538c2f9be4466b55158d0abcdd51a4d2612634b2b03ff869ed41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891866"
---
# <a name="getphysicalpresenceresponse-method-of-the-win32_tpm-class"></a>Método GetPhysicalPresenceResponse de la clase Tpm de \_ Win32

El **método GetPhysicalPresenceResponse de** la clase [**\_ Tpm de Win32**](win32-tpm.md) devuelve los resultados de una operación de presencia física de TPM que se realizó. Use el [**método SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) para solicitar una operación.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetPhysicalPresenceResponse(
  [out] uint32 Request,
  [out] uint32 Response
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Solicitud* \[ out\]
</dt> <dd>

Tipo: **uint32**

Valor entero que especifica la operación de presencia física de TPM que se realizó.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt>0</dt> </dl></td>
<td>Sin solicitud.<br/> No se realizó ninguna operación de presencia física.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>1</dt> </dl></td>
<td>Habilite el TPM.<br/> Esta operación se invierte mediante la operación 2. <br/> Para obtener más información, vea estos métodos relacionados que no implican la presencia física:
<ul>
<li><a href="enable-win32-tpm.md"><strong>Habilitar</strong></a></li>
<li><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>2</dt> </dl></td>
<td>Deshabilite el TPM.<br/> Esta operación se invierte mediante la operación 1. <br/> Para obtener más información, vea este método relacionado que no implica presencia física: <a href="disable-win32-tpm.md"><strong>Deshabilitar</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>3</dt> </dl></td>
<td>Active el TPM.<br/> Esta operación se invierte mediante la operación 4.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>4</dt> </dl></td>
<td>Desactive el TPM.<br/> Esta operación se invierte mediante la operación 3.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>5</dt> </dl></td>
<td>Borre el TPM.<br/> Esta operación no se puede invertir. <br/> Para obtener más información, vea este método relacionado que no implica presencia física: <a href="clear-win32-tpm.md"><strong>Borrar</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>6</dt> </dl></td>
<td>Habilite y active el TPM.<br/> Esta operación se invierte mediante la operación 7.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>7</dt> </dl></td>
<td>Desactive y deshabilite el TPM.<br/> Esta operación se invierte mediante la operación 6. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>8</dt> </dl></td>
<td>Permitir la instalación de un propietario de TPM.<br/> Esta operación se invierte mediante la operación 9.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>9</dt> </dl></td>
<td>Impedir la instalación de un propietario de TPM.<br/> Esta operación se invierte mediante la operación 8. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>10</dt> </dl></td>
<td>Habilitar, activar y permitir la instalación de un propietario de TPM.<br/> Esta operación se invierte mediante la operación 11.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>11</dt> </dl></td>
<td>Desactive, deshabilite e impida la instalación de un propietario de TPM.<br/> Esta operación se invierte mediante la operación 10.<br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <dt><strong></strong></dt><dt>12</dt> </dl></td>
<td>Presencia física diferidaacodFieldUpgrade<br/> Se ha actualizado la configuración de presencia física.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>14</dt> </dl></td>
<td>Borre, habilite y active el TPM.<br/> Esta operación no se puede invertir.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>15</dt> </dl></td>
<td>SetNoPPIProvision_False<br/> Establece el aprovisionamiento que debe tener presencia física para establecer el TPM.<br/> Esta operación se invierte mediante la operación 16.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>16</dt> </dl></td>
<td>SetNoPPIProvision_True<br/> Establece el aprovisionamiento que no es necesario que esté físicamente presente para establecer el TPM.<br/> Esta operación se invierte mediante la operación 15.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>17</dt> </dl></td>
<td>SetNoPPIClear_False<br/> Establece el aprovisionamiento que debe tener presencia física para borrar el TPM.<br/> Esta operación se invierte mediante la operación 18.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>18</dt> </dl></td>
<td>SetNoPPIClear_True<br/> Establece el aprovisionamiento que no es necesario que esté físicamente presente para borrar el TPM.<br/> Esta operación se invierte mediante la operación 17.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>19</dt> </dl></td>
<td>SetNoPPIMaintenance_False<br/> Establece el aprovisionamiento que debe tener presencia física para mantener el TPM.<br/> Esta operación se invierte mediante la operación 20.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>20</dt> </dl></td>
<td>SetNoPPIMaintenance_True<br/> Establece el aprovisionamiento que debe tener presencia física para mantener el TPM.<br/> Esta operación se invierte mediante la operación 19.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>21</dt> </dl></td>
<td>Habilitar + Activar + Borrar<br/> Habilite, active y desactive el TPM.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>22</dt> </dl></td>
<td>Habilitar + Activar + Borrar + Habilitar + Activar<br/> Habilite, active y desactive el TPM y, a continuación, habilite y reactive el TPM.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:</strong> Este valor no se admite.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*Respuesta* \[ out\]
</dt> <dd>

Tipo: **uint32**

Valor entero que especifica los resultados de realizar la operación de presencia física de TPM.

Una operación de presencia física es correcta si un usuario físicamente presente confirma la operación y si la operación se ejecuta sin errores.

Este valor puede contener cualquier error de TPM. En la tabla siguiente se enumeran algunas de las respuestas de error comunes.



| Valor                                                                                                                                                                                                                                                                    | Significado                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                                                                                                                                                                                             | La operación de TPM solicitada se ha realizado correctamente.<br/>              |
| <span id="TPM_E_PPI_USER_ABORT"></span><span id="tpm_e_ppi_user_abort"></span><dl> <dt>**TPM \_ E \_ PPP USER \_ \_ ABORT**</dt> <dt>2150171393 (0x80290301)</dt> </dl>       | El usuario rechazó la operación de TPM solicitada.<br/>           |
| <span id="TPM_E_PPI_BIOS_FAILURE"></span><span id="tpm_e_ppi_bios_failure"></span><dl> <dt>**TPM \_ E \_ PPP BIOS FAILURE \_ \_ 2150171394**</dt> <dt>(0x80290302)</dt> </dl> | Error del BIOS al ejecutar la operación de TPM.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                                                      | Descripción                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                      | Método realizado correctamente.<br/>                                                            |
| <dl> <dt>**TPM \_ E \_ PPP \_ ACPI \_ FAILURE**</dt> <dt>2150171392 (0x80290300)</dt> </dl> | Se produjo un error de hardware. Consulte al fabricante del equipo para obtener más información.<br/> |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                      |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Tpm de \_ Win32**](win32-tpm.md)
</dt> <dt>

[**Borrar**](clear-win32-tpm.md)
</dt> <dt>

[**Deshabilitar**](disable-win32-tpm.md)
</dt> <dt>

[**Habilitar**](enable-win32-tpm.md)
</dt> <dt>

[**IsEnabled**](isenabled-win32-tpm.md)
</dt> </dl>

 

 
