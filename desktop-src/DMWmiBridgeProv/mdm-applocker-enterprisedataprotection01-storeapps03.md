---
title: MDM_AppLocker_EnterpriseDataProtection01_StoreApps03 clase
description: La clase Mdm \_ AppLocker \_ EnterpriseDataProtection01 StoreApps03 captura la lista de aplicaciones Windows que pueden controlar \_ datos empresariales. Debe usarse junto con la configuración de ./Vendor/MSFT/Policy/ConfigSource/DataProtection .
ms.assetid: f37fe52d-dbe1-45b7-acd5-5047c46d9bd0
keywords:
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03 clase
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5b0c3af455e501695cb7a2093b841159f5755ac54e1de97a370c7dc7f2d6fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077419"
---
# <a name="mdm_applocker_enterprisedataprotection01_storeapps03-class"></a>Clase \_ Mdm AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

La **clase Mdm \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** captura la lista de aplicaciones Windows que pueden controlar datos empresariales. Debe usarse junto con la configuración de ./Vendor/MSFT/Policy/ConfigSource/DataProtection .

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a>Miembros

La **clase Mdm \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Mdm \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** tiene estas propiedades.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Define las restricciones para ejecutar aplicaciones de la Tienda Windows.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Grouping"*

</dd> <dt>

[**Directiva**](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | DMMap \\ \\ de MDM de CIMv2 \\ raíz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de scripts de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

