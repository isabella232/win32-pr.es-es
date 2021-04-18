---
description: Representa la asociación entre los elementos administrados y sus capacidades.
ms.assetid: F083E6D2-CC74-4DAD-8FF7-3FE3CA4EEFFF
title: Msvm_ElementCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementCapabilities
- Msvm_ElementCapabilities.ManagedElement
- Msvm_ElementCapabilities.Capabilities
- Msvm_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d7602de569a51aec73130a4b5f4d3ba339cb29c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687845"
---
# <a name="msvm_elementcapabilities-class"></a>MSVM \_ ElementCapabilities (clase)

Representa la asociación entre los elementos administrados y sus capacidades.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementCapabilities : CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ ElementCapabilities** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ ElementCapabilities** tiene estas propiedades.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ capacidades de CIM**](/previous-versions//cc136806(v=vs.85))**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Objeto Capabilities asociado al elemento. Esta propiedad se hereda de [**\_ ElementCapabilities CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).

</dd> <dt>

**Características**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona información descriptiva acerca de las capacidades de. Esta propiedad se hereda de [**\_ ElementCapabilities CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).



| Value                                                                                                                                                                                                                       | Significado                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <dt>**Valor predeterminado**</dt> <dt>2</dt> </dl> | Las capacidades asociadas representan las funciones predeterminadas del elemento administrado.<br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <dt>**Actual**</dt> <dt>3</dt> </dl> | Las capacidades asociadas representan las capacidades actuales del elemento administrado.<br/> |



 

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**, **mín** . (1)
</dt> </dl>

Elemento administrado. Esta propiedad se hereda de [**\_ ElementCapabilities CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ ElementCapabilities** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_ELEMENTCAPABILITIES CIM**](cim-elementcapabilities.md)
</dt> <dt>

[**\_ELEMENTCAPABILITIES CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)
</dt> <dt>

[**MSVM \_ ElementCapabilities (V1)**](/previous-versions/windows/desktop/virtual/msvm-elementcapabilities)
</dt> </dl>

 

