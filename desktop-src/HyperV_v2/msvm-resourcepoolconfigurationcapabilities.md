---
description: Describe las capacidades de la clase MSVM \_ ResourcePoolConfigurationService asociada.
ms.assetid: 3e6857f9-62a0-420b-8f1d-8aad685a7ff7
title: Msvm_ResourcePoolConfigurationCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationCapabilities
- Msvm_ResourcePoolConfigurationCapabilities.InstanceID
- Msvm_ResourcePoolConfigurationCapabilities.Caption
- Msvm_ResourcePoolConfigurationCapabilities.Description
- Msvm_ResourcePoolConfigurationCapabilities.ElementName
- Msvm_ResourcePoolConfigurationCapabilities.AsynchronousMethodsSupported
- Msvm_ResourcePoolConfigurationCapabilities.SynchronousMethodsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b70d9e84e2c85d4c5b702a638982df0b47d62193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910729"
---
# <a name="msvm_resourcepoolconfigurationcapabilities-class"></a>MSVM \_ ResourcePoolConfigurationCapabilities (clase)

Describe las capacidades de la clase [**MSVM \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) asociada. Los clientes pueden usar instancias de esta clase para determinar qué métodos se admiten de forma sincrónica o asincrónica. El mismo método no debe estar en ambas listas. Las implementaciones de método deben ser sincrónicas o asincrónicas.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ResourcePoolConfigurationCapabilities : CIM_Capabilities
{
  string InstanceID;
  string Caption = "Resource Pool Configuration Capabilities";
  string Description = "Microsoft Resource Pool Configuration Capabilities";
  string ElementName = "Resource Pool Configuration Capabilities";
  uint32 AsynchronousMethodsSupported[];
  uint32 SynchronousMethodsSupported[];
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ ResourcePoolConfigurationCapabilities** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ ResourcePoolConfigurationCapabilities** tiene estas propiedades.

<dl> <dt>

**AsynchronousMethodsSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una matriz de identificadores de método, cada uno de los cuales identifica un método de la clase [**MSVM \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) que la implementación admite de forma asincrónica.

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="CreatePool_is_supported"></span><span id="createpool_is_supported"></span><span id="CREATEPOOL_IS_SUPPORTED"></span>

**Se admite createpool** (32768)


</dt> <dd></dd> <dt>

<span id="ChangePoolResources_is_supported"></span><span id="changepoolresources_is_supported"></span><span id="CHANGEPOOLRESOURCES_IS_SUPPORTED"></span>

**Se admite ChangePoolResources** (32769)


</dt> <dd></dd> <dt>

<span id="ChangePoolSettings_is_supported"></span><span id="changepoolsettings_is_supported"></span><span id="CHANGEPOOLSETTINGS_IS_SUPPORTED"></span>

**Se admite ChangePoolSettings** (32770)


</dt> <dd></dd> <dt>

<span id="DeletePool_is_supported"></span><span id="deletepool_is_supported"></span><span id="DELETEPOOL_IS_SUPPORTED"></span>

**Se admite DeletePool** (32771)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Proveedor reservado** (32772.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "capacidades de configuración del grupo de recursos".

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "capacidades de configuración del grupo de recursos de Microsoft".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "capacidades de configuración del grupo de recursos".

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**SynchronousMethodsSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una matriz de identificadores de método, cada uno de los cuales identifica un método de la clase [**MSVM \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) que la implementación admite sincrónicamente.

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="CreatePool_is_supported"></span><span id="createpool_is_supported"></span><span id="CREATEPOOL_IS_SUPPORTED"></span>

**Se admite createpool** (32768)


</dt> <dd></dd> <dt>

<span id="ChangePoolResources_is_supported"></span><span id="changepoolresources_is_supported"></span><span id="CHANGEPOOLRESOURCES_IS_SUPPORTED"></span>

**Se admite ChangePoolResources** (32769)


</dt> <dd></dd> <dt>

<span id="ChangePoolSettings_is_supported"></span><span id="changepoolsettings_is_supported"></span><span id="CHANGEPOOLSETTINGS_IS_SUPPORTED"></span>

**Se admite ChangePoolSettings** (32770)


</dt> <dd></dd> <dt>

<span id="DeletePool_is_supported"></span><span id="deletepool_is_supported"></span><span id="DELETEPOOL_IS_SUPPORTED"></span>

**Se admite DeletePool** (32771)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Proveedor reservado** (32772.. 65535)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                                 |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

