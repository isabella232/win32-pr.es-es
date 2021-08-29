---
description: Representa la asociación entre los elementos administrados y sus funcionalidades.
ms.assetid: F083E6D2-CC74-4DAD-8FF7-3FE3CA4EEFFF
title: Msvm_ElementCapabilities clase
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
ms.openlocfilehash: 56b0180e7f6fe4b7bb80129006e9290c23b38f2c5c10beaaa6377096b243b275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148449"
---
# <a name="msvm_elementcapabilities-class"></a>Clase ElementCapabilities de Msvm \_

Representa la asociación entre los elementos administrados y sus funcionalidades.

La sintaxis siguiente se Managed Object Format código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

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

La **clase \_ ElementCapabilities de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ElementCapabilities de Msvm** tiene estas propiedades.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Funcionalidades cim \_**](/previous-versions//cc136806(v=vs.85))**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Objeto capabilities asociado al elemento. Esta propiedad se hereda del [**elemento \_ CIMCapabilities.**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)

</dd> <dt>

**Características**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona información descriptiva sobre las funcionalidades. Esta propiedad se hereda del [**elemento \_ CIMCapabilities.**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)



| Valor                                                                                                                                                                                                                       | Significado                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <dt>**Valor**</dt> <dt>predeterminado 2</dt> </dl> | Las funcionalidades asociadas representan las funcionalidades predeterminadas del elemento administrado.<br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <dt>**Actual**</dt> <dt>3</dt> </dl> | Las funcionalidades asociadas representan las funcionalidades actuales del elemento administrado.<br/> |



 

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Key**, **Min** ( 1 )
</dt> </dl>

Elemento administrado. Esta propiedad se hereda del [**elemento \_ CIMCapabilities.**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a la **clase \_ ElementCapabilities de Msvm** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ ElementCapabilities**](cim-elementcapabilities.md)
</dt> <dt>

[**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)
</dt> <dt>

[**ElementCapabilities de Msvm \_ (V1)**](/previous-versions/windows/desktop/virtual/msvm-elementcapabilities)
</dt> </dl>

 

