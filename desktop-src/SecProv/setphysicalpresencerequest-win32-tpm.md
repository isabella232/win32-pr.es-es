---
description: Solicita una operación de TPM que requiere presencia física.
ms.assetid: e71eb6ab-b6ab-4586-8999-0a464f11047a
title: Método SetPhysicalPresenceRequest de la Win32_Tpm clase
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
ms.openlocfilehash: 9c1b1e2760ed5015b6b682b94bd364e469edb4ed519adc371e2c348a0bf8c607
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891360"
---
# <a name="setphysicalpresencerequest-method-of-the-win32_tpm-class"></a>Método SetPhysicalPresenceRequest de la clase Tpm de \_ Win32

El **método SetPhysicalPresenceRequest** de la clase [**\_ Tpm de Win32**](win32-tpm.md) solicita una operación de TPM que requiere presencia física. Después de usar este método para enviar una solicitud, aplique el siguiente paso indicado en el [**método GetPhysicalPresenceTransition.**](getphysicalpresencetransition-win32-tpm.md) Por último, use [**el método GetPhysicalPresenceResponse para**](getphysicalpresenceresponse-win32-tpm.md) comprobar si la operación se ejecutó correctamente. Este método suspende BitLocker si la llamada a podría provocar que se requiera la recuperación de BitLocker. BitLocker se reanudaría automáticamente una vez que se haya aprovisionado TPM.

Estos pasos son necesarios porque las operaciones de presencia física solo se pueden ejecutar después de que el equipo haya detectado al usuario físicamente presente.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetPhysicalPresenceRequest(
  [in] uint32 Request
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Solicitud* \[ En\]
</dt> <dd>

Tipo: **uint32**

Valor entero que especifica la operación de TPM solicitada que requiere presencia física.



| Valor                                                                                                                               | Significado                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                                                        | Sin solicitud.<br/> Use este valor para borrar una solicitud pendiente.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>1</dt> </dl>                                                        | Habilite el TPM.<br/> Esta operación se invierte mediante la operación 2.<br/> Para obtener más información, vea los siguientes métodos relacionados que no implican la presencia física: [**Enable**](enable-win32-tpm.md) [**y IsEnabled.**](isenabled-win32-tpm.md)<br/>                                 |
| <dl> <dt>2</dt> </dl>                                                        | Deshabilite el TPM.<br/> Esta operación se invierte mediante la operación 1.<br/> Para obtener más información, vea el siguiente método relacionado que no implica presencia física: [**Deshabilitar**](disable-win32-tpm.md).<br/>                                                                          |
| <dl> <dt>3</dt> </dl>                                                        | Active el TPM.<br/> Esta operación se invierte mediante la operación 4.<br/>                                                                                                                                                                                                                          |
| <dl> <dt>4</dt> </dl>                                                        | Desactive el TPM.<br/> Esta operación se invierte mediante la operación 3.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>5</dt> </dl>                                                        | Borre el TPM.<br/> Esta operación no se puede invertir.<br/> Para obtener más información, vea el siguiente método relacionado que no implica presencia física: [**Clear**](clear-win32-tpm.md).<br/>                                                                                        |
| <dl> <dt>6</dt> </dl>                                                        | Habilite y active el TPM.<br/> Esta operación se invierte mediante la operación 7.<br/>                                                                                                                                                                                                               |
| <dl> <dt>7</dt> </dl>                                                        | Desactive y deshabilite el TPM.<br/> Esta operación se invierte mediante la operación 6.<br/>                                                                                                                                                                                                            |
| <dl> <dt>8</dt> </dl>                                                        | Permitir la instalación de un propietario de TPM.<br/> Esta operación se invierte mediante la operación 9.<br/>                                                                                                                                                                                                     |
| <dl> <dt>9</dt> </dl>                                                        | Impedir la instalación de un propietario de TPM.<br/> Esta operación se invierte mediante la operación 8. <br/>                                                                                                                                                                                                  |
| <dl> <dt>10</dt> </dl>                                                       | Habilitar, activar y permitir la instalación de un propietario de TPM.<br/> Esta operación se invierte mediante la operación 11.<br/>                                                                                                                                                                              |
| <dl> <dt>11</dt> </dl>                                                       | Desactive, deshabilite e impida la instalación de un propietario de TPM.<br/> Esta operación se invierte mediante la operación 10.<br/>                                                                                                                                                                         |
| <dl> <dt></dt><dt>12</dt> </dl> | Presencia física diferidaacodFieldUpgrade<br/> Se ha actualizado la configuración de presencia física.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:** Este valor no se admite.<br/>                                                                       |
| <dl> <dt>14</dt> </dl>                                                       | Borre, habilite y active el TPM.<br/> Esta operación no se puede invertir.<br/>                                                                                                                                                                                                               |
| <dl> <dt>15</dt> </dl>                                                       | SetNo PPPProvision \_ False<br/> Establece el aprovisionamiento que debe tener presencia física para establecer el TPM.<br/> Esta operación se invierte mediante la operación 16.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:** Este valor no se admite.<br/>         |
| <dl> <dt>16</dt> </dl>                                                       | SetNo PPPProvision \_ True<br/> Establece el aprovisionamiento que no es necesario que esté físicamente presente para establecer el TPM.<br/> Esta operación se invierte mediante la operación 15.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:** Este valor no se admite.<br/> |
| <dl> <dt>17</dt> </dl>                                                       | SetNo PPPClear \_ False<br/> Establece el aprovisionamiento que debe tener presencia física para borrar el TPM.<br/> Esta operación se invierte mediante la operación 18.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:** Este valor no se admite.<br/>           |
| <dl> <dt>18</dt> </dl>                                                       | SetNo PPPClear \_ True<br/> Establece el aprovisionamiento que no es necesario que esté físicamente presente para borrar el TPM.<br/> Esta operación se invierte mediante la operación 17.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:** Este valor no se admite.<br/>   |
| <dl> <dt>19</dt> </dl>                                                       | SetNo PPPMaintenance \_ False<br/> Establece el aprovisionamiento que debe tener presencia física para mantener el TPM.<br/> Esta operación se invierte mediante la operación 20.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:** Este valor no se admite.<br/>  |
| <dl> <dt>20</dt> </dl>                                                       | SetNo PPPMaintenance \_ True<br/> Establece el aprovisionamiento que no es necesario que esté físicamente presente para mantener el TPM.<br/> Esta operación se invierte mediante la operación 19.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:** Este valor no se admite.<br/>   |
| <dl> <dt>21</dt> </dl>                                                       | Habilitar + Activar + Borrar<br/> Habilite, active y desactive el TPM.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:** Este valor no se admite.<br/>                                                                                                  |
| <dl> <dt>22</dt> </dl>                                                       | Habilitar + Activar + Borrar + Habilitar + Activar<br/> Habilite, active y desactive el TPM y, a continuación, habilite y reactive el TPM.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:** Este valor no se admite.<br/>                                      |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.



| Código o valor devuelto                                                                                                                                                                       | Descripción                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                       | Método realizado correctamente.<br/> Use el [**método GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md) para determinar el paso siguiente que se necesita.<br/>                                                  |
| <dl> <dt>**TPM \_ E \_ PPP NO \_ \_ COMPATIBLE**</dt> <dt>2150171395 (0x80290303)</dt> </dl> | El equipo no admite operaciones de presencia física de TPM mediante este método.<br/> Consulte al fabricante del equipo para obtener más información. El BIOS del equipo puede tener compatibilidad alternativa para configurar el TPM.<br/> |
| <dl> <dt>**TPM \_ E \_ PPP \_ ACPI \_ FAILURE**</dt> <dt>2150171392 (0x80290300)</dt> </dl>  | Se produjo un error de hardware.<br/> Consulte al fabricante del equipo para obtener más información.<br/>                                                                                                                                  |



 

## <a name="remarks"></a>Comentarios

Las operaciones de presencia física de TPM no requieren autorización del propietario del TPM. Sin embargo, requieren pasos adicionales para ayudar a protegerse frente a cambios no autorizados en el TPM.

Los equipos que admiten operaciones de presencia física de TPM intentarán detectar al usuario físicamente presente antes de ejecutar la operación. Aunque los equipos pueden diferir en la forma en que se realiza esta detección, la idea es que un usuario o administrador presente físicamente autorice la operación.

Por ejemplo, el equipo puede requerir que el usuario reinicie el equipo. Una vez reiniciado el equipo, el equipo puede mostrar un cuadro de diálogo de confirmación del BIOS que permite al usuario confirmar la operación mediante el teclado.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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

[**Habilitar**](enable-win32-tpm.md)
</dt> <dt>

[**IsEnabled**](isenabled-win32-tpm.md)
</dt> <dt>

[**Deshabilitar**](disable-win32-tpm.md)
</dt> <dt>

[**Borrar**](clear-win32-tpm.md)
</dt> </dl>

 

 
