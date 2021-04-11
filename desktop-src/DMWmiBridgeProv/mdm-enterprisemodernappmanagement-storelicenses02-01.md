---
title: MDM_EnterpriseModernAppManagement_StoreLicenses02_01 (clase)
description: La \_ clase EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 de MDM se usa para administrar las licencias de las aplicaciones de la tienda.
ms.assetid: 9fdcba35-6c21-4a39-99f4-470acf7d35bb
keywords:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01 (clase)
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
ms.openlocfilehash: 19a4549ba473afaf76bea3f23ec65aacf301121a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079595"
---
# <a name="mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a>\_Clase EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 de MDM

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

La **clase \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 de MDM** se usa para administrar las licencias de las aplicaciones de la tienda.

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

La **clase \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 de MDM** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 de MDM** tiene estos métodos.



| Método                                                                                                              | Descripción                                             |
|:--------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| [**AddLicenseMethod**](mdm-enterprisemodernappmanagement-storelicenses02-01-addlicensemethod.md)                   | Método para agregar una licencia.<br/>                 |
| [**GetLicenseFromStoreMethod**](mdm-enterprisemodernappmanagement-storelicenses02-01-getlicensefromstoremethod.md) | Método para obtener una licencia del almacén.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 de MDM** tiene estas propiedades.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nodo opcional. IDENTIFICADOR de licencia para una aplicación instalada en el almacén. El identificador de licencia es generalmente el PFN de la aplicación.

Las operaciones admitidas son Add, get y DELETE.

</dd> <dt>

[LicenseCategory](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licensecategory)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

[LicenseUsage](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licenseusage)
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

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/EnterpriseModernAppManagement/AppLicenses/StoreLicenses".

</dd> <dt>

[RequesterID](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-requesterid)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | Dmmap de MDM raíz de \\ cimv2 \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar scripting de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

