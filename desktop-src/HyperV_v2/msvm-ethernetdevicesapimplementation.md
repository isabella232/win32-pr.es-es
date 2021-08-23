---
description: 'Msvm_EthernetDeviceSAPImplementation clase : representa una asociación entre un punto de acceso de servicio y el dispositivo lógico que lo implementa.'
ms.assetid: C0DDB199-AD97-4DD7-8056-BD6BD0CECFA8
title: Msvm_EthernetDeviceSAPImplementation clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetDeviceSAPImplementation
- Msvm_EthernetDeviceSAPImplementation.Antecedent
- Msvm_EthernetDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0cabf80b7e55513fc5fc31b744db8cbc973ccd15bcda170804c754850d65dbfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524985"
---
# <a name="msvm_ethernetdevicesapimplementation-class"></a>Clase Msvm \_ EthernetDeviceSAPImplementation

Representa una asociación entre un punto de acceso de servicio y el dispositivo lógico que lo implementa. La cardinalidad de esta asociación es de varios a varios. Más de un dispositivo lógico puede proporcionar un punto de acceso de servicio (SAP), que funciona conjuntamente. Cualquier dispositivo puede proporcionar más de un SAP. Cuando muchos dispositivos lógicos están asociados a un único SAP, se supone que estos elementos funcionan juntos para proporcionar el punto de acceso. Si existen implementaciones diferentes de un SAP, cada una de estas implementaciones daría lugar a instancias individuales del objeto de SAP. Estas instancias individuales tendrían asociaciones con las implementaciones únicas.

La sintaxis siguiente se Managed Object Format código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_EthernetPort REF Antecedent;
  Msvm_LANEndpoint REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ EthernetDeviceSAPImplementation** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ EthernetDeviceSAPImplementation** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Referencia a una clase derivada de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) que representa el dispositivo lógico.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ LANEndpoint**](msvm-lanendpoint.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Referencia a una instancia de la clase [**\_ Msvm LANEndpoint**](msvm-lanendpoint.md) que representa el SAP que usa **el antecedente**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

