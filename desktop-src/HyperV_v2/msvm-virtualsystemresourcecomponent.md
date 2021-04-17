---
description: Representa un servicio de dispositivo virtual de la plataforma Hyper-V de Microsoft Windows.
ms.assetid: 865D83E1-0FC6-4F96-94BB-AA5116890127
title: Msvm_VirtualSystemResourceComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceComponent
- Msvm_VirtualSystemResourceComponent.Name
- Msvm_VirtualSystemResourceComponent.CLSID
- Msvm_VirtualSystemResourceComponent.Context
- Msvm_VirtualSystemResourceComponent.Enabled
- Msvm_VirtualSystemResourceComponent.AdditionalClassNames
- Msvm_VirtualSystemResourceComponent.Type
- Msvm_VirtualSystemResourceComponent.HotAdd
- Msvm_VirtualSystemResourceComponent.HotRemove
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 81c2d31a6497325ac77003ded266333518de890a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666325"
---
# <a name="msvm_virtualsystemresourcecomponent-class"></a>MSVM \_ VirtualSystemResourceComponent (clase)

Representa un servicio de dispositivo virtual de la plataforma Hyper-V de Microsoft Windows.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
class Msvm_VirtualSystemResourceComponent : Msvm_VirtualizationComponent
{
  string  Name;
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  AdditionalClassNames[];
  uint16  Type = 1;
  boolean HotAdd = False;
  boolean HotRemove = False;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ VirtualSystemResourceComponent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ VirtualSystemResourceComponent** tiene estas propiedades.

<dl> <dt>

**AdditionalClassNames**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de cadenas que contiene las clases no asociadas adicionales expuestas por esta instancia de **\_ VirtualSystemResourceComponent de MSVM** . Estas clases deben derivarse de no tener ningún [**\_ desResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ni de CIM.

</dd> <dt>

**CLSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

GUID que representa el identificador de clase del objeto COM del servicio. Esta propiedad se hereda de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).

</dd> <dt>

**Contexto**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Contexto en el que se ejecutará el objeto recién creado. Este valor se pasa en el parámetro *dwClsContext* a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Esta propiedad se hereda de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)y siempre está establecida en 1.

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**True** si esta instancia está habilitada y se puede usar para completar las solicitudes de cliente; en caso contrario, **false**. Esta propiedad se hereda de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)y siempre se establece en **true**.

</dd> <dt>

**HotAdd**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**True** si esta instancia se puede Agregar en caliente a una máquina virtual; en caso contrario, **false**. El valor predeterminado es **False**.

</dd> <dt>

**HotRemove**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**True** si esta instancia se puede quitar en caliente de una máquina virtual; en caso contrario, **false**. El valor predeterminado es **False**.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Cadena independiente del lenguaje que identifica de forma única el servicio. Se sugiere el siguiente formato para evitar conflictos de nomenclatura: " \| versión del componente del proveedor \| ". Por ejemplo, este nombre representa la versión 1,0 del componente de puerto de red emulado de Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| v 1.0". Esta propiedad se hereda de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La relación del objeto WMI que se describe aquí con el dispositivo virtual.



| Value                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_Not_Changeable_"></span><span id="_not_changeable_"></span><span id="_NOT_CHANGEABLE_"></span><dl> <dt>**"No modificable"**</dt> <dt>0</dt> </dl> |                                                                                                                                                                                                                |
| <span id="_Singleton_"></span><span id="_singleton_"></span><span id="_SINGLETON_"></span><dl> <dt>**"Singleton"**</dt> <dt>1</dt> </dl>                     | Singleton es un objeto WMI de nivel superior que está vinculado a 1:1 con un dispositivo virtual y solo puede existir una vez por cada máquina virtual. Este es el valor predeterminado.<br/>                                                  |
| <span id="_MultiInstance_"></span><span id="_multiinstance_"></span><span id="_MULTIINSTANCE_"></span><dl> <dt>**"Multiinstancia"**</dt> <dt>2</dt> </dl>     | Multiinstancia es un objeto WMI de nivel superior que puede existir varias veces por máquina virtual y que está vinculado a 1:1 con un dispositivo virtual.<br/>                                                                    |
| <span id="_Subdevice_"></span><span id="_subdevice_"></span><span id="_SUBDEVICE_"></span><dl> <dt>**"Subdispositivo"**</dt> <dt>3</dt> </dl>                     | El subdispositivo es un objeto WMI que no tiene referencia primaria pero que solo está controlado por un único dispositivo virtual que solo puede existir una vez por cada máquina virtual. Aunque el objeto WMI puede existir varias veces.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ VirtualSystemResourceComponent** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Fin de compatibilidad de cliente<br/>    | Windows 8.1<br/>                                                                                  |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ VirtualizationComponent**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)
</dt> </dl>

 

