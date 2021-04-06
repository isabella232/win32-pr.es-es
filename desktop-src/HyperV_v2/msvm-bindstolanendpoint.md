---
description: Esta asociación establece un punto de acceso al servicio (SAP) como solicitante de servicios de protocolo desde un punto de conexión de protocolo.
ms.assetid: 14edefd8-d59b-4925-8b78-a979fb9a975f
title: Msvm_BindsToLANEndpoint (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BindsToLANEndpoint
- Msvm_BindsToLANEndpoint.Antecedent
- Msvm_BindsToLANEndpoint.Dependent
- Msvm_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c2fa01c8e9e7df40a2907e6e43a9cb4b507a53d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002788"
---
# <a name="msvm_bindstolanendpoint-class"></a>MSVM \_ BindsToLANEndpoint (clase)

Esta asociación establece un punto de acceso al servicio (SAP) como solicitante de servicios de protocolo desde un punto de conexión de protocolo. Normalmente, esta asociación se ejecuta entre SAP y los puntos de conexión en un único sistema. Dado que un punto de conexión de protocolo es un tipo de SAP, este enlace se puede usar para establecer una capa de dos protocolos, con la capa superior representada por el **dependiente** y la capa inferior representada por el **antecedente**.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BindsToLANEndpoint : CIM_BindsToLANEndpoint
{
  Msvm_LANEndpoint  REF Antecedent;
  Msvm_VLANEndpoint REF Dependent;
  uint16                FrameType;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ BindsToLANEndpoint** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ BindsToLANEndpoint** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ LANEndpoint**](msvm-lanendpoint.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Una referencia a una clase [**MSVM \_ LANEndpoint**](msvm-lanendpoint.md) que representa el puerto del conmutador. Esta propiedad se hereda de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ VLANEndpoint**](msvm-vlanendpoint.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")
</dt> </dl>

Una referencia a [**MSVM \_ VLANEndpoint**](msvm-vlanendpoint.md) asociada con el puerto del conmutador. Esta propiedad se hereda de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**FrameType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe el método de tramas para el punto de conexión o SAP de nivel superior que está enlazado al punto de conexión de LAN. Esta propiedad se hereda de **CIM \_ BindsToLANEndpoint** y siempre está establecida en **null**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

