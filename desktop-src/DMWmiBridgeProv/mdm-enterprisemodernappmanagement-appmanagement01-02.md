---
title: MDM_EnterpriseModernAppManagement_AppManagement01_02 (clase)
description: La \_ clase EnterpriseModernAppManagement \_ AppManagement01 \_ 02 de MDM especifica si desea bloquear la actualización de una aplicación específica a través de actualizaciones automáticas.
ms.assetid: b018f61a-2458-4c1a-b75c-6ca5eebb2977
keywords:
- MDM_EnterpriseModernAppManagement_AppManagement01_02 (clase)
- MDM_EnterpriseModernAppManagement_AppManagement01_02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01_02
- MDM_EnterpriseModernAppManagement_AppManagement01_02.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01_02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11441e8700d10bc7b0d5bebd31c002802a857417
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491951"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01_02-class"></a>\_Clase EnterpriseModernAppManagement \_ AppManagement01 \_ 02 de MDM

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

La **clase \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02 de MDM** especifica si desea bloquear la actualización de una aplicación específica a través de actualizaciones automáticas.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01_02
{
  string InstanceID;
  string ParentID;
  sint32 DoNotUpdate;
};
```

## <a name="members"></a>Miembros

La **clase \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02 de MDM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02 de MDM** tiene estas propiedades.

<dl> <dt>

[DoNotUpdate](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-donotupdate)
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

Identifica el nombre del nodo primario. Para esta clase, la cadena es la instancia del nombre de familia del paquete.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID*".

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

 

