---
title: Método StoreInstallMethod de la MDM_EnterpriseModernAppManagement_AppInstallation01_01 clase
description: Método para realizar una instalación de una aplicación y una licencia desde Windows Store. Consulte también StoreInstall.
ms.assetid: 4f8aff47-ad16-4fe5-85be-7ddb55ddff24
keywords:
- Método StoreInstallMethod
- Método StoreInstallMethod, MDM_EnterpriseModernAppManagement_AppInstallation01_01 clase
- MDM_EnterpriseModernAppManagement_AppInstallation01_01 clase, método StoreInstallMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.StoreInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a8e60134da45982773c0219ade8e0e0f12f37ec9e6d16cd97f4595ae8b507a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084945"
---
# <a name="storeinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a>Método StoreInstallMethod de la clase \_ MDM EnterpriseInstallAppManagement \_ AppInstallation01 \_ 01

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Método para realizar una instalación de una aplicación y una licencia desde Windows Store. Consulte también [StoreInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).

## <a name="syntax"></a>Sintaxis


```mof
uint32 StoreInstallMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*param* \[ En\]
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

