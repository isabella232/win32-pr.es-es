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
ms.openlocfilehash: e8c4518653b9ff34aac69a4e8474940c7998429b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467071"
---
# <a name="getphysicalpresenceresponse-method-of-the-win32_tpm-class"></a>Método GetPhysicalPresenceResponse de la clase Tpm de \_ Win32

El **método GetPhysicalPresenceResponse** de la clase [**\_ Tpm de Win32**](win32-tpm.md) devuelve los resultados de una operación de presencia física de TPM que se realizó. Use el [**método SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) para solicitar una operación.

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




| Valor | Significado | 
|-------|---------|
| <dl><dt>0</dt></dl> | Sin solicitud.<br /> No se realizó ninguna operación de presencia física.<br /> | 
| <dl><dt>1</dt></dl> | Habilite el TPM.<br /> Esta operación se invierte mediante la operación 2. <br /> Para obtener más información, vea estos métodos relacionados que no implican la presencia física:<ul><li><a href="enable-win32-tpm.md"><strong>Habilitar</strong></a></li><li><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></li></ul><br /> | 
| <dl><dt>2</dt></dl> | Deshabilite el TPM.<br /> Esta operación se invierte mediante la operación 1. <br /> Para obtener más información, vea este método relacionado que no implica presencia física: <a href="disable-win32-tpm.md"><strong>Deshabilitar</strong></a>.<br /> | 
| <dl><dt>3</dt></dl> | Active el TPM.<br /> Esta operación se invierte mediante la operación 4.<br /> | 
| <dl><dt>4</dt></dl> | Desactive el TPM.<br /> Esta operación se invierte mediante la operación 3.<br /> | 
| <dl><dt>5</dt></dl> | Borre el TPM.<br /> Esta operación no se puede invertir. <br /> Para obtener más información, vea este método relacionado que no implica presencia física: <a href="clear-win32-tpm.md"><strong>Borrar</strong></a>.<br /> | 
| <dl><dt>6</dt></dl> | Habilite y active el TPM.<br /> Esta operación se invierte mediante la operación 7.<br /> | 
| <dl><dt>7</dt></dl> | Desactive y deshabilite el TPM.<br /> Esta operación se invierte mediante la operación 6. <br /> | 
| <dl><dt>8</dt></dl> | Permitir la instalación de un propietario de TPM.<br /> Esta operación se invierte mediante la operación 9.<br /> | 
| <dl><dt>9</dt></dl> | Impedir la instalación de un propietario de TPM.<br /> Esta operación se invierte mediante la operación 8. <br /> | 
| <dl><dt>10</dt></dl> | Habilitar, activar y permitir la instalación de un propietario de TPM.<br /> Esta operación se invierte mediante la operación 11.<br /> | 
| <dl><dt>11</dt></dl> | Desactivar, deshabilitar e impedir la instalación de un propietario de TPM.<br /> Esta operación se invierte mediante la operación 10.<br /> | 
| <span></span><dl><dt><strong></strong></dt><dt>12</dt></dl> | Presencia física diferidaacownedFieldUpgrade<br /> Se ha actualizado la configuración de presencia física.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:</strong> Este valor no se admite.<br /> | 
| <dl><dt>14</dt></dl> | Borre, habilite y active el TPM.<br /> Esta operación no se puede invertir.<br /> | 
| <dl><dt>15</dt></dl> | SetNoPPIProvision_False<br /> Establece el aprovisionamiento que debe tener físicamente para establecer el TPM.<br /> Esta operación se invierte mediante la operación 16.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:</strong> Este valor no se admite.<br /> | 
| <dl><dt>16</dt></dl> | SetNoPPIProvision_True<br /> Establece el aprovisionamiento que no es necesario que esté físicamente presente para establecer el TPM.<br /> Esta operación se invierte mediante la operación 15.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:</strong> Este valor no se admite.<br /> | 
| <dl><dt>17</dt></dl> | SetNoPPIClear_False<br /> Establece el aprovisionamiento que debe tener presencia física para borrar el TPM.<br /> Esta operación se invierte mediante la operación 18.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:</strong> Este valor no se admite.<br /> | 
| <dl><dt>18</dt></dl> | SetNoPPIClear_True<br /> Establece el aprovisionamiento que no es necesario que esté físicamente presente para borrar el TPM.<br /> Esta operación se invierte mediante la operación 17.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:</strong> Este valor no se admite.<br /> | 
| <dl><dt>19</dt></dl> | SetNoPPIMaintenance_False<br /> Establece el aprovisionamiento que debe tener físicamente para mantener el TPM.<br /> Esta operación se invierte mediante la operación 20.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:</strong> Este valor no se admite.<br /> | 
| <dl><dt>20</dt></dl> | SetNoPPIMaintenance_True<br /> Establece el aprovisionamiento que debe tener físicamente para mantener el TPM.<br /> Esta operación se invierte mediante la operación 19.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:</strong> Este valor no se admite.<br /> | 
| <dl><dt>21</dt></dl> | Habilitar + Activar + Borrar<br /> Habilite, active y borre el TPM.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:</strong> Este valor no se admite.<br /> | 
| <dl><dt>22</dt></dl> | Habilitar + Activar + Borrar + Habilitar + Activar<br /> Habilite, active y borre el TPM y, a continuación, habilite y reactive el TPM.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:</strong> Este valor no se admite.<br /> | 




 

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
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0 (0x0)</dt> </dl>                                      | Método realizado correctamente.<br/>                                                            |
| <dl> <dt>**TPM \_ E \_ PPP \_ ACPI \_ FAILURE**</dt> <dt>2150171392 (0x80290300)</dt> </dl> | Se produjo un error de hardware. Consulte al fabricante del equipo para obtener más información.<br/> |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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

 

 
