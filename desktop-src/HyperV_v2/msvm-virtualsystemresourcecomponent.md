---
description: Representa un servicio de dispositivo virtual de Microsoft Windows plataforma Hyper-V.
ms.assetid: 865D83E1-0FC6-4F96-94BB-AA5116890127
title: Msvm_VirtualSystemResourceComponent clase
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
ms.openlocfilehash: 0758858e9e45066cdfaddf36616c7861bbae914b12e3698665f8650c6c57d67c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340175"
---
# <a name="msvm_virtualsystemresourcecomponent-class"></a>Clase Msvm \_ VirtualSystemResourceComponent

Representa un servicio de dispositivo virtual de Microsoft Windows plataforma Hyper-V.

La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.

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

La **clase Msvm \_ VirtualSystemResourceComponent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ VirtualSystemResourceComponent** tiene estas propiedades.

<dl> <dt>

**AdditionalClassNames**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de cadenas que contiene clases adicionales que no son de asociación que esta instancia de **Msvm \_ VirtualSystemResourceComponent** ha presentado. Estas clases no deben derivar de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ni [**de \_ ResourceAllocationSettingData de CIM.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Clsid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

GUID que representa el identificador de clase del objeto COM del servicio. Esta propiedad se hereda de [**Msvm \_ VirtualizationComponent.**](msvm-virtualizationcomponent.md)

</dd> <dt>

**Contexto**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Contexto en el que se ejecutará el objeto recién creado. Este valor se pasa en el *parámetro dwClsContext* a [**CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) Esta propiedad se hereda de [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)y siempre se establece en 1.

</dd> <dt>

**Habilitado**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**True** si esta instancia está habilitada y se puede usar para completar las solicitudes de cliente; de lo contrario, **False**. Esta propiedad se hereda de [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)y siempre se establece en **True.**

</dd> <dt>

**HotAdd**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**True** si esta instancia se puede agregar en caliente a una máquina virtual; de lo contrario, **False**. El valor predeterminado es **False**.

</dd> <dt>

**HotRemove**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**True** si esta instancia se puede quitar en caliente de una máquina virtual; de lo contrario, **False**. El valor predeterminado es **False**.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Cadena neutra del idioma que identifica de forma única el servicio. Se recomienda el formato siguiente para evitar conflictos de nomenclatura: "versión del \| componente \| de proveedor". Por ejemplo, este nombre representa la versión 1.0 del componente de puerto de red emulado de Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| V1.0". Esta propiedad se hereda de [**Msvm \_ VirtualizationComponent.**](msvm-virtualizationcomponent.md)

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Relación del objeto WMI que se describe aquí con el dispositivo virtual.



| Value                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_Not_Changeable_"></span><span id="_not_changeable_"></span><span id="_NOT_CHANGEABLE_"></span><dl> <dt>**"No modificable"**</dt> <dt>0</dt> </dl> |                                                                                                                                                                                                                |
| <span id="_Singleton_"></span><span id="_singleton_"></span><span id="_SINGLETON_"></span><dl> <dt>**"Singleton"**</dt> <dt>1</dt> </dl>                     | Singleton es un objeto WMI de nivel superior que está asociado 1:1 con un dispositivo virtual y solo puede existir una vez por máquina virtual. Este es el valor predeterminado.<br/>                                                  |
| <span id="_MultiInstance_"></span><span id="_multiinstance_"></span><span id="_MULTIINSTANCE_"></span><dl> <dt>**"MultiInstance"**</dt> <dt>2</dt> </dl>     | MultiInstance es un objeto WMI de nivel superior que puede existir varias veces por máquina virtual y está asociado 1:1 con un dispositivo virtual.<br/>                                                                    |
| <span id="_Subdevice_"></span><span id="_subdevice_"></span><span id="_SUBDEVICE_"></span><dl> <dt>**"Subdevice"**</dt> <dt>3</dt> </dl>                     | El subdispositivo es un objeto WMI que no tiene referencia primaria, pero que solo se controla mediante un dispositivo virtual que solo puede existir una vez por máquina virtual. Sin embargo, el objeto WMI puede existir varias veces.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase \_ VirtualSystemResourceComponent de Msvm** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Fin de compatibilidad de cliente<br/>    | Windows 8.1<br/>                                                                                  |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ VirtualizationComponent**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)
</dt> </dl>

 

