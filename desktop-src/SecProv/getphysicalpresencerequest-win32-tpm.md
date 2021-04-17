---
description: Devuelve la operación de presencia física de TPM pendiente. Use el método SetPhysicalPresenceRequest para solicitar una operación.
ms.assetid: c50378ae-b465-4c82-beb9-8ecb7939dae2
title: Método GetPhysicalPresenceRequest de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceRequest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8d631aabfc1e2df15aa4182b8332091fe503f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688155"
---
# <a name="getphysicalpresencerequest-method-of-the-win32_tpm-class"></a>Método GetPhysicalPresenceRequest de la \_ clase Win32 TPM

El método **GetPhysicalPresenceRequest** de la clase [**Win32 \_ TPM**](win32-tpm.md) devuelve la operación de presencia física de TPM pendiente. Use el método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) para solicitar una operación.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetPhysicalPresenceRequest(
  [out] uint32 Request
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Solicitud* \[ de enuncia\]
</dt> <dd>

Tipo: **UInt32**

Valor que especifica la operación de presencia física del TPM pendiente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt>0,1</dt> </dl></td>
<td>Ninguna solicitud.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>1</dt> </dl></td>
<td>Habilite el TPM.<br/> Esta operación se invierte en la operación 2. <br/> Para obtener más información, consulte estos métodos relacionados que no implican la presencia física:
<ul>
<li><a href="enable-win32-tpm.md"><strong>Habilitar</strong></a></li>
<li><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>2</dt> </dl></td>
<td>Deshabilite TPM.<br/> Esta operación se invierte en la operación 1. <br/> Para obtener más información, vea este método relacionado que no implica la presencia física: <a href="disable-win32-tpm.md"><strong>deshabilitar</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>3</dt> </dl></td>
<td>Active el TPM.<br/> Esta operación se invierte en la operación 4.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>4</dt> </dl></td>
<td>Desactive el TPM.<br/> Esta operación se invierte en la operación 3.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>5</dt> </dl></td>
<td>Borre el TPM.<br/> Esta operación no se puede revertir.<br/> Para obtener más información, consulte este método relacionado que no implica la presencia física: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>1,8</dt> </dl></td>
<td>Habilitar y activar el TPM. <br/> Esta operación se invierte en la operación 7.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>7</dt> </dl></td>
<td>Desactivar y deshabilitar TPM.<br/> Esta operación se invierte en la operación 6. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>203</dt> </dl></td>
<td>Permitir la instalación de un propietario de TPM. <br/> Esta operación se invierte en la operación 9.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>9</dt> </dl></td>
<td>Impedir la instalación de un propietario de TPM.<br/> Esta operación se invierte en la operación 8. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>7</dt> </dl></td>
<td>Habilitar, activar y permitir la instalación de un propietario de TPM.<br/> Esta operación se invierte en la operación 11.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>279</dt> </dl></td>
<td>Desactive, deshabilite y evite la instalación de un propietario de TPM.<br/> Esta operación se invierte en la operación 10.<br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <dt><strong></strong></dt><dt>12</dt> </dl></td>
<td>PresenceunownedFieldUpgrade físico diferida<br/> La configuración de presencia física se ha actualizado.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>14</dt> </dl></td>
<td>Desactive, habilite y active el TPM.<br/> Esta operación no se puede revertir.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>4,5</dt> </dl></td>
<td>SetNoPPIProvision_False<br/> Establece la provisión de que debe estar físicamente en presencia para establecer el TPM.<br/> Esta operación se invierte en la operación 16.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>dieciséi</dt> </dl></td>
<td>SetNoPPIProvision_True<br/> Establece el aprovisionamiento que no es necesario tener físicamente en presencia para establecer el TPM.<br/> Esta operación se invierte en la operación 15.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>18</dt> </dl></td>
<td>SetNoPPIClear_False<br/> Establece la provisión de que debe estar físicamente en presencia para borrar el TPM.<br/> Esta operación se invierte en la operación 18.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>18</dt> </dl></td>
<td>SetNoPPIClear_True<br/> Establece el aprovisionamiento que no es necesario tener físicamente en presencia para borrar el TPM.<br/> Esta operación se invierte en la operación 17.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>19</dt> </dl></td>
<td>SetNoPPIMaintenance_False<br/> Establece la provisión de que debe estar físicamente en presencia para mantener el TPM.<br/> Esta operación se invierte en la operación 20.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>20</dt> </dl></td>
<td>SetNoPPIMaintenance_True<br/> Establece la provisión de que debe estar físicamente en presencia para mantener el TPM.<br/> Esta operación se invierte en la operación 19.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>21</dt> </dl></td>
<td>Habilitar + Activar + borrar<br/> Habilite, Active y desactive el TPM.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>56</dt> </dl></td>
<td>Habilitar + Activar + desactivar + habilitar + activar<br/> Habilite, Active y desactive el TPM y, a continuación, habilite y vuelva a activar TPM.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.<br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

En la tabla siguiente se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                                                      | Descripción                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                      | Método realizado correctamente.<br/>                                                            |
| <dl> <dt>**TPM \_ E \_ PPI \_ ACPI \_ error**</dt> <dt>2150171392 (0x80290300)</dt> </dl> | Error de hardware. Consulte al fabricante del equipo para obtener más información.<br/> |



 

## <a name="remarks"></a>Observaciones

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

[**Claridad**](clear-win32-tpm.md)
</dt> <dt>

[**Disable**](disable-win32-tpm.md)
</dt> <dt>

[**Habilitar**](enable-win32-tpm.md)
</dt> <dt>

[**IsEnabled**](isenabled-win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
