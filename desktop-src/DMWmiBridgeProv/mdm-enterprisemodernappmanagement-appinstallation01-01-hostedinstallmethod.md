---
title: Método HostedInstallMethod de la MDM_EnterpriseModernAppManagement_AppInstallation01_01 clase
description: Método para realizar una instalación de un paquete de aplicación desde una ubicación hospedada, como una unidad local, un origen de datos UNC o HTTPS. Consulte también HostedInstall.
ms.assetid: 1ec16315-75ce-4613-804e-6b587c4071d6
keywords:
- Método HostedInstallMethod
- Método HostedInstallMethod, MDM_EnterpriseModernAppManagement_AppInstallation01_01 clase
- MDM_EnterpriseModernAppManagement_AppInstallation01_01, método HostedInstallMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.HostedInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60cd27419dce09b2a0e4aa7304bb53ac63e7d205b93cbaacbf832aa4a3501338
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750635"
---
# <a name="hostedinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a>Método HostedInstallMethod de la clase \_ MDM EnterpriseInstallAppManagement \_ AppInstallation01 \_ 01

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Método para realizar una instalación de un paquete de aplicación desde una ubicación hospedada, como una unidad local, un origen de datos UNC o HTTPS. Consulte también [HostedInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).

## <a name="syntax"></a>Sintaxis


```mof
uint32 HostedInstallMethod(
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

[**MDM \_ \_ EnterpriseInstallation01 01 AppInstallation \_**](mdm-enterprisemodernappmanagement-appinstallation01-01.md)
</dt> <dt>

[Uso de scripts de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

