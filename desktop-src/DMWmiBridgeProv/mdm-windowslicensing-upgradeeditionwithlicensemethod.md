---
title: Método UpgradeEditionWithLicenseMethod de la MDM_WindowsLicensing clase
description: Método para proporcionar una licencia para una actualización de edición de Windows 10 dispositivos móviles. Consulte también UpgradeEditionWithLicense.
ms.assetid: 1a57fb71-eea6-41bf-bc44-6d3a816096a4
keywords:
- Método UpgradeEditionWithLicenseMethod
- Método UpgradeEditionWithLicenseMethod, MDM_WindowsLicensing clase
- MDM_WindowsLicensing clase, método UpgradeEditionWithLicenseMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithLicenseMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26329c98bc73919d374787deea21841a2912a9df3fded8fdcde0637d8798c92f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913265"
---
# <a name="upgradeeditionwithlicensemethod-method-of-the-mdm_windowslicensing-class"></a>Método UpgradeEditionWithLicenseMethod de la clase \_ WindowsLicensing de MDM

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Método para proporcionar una licencia para una actualización de edición de Windows 10 dispositivos móviles. Consulte también [UpgradeEditionWithLicense](/windows/client-management/mdm/windowslicensing-csp).

## <a name="syntax"></a>Sintaxis


```mof
uint32 UpgradeEditionWithLicenseMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*param* \[ En\]
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MDM \_ WindowsLicensing**](mdm-windowslicensing.md)
</dt> <dt>

[Uso de scripts de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

