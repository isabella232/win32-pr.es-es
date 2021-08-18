---
title: MDM_DeviceStatus_DeviceGuard01 clase
description: La empresa usa la clase \_ DeviceStatus DeviceGuard01 de MDM para realizar un seguimiento del inventario de dispositivos y consultar el estado de cumplimiento de estos dispositivos con sus \_ directivas empresariales.
ms.assetid: 267129f6-ec37-43ae-bba3-e21917012f27
keywords:
- MDM_DeviceStatus_DeviceGuard01 clase
- MDM_DeviceStatus_DeviceGuard01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_DeviceGuard01
- MDM_DeviceStatus_DeviceGuard01.InstanceID
- MDM_DeviceStatus_DeviceGuard01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccba37e5a7fef2890f7bae832153789795a0b1f8104e6cd0ab587940c704a3cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797075"
---
# <a name="mdm_devicestatus_deviceguard01-class"></a>Clase \_ DeviceStatus \_ DeviceGuard01 de MDM

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

La empresa usa la clase \_ DeviceStatus DeviceGuard01 de MDM para realizar un seguimiento del inventario de dispositivos y consultar el estado de cumplimiento de estos dispositivos con sus \_ directivas empresariales.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_DeviceGuard01
{
  string InstanceID;
  string ParentID;
  sint32 VirtualizationBasedSecurityHwReq;
  sint32 VirtualizationBasedSecurityStatus;
  sint32 LsaCfgCredGuardStatus;
};
```

## <a name="members"></a>Miembros

La **clase \_ DeviceStatus \_ DeviceGuard01** de MDM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ DeviceStatus \_ DeviceGuard01** de MDM tiene estas propiedades.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

[LsaCfgCredGuardStatus](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-lsacfgcredguardstatus)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

[VirtualizationBasedSecurityHwReq](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-virtualizationbasedsecurityhwreq)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[VirtualizationBasedSecurityStatus](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-virtualizationbasedsecuritystatus)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

