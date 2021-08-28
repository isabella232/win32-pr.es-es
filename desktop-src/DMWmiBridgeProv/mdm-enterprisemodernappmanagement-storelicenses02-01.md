---
title: MDM_EnterpriseModernAppManagement_StoreLicenses02_01 clase
description: La clase MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 01 se usa \_ para administrar licencias para aplicaciones de la tienda.
ms.assetid: 9fdcba35-6c21-4a39-99f4-470acf7d35bb
keywords:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01 clase
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.InstanceID
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0342acc9cb74825552a409d686e5bc55f0cebc75642d5981a7144f3bac74bee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018113"
---
# <a name="mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a>Clase \_ MDM EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

La **clase MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** se usa para administrar licencias para aplicaciones de la tienda.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_StoreLicenses02_01
{
  string InstanceID;
  string ParentID;
  string LicenseCategory;
  string LicenseUsage;
  string RequesterID;
};
```

## <a name="members"></a>Miembros

La **clase \_ MDM EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ MDM EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** tiene estos métodos.



| Método                                                                                                              | Descripción                                             |
|:--------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| [**AddLicenseMethod**](mdm-enterprisemodernappmanagement-storelicenses02-01-addlicensemethod.md)                   | Método para agregar una licencia.<br/>                 |
| [**GetLicenseFromStoreMethod**](mdm-enterprisemodernappmanagement-storelicenses02-01-getlicensefromstoremethod.md) | Método para obtener una licencia de la tienda.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ MDM EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** tiene estas propiedades.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nodo opcional. Identificador de licencia de una aplicación instalada de la tienda. El identificador de licencia suele ser el PFN de la aplicación.

Las operaciones admitidas son Agregar, Obtener y Eliminar.

</dd> <dt>

[LicenseCategory](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licensecategory)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[LicenseUsage](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licenseusage)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
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

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/EnterpriseModernAppManagement/AppLicenses/StoreLicenses"

</dd> <dt>

[RequesterID](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-requesterid)
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
| Espacio de nombres<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de scripts de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

