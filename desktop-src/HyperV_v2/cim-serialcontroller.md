---
description: Describe las funcionalidades y la administración de un controlador serie.
ms.assetid: ce3e0424-4ab8-435d-a155-1164535b3b0d
title: CIM_SerialController (administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialController
- CIM_SerialController.Capabilities
- CIM_SerialController.CapabilityDescriptions
- CIM_SerialController.MaxBaudRate
- CIM_SerialController.Security
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6a438919674f805f59cb6e2cac6e76cb6367f03ce12fa2ceb0787527e56adb83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980835"
---
# <a name="cim_serialcontroller-class-hyper-v-management"></a>CIM_SerialController (administración de Hyper-V)

Describe las funcionalidades y la administración de un controlador serie.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_SerialController : CIM_Controller
{
  uint16 Capabilities[];
  string CapabilityDescriptions[];
  uint32 MaxBaudRate;
  uint16 Security;
};
```

## <a name="members"></a>Miembros

La **clase CIM \_ SerialController** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase CIM \_ SerialController** tiene estas propiedades.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Puertos serie DMTF \| \| 004.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SerialController**.**CapabilityDescriptions**")
</dt> </dl>

Compatibilidad de nivel de chip para el controlador serie. Esta propiedad describe el almacenamiento en búfer y otras funcionalidades del controlador serie que podrían ser inherentes al hardware del chip.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

**Compatible con XT/AT** (3)


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

**Compatible con 16450** (4)


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

**Compatible con 16550** (5)


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

**Compatible con 16550A** (6)


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

**Compatible con 8251** (160)


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

**Compatible con 8251FIFO** (161)


</dt> <dd></dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SerialController**.**Funcionalidades**")
</dt> </dl>

Matriz que contiene explicaciones más detalladas de las características del controlador serie en la **matriz Capabilities.** Los elementos de la **matriz CapabilityDescriptions** se correlacionan con los de la **matriz Capabilities.**

</dd> <dt>

**MaxBaudRate**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits por segundo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Puertos serie DMTF \| \| 004.6"), **PUnit** ("bit/segundo")
</dt> </dl>

Velocidad en baudios máxima, bits por segundo, que es compatible con el controlador serie.

</dd> <dt>

**Seguridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Puertos serie DMTF \| \| 004.9")
</dt> </dl>

Seguridad operativa del controlador.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Ninguno** (3)


</dt> <dd></dd> <dt>

<span id="External_Interface_Locked_Out"></span><span id="external_interface_locked_out"></span><span id="EXTERNAL_INTERFACE_LOCKED_OUT"></span>

**Interfaz externa bloqueada** (4)


</dt> <dd></dd> <dt>

<span id="External_Interface_Enabled"></span><span id="external_interface_enabled"></span><span id="EXTERNAL_INTERFACE_ENABLED"></span>

**Interfaz externa habilitada** (5)


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

**Omisión del** arranque (6)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controlador \_ CIM**](cim-controller.md)
</dt> </dl>

 

