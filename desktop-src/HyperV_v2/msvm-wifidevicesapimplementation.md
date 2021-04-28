---
description: 'Msvm_WiFiDeviceSAPImplementation clase : asociación entre un punto de acceso de servicio (SAP) y cómo se implementa.'
ms.assetid: d1d99299-f2d9-4025-a48d-cf8180f2f7af
title: Msvm_WiFiDeviceSAPImplementation clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiDeviceSAPImplementation
- Msvm_WiFiDeviceSAPImplementation.Antecedent
- Msvm_WiFiDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 99826ce3a37e19867cef1a6ddf276f5136b21a3d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109253"
---
# <a name="msvm_wifidevicesapimplementation-class"></a>Clase Msvm \_ WiFiDeviceSAPImplementation

Asociación entre un punto de acceso de servicio (SAP) y cómo se implementa. La cardinalidad de esta asociación es de varios a varios. Un SAP se puede proporcionar mediante más de un dispositivo lógico, que funciona conjuntamente. Cualquier dispositivo puede proporcionar más de un SAP. Cuando muchos dispositivos lógicos están asociados a un único SAP, se supone que estos elementos funcionan juntos para proporcionar el punto de acceso. Si existen implementaciones diferentes de un SAP, cada una de estas implementaciones daría como resultado instancias individuales del objeto de SAP. Estas instancias individuales tendrían entonces asociaciones con las implementaciones únicas.

La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  Msvm_WiFiPort     REF Antecedent;
  Msvm_WiFiEndpoint REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase \_ WiFiDeviceSAPImplementation de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ WiFiDeviceSAPImplementation** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ WiFiPort**](msvm-wifiport.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Instancia de la [**clase \_ WiFiPort de Msvm**](msvm-wifiport.md) que representa el dispositivo lógico.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ WiFiEndpoint**](msvm-wifiendpoint.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidar**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Instancia de la clase [**\_ WiFiEndpoint de Msvm**](msvm-wifiendpoint.md) que representa el punto de acceso de servicio implementado mediante el dispositivo lógico.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8 solo \[ aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

