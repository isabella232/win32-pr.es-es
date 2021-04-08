---
title: MDM_DeviceStatus_UAC01 (clase)
description: '\_ \_ La empresa usa la clase UAC01 de DEVICESTATUS de MDM para consultar el estado de UAC de los dispositivos con sus directivas de empresa.'
ms.assetid: fb1ca1bb-229e-4eaa-a1e3-e790c1dab760
keywords:
- MDM_DeviceStatus_UAC01 (clase)
- MDM_DeviceStatus_UAC01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_UAC01
- MDM_DeviceStatus_UAC01.InstanceID
- MDM_DeviceStatus_UAC01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eecba42cd97bee660f66570e7f96c1ab2799f85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803115"
---
# <a name="mdm_devicestatus_uac01-class"></a>\_Clase UAC01 DeviceStatus de MDM \_

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

La empresa usa la clase **\_ \_ UAC01 de DeviceStatus de MDM** para consultar el estado de UAC de los dispositivos con sus directivas de empresa.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_UAC01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a>Miembros

La **clase \_ \_ UAC01 de MDM DeviceStatus** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ \_ UAC01 de MDM DeviceStatus** tiene estas propiedades.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nodo para la consulta de UAC.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/DeviceStatus".

</dd> <dt>

[Estado](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | Dmmap de MDM raíz de \\ cimv2 \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

