---
title: MDM_Policy_Config01_NetworkIsolation02 (clase)
description: La \_ clase Config01 de NetworkIsolation02 de directivas MDM \_ \_ representa las directivas de explorador disponibles.
ms.assetid: f25ecbef-d232-4731-bac8-38a7d597db00
keywords:
- MDM_Policy_Config01_NetworkIsolation02 (clase)
- MDM_Policy_Config01_NetworkIsolation02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_NetworkIsolation02
- MDM_Policy_Config01_NetworkIsolation02.InstanceID
- MDM_Policy_Config01_NetworkIsolation02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9062d150de07860fd9d5b2510269ddcc3d2f8a35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079348"
---
# <a name="mdm_policy_config01_networkisolation02-class"></a>\_ \_ Clase NetworkIsolation02 de Config01 de directivas MDM \_

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

La **clase \_ \_ Config01 de \_ NetworkIsolation02 de directivas MDM** representa las directivas de explorador disponibles.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_NetworkIsolation02
{
  string InstanceID;
  string ParentID;
  string EnterpriseIPRange;
  sint32 EnterpriseIPRangesAreAuthoritative;
  string EnterpriseNetworkDomainNames;
  string EnterpriseProxyServers;
  sint32 EnterpriseProxyServersAreAuthoritative;
  string NeutralResources;
  string EnterpriseCloudResources;
  string EnterpriseInternalProxyServers;
};
```

## <a name="members"></a>Miembros

La clase Config01 de la **\_ Directiva MDM \_ \_ NetworkIsolation02** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ \_ Config01 de \_ NetworkIsolation02 de directivas MDM** tiene estas propiedades.

<dl> <dt>

[EnterpriseCloudResources](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisecloudresources)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

[EnterpriseInternalProxyServers](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseinternalproxyservers)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

[EnterpriseIPRange](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprange)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

[EnterpriseIPRangesAreAuthoritative](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprangesareauthoritative)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

[EnterpriseNetworkDomainNames](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisenetworkdomainnames)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

[EnterpriseProxyServers](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyservers)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

[EnterpriseProxyServersAreAuthoritative](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyserversareauthoritative)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica el nombre del nodo primario. Para esta clase, la cadena es "NetworkIsolation".

</dd> <dt>

[NeutralResources](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-neutralresources)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | Dmmap de MDM raíz de \\ cimv2 \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

