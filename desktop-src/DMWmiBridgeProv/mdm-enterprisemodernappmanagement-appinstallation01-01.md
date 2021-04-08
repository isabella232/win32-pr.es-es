---
title: MDM_EnterpriseModernAppManagement_AppInstallation01_01 (clase)
description: La \_ clase EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 de MDM se usa para instalar aplicaciones de la tienda Windows o de una ubicación hospedada.
ms.assetid: fc4c4c82-6f43-41fc-863b-940c0517f28b
keywords:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01 (clase)
- MDM_EnterpriseModernAppManagement_AppInstallation01_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.InstanceID
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6cd3fc5478e73df5276fdc9d6a1d66c9649dd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996788"
---
# <a name="mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a>\_Clase EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 de MDM

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

La **clase \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 de MDM** se usa para instalar aplicaciones de la tienda Windows o de una ubicación hospedada.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppInstallation01_01
{
  string InstanceID;
  string ParentID;
  sint32 LastError;
  string LastErrorDesc;
  sint32 Status;
  sint32 ProgressStatus;
};
```

## <a name="members"></a>Miembros

La **clase \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 de MDM** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 de MDM** tiene estos métodos.



| Método                                                                                                    | Descripción                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**HostedInstallMethod**](mdm-enterprisemodernappmanagement-appinstallation01-01-hostedinstallmethod.md) | Método para realizar una instalación de un paquete de la aplicación desde una ubicación hospedada (puede ser una unidad local, un origen de datos UNC o https).<br/> |
| [**StoreInstallMethod**](mdm-enterprisemodernappmanagement-appinstallation01-01-storeinstallmethod.md)   | Método para realizar una instalación de una aplicación y una licencia de la tienda Windows.<br/>                                                    |



 

### <a name="properties"></a>Propiedades

La **clase \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 de MDM** tiene estas propiedades.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica el nombre del nodo primario. Para esta clase, la cadena es "AppInstallation".

</dd> <dt>

[LastError](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-lasterror)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

[LastErrorDesc](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
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

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/EnterpriseModernAppManagement/AppInstallation".

</dd> <dt>

[ProgressStatus](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

[Estado](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-status)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
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

 

