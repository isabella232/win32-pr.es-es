---
description: Solicita una operación de TPM que requiere presencia física.
ms.assetid: e71eb6ab-b6ab-4586-8999-0a464f11047a
title: Método SetPhysicalPresenceRequest de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.SetPhysicalPresenceRequest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 55a0f8c5fc0a8573192f25e3901b63f24e05f7c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666380"
---
# <a name="setphysicalpresencerequest-method-of-the-win32_tpm-class"></a>Método SetPhysicalPresenceRequest de la \_ clase Win32 TPM

El método **SetPhysicalPresenceRequest** de la clase de [**Win32 \_ TPM**](win32-tpm.md) solicita una operación de TPM que requiere presencia física. Después de usar este método para enviar una solicitud, aplique el siguiente paso indicado en el método [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md) . Por último, use el método [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) para comprobar si la operación se ejecutó correctamente. Este método suspende BitLocker si la llamada puede hacer que se requiera la recuperación de BitLocker. BitLocker se reanudará automáticamente una vez que se haya aprovisionado TPM.

Estos pasos son necesarios porque las operaciones de presencia física solo se pueden ejecutar después de que el equipo haya detectado el usuario presente físicamente.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetPhysicalPresenceRequest(
  [in] uint32 Request
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Solicitud* \[ de de\]
</dt> <dd>

Tipo: **UInt32**

Valor entero que especifica la operación de TPM solicitada que requiere presencia física.



| Value                                                                                                                               | Significado                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                                                        | Ninguna solicitud.<br/> Use este valor para borrar una solicitud pendiente.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>1</dt> </dl>                                                        | Habilite el TPM.<br/> Esta operación se invierte en la operación 2.<br/> Para obtener más información, vea los siguientes métodos relacionados que no implican presencia física: [**enable**](enable-win32-tpm.md) y [**IsEnabled**](isenabled-win32-tpm.md).<br/>                                 |
| <dl> <dt>2</dt> </dl>                                                        | Deshabilite TPM.<br/> Esta operación se invierte en la operación 1.<br/> Para obtener más información, vea el siguiente método relacionado que no implica la presencia física: [**Disable**](disable-win32-tpm.md).<br/>                                                                          |
| <dl> <dt>3</dt> </dl>                                                        | Active el TPM.<br/> Esta operación se invierte en la operación 4.<br/>                                                                                                                                                                                                                          |
| <dl> <dt>4</dt> </dl>                                                        | Desactive el TPM.<br/> Esta operación se invierte en la operación 3.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>5</dt> </dl>                                                        | Borre el TPM.<br/> Esta operación no se puede revertir.<br/> Para obtener más información, vea el siguiente método relacionado que no implica la presencia física: [**Clear**](clear-win32-tpm.md).<br/>                                                                                        |
| <dl> <dt>6</dt> </dl>                                                        | Habilitar y activar el TPM.<br/> Esta operación se invierte en la operación 7.<br/>                                                                                                                                                                                                               |
| <dl> <dt>7</dt> </dl>                                                        | Desactivar y deshabilitar TPM.<br/> Esta operación se invierte en la operación 6.<br/>                                                                                                                                                                                                            |
| <dl> <dt>8</dt> </dl>                                                        | Permitir la instalación de un propietario de TPM.<br/> Esta operación se invierte en la operación 9.<br/>                                                                                                                                                                                                     |
| <dl> <dt>9</dt> </dl>                                                        | Impedir la instalación de un propietario de TPM.<br/> Esta operación se invierte en la operación 8. <br/>                                                                                                                                                                                                  |
| <dl> <dt>10</dt> </dl>                                                       | Habilitar, activar y permitir la instalación de un propietario de TPM.<br/> Esta operación se invierte en la operación 11.<br/>                                                                                                                                                                              |
| <dl> <dt>11</dt> </dl>                                                       | Desactive, deshabilite y evite la instalación de un propietario de TPM.<br/> Esta operación se invierte en la operación 10.<br/>                                                                                                                                                                         |
| <dl> <dt></dt><dt>12</dt> </dl> | PresenceunownedFieldUpgrade físico diferida<br/> La configuración de presencia física se ha actualizado.<br/> **Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Este valor no se admite.<br/>                                                                       |
| <dl> <dt>14</dt> </dl>                                                       | Desactive, habilite y active el TPM.<br/> Esta operación no se puede revertir.<br/>                                                                                                                                                                                                               |
| <dl> <dt>15</dt> </dl>                                                       | SetNoPPIProvision \_ false<br/> Establece la provisión de que debe estar físicamente en presencia para establecer el TPM.<br/> Esta operación se invierte en la operación 16.<br/> **Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Este valor no se admite.<br/>         |
| <dl> <dt>16</dt> </dl>                                                       | SetNoPPIProvision \_ true<br/> Establece el aprovisionamiento que no es necesario tener físicamente en presencia para establecer el TPM.<br/> Esta operación se invierte en la operación 15.<br/> **Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Este valor no se admite.<br/> |
| <dl> <dt>17</dt> </dl>                                                       | SetNoPPIClear \_ false<br/> Establece la provisión de que debe estar físicamente en presencia para borrar el TPM.<br/> Esta operación se invierte en la operación 18.<br/> **Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Este valor no se admite.<br/>           |
| <dl> <dt>18</dt> </dl>                                                       | SetNoPPIClear \_ true<br/> Establece el aprovisionamiento que no es necesario tener físicamente en presencia para borrar el TPM.<br/> Esta operación se invierte en la operación 17.<br/> **Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Este valor no se admite.<br/>   |
| <dl> <dt>19</dt> </dl>                                                       | SetNoPPIMaintenance \_ false<br/> Establece la provisión de que debe estar físicamente en presencia para mantener el TPM.<br/> Esta operación se invierte en la operación 20.<br/> **Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Este valor no se admite.<br/>  |
| <dl> <dt>20</dt> </dl>                                                       | SetNoPPIMaintenance \_ true<br/> Establece la provisión de que no es necesario tener físicamente presencia para mantener el TPM.<br/> Esta operación se invierte en la operación 19.<br/> **Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Este valor no se admite.<br/>   |
| <dl> <dt>21</dt> </dl>                                                       | Habilitar + Activar + borrar<br/> Habilite, Active y desactive el TPM.<br/> **Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Este valor no se admite.<br/>                                                                                                  |
| <dl> <dt>22</dt> </dl>                                                       | Habilitar + Activar + desactivar + habilitar + activar<br/> Habilite, Active y desactive el TPM y, a continuación, habilite y vuelva a activar TPM.<br/> **Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Este valor no se admite.<br/>                                      |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.



| Código o valor devuelto                                                                                                                                                                       | Descripción                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                       | Método realizado correctamente.<br/> Use el método [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md) para determinar el siguiente paso que se necesita.<br/>                                                  |
| <dl> <dt>**TPM \_ \_No se \_ \_ admiten PPP E**</dt> <dt>2150171395 (0x80290303)</dt> </dl> | El equipo no admite operaciones de presencia física de TPM mediante este método.<br/> Consulte al fabricante del equipo para obtener más información. Es posible que el BIOS del equipo tenga compatibilidad alternativa con la configuración del TPM.<br/> |
| <dl> <dt>**TPM \_ E \_ PPI \_ ACPI \_ error**</dt> <dt>2150171392 (0x80290300)</dt> </dl>  | Error de hardware.<br/> Consulte al fabricante del equipo para obtener más información.<br/>                                                                                                                                  |



 

## <a name="remarks"></a>Observaciones

Las operaciones de presencia física del TPM no requieren la autorización del propietario del TPM. Sin embargo, requieren pasos adicionales para ayudar a protegerse contra cambios no autorizados en el TPM.

Los equipos que admiten operaciones de presencia física de TPM intentarán detectar el usuario presente físicamente antes de ejecutar la operación. Aunque es posible que los equipos difieran en la forma en que se realiza esta detección, la idea es que un usuario o administrador presente de forma física autorice la operación.

Por ejemplo, el equipo puede requerir que el usuario reinicie el equipo. Una vez reiniciado el equipo, el equipo puede mostrar un cuadro de diálogo de confirmación del BIOS que permite al usuario confirmar la operación mediante el teclado.

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

[**Habilitar**](enable-win32-tpm.md)
</dt> <dt>

[**IsEnabled**](isenabled-win32-tpm.md)
</dt> <dt>

[**Disable**](disable-win32-tpm.md)
</dt> <dt>

[**Claridad**](clear-win32-tpm.md)
</dt> </dl>

 

 
