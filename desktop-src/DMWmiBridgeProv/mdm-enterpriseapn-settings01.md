---
title: MDM_EnterpriseAPN_Settings01 clase
description: La empresa usa la clase \_ MDM EnterpriseAPN \_ Settings01 para cambiar la configuración global de APN.
ms.assetid: 3f2d3d38-c389-4945-b519-5f2d7dedb86c
keywords:
- MDM_EnterpriseAPN_Settings01 clase
- MDM_EnterpriseAPN_Settings01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseAPN_Settings01
- MDM_EnterpriseAPN_Settings01.InstanceID
- MDM_EnterpriseAPN_Settings01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6150e86f798e9408117daac5966f1efdecae4063ae3c4665b3f7577c1e2f31e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053535"
---
# <a name="mdm_enterpriseapn_settings01-class"></a>Clase MDM \_ EnterpriseAPN \_ Settings01

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

La empresa usa la clase **\_ MDM EnterpriseAPN \_ Settings01** para cambiar la configuración global de APN.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseAPN_Settings01
{
  string  InstanceID;
  string  ParentID;
  boolean AllowUserControl;
  boolean HideView;
};
```

## <a name="members"></a>Miembros

La **clase MDM \_ EnterpriseAPN \_ Settings01** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ Mdm EnterpriseAPN \_ Settings01** tiene estas propiedades.

<dl> <dt>

[AllowUserControl](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-settings-allowusercontrol)
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[HideView](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-settings-hideview)
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
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

Nodo que contiene la configuración global de APN.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/EnterpriseAPN/Configuración"

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

