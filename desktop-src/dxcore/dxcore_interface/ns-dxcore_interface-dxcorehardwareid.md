---
title: DXCoreHardwareID
description: Representa las partes de id. de hardware PnP de un adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 68cdb130dd6f0c0338e5b94da2f68c58f98bb91d404871e18ac82e817881117c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118632"
---
# <a name="dxcorehardwareid-structure"></a>DXCoreHardwareID (estructura)

Representa las partes de id. de hardware PnP de un adaptador.

## <a name="syntax"></a>Sintaxis

```cpp
struct DXCoreHardwareID
{
  uint32_t vendorID;
  uint32_t deviceID;
  uint32_t subSysID;
  uint32_t revision;
};
```

## <a name="members"></a>Miembros

### <a name="vendorid"></a>vendorId

Tipo: **uint32_t \***

El id. de PCI del proveedor de hardware del adaptador.

### <a name="deviceid"></a>deviceId

Tipo: **uint32_t \***

El identificador PCI del dispositivo de hardware del adaptador.

### <a name="subsysid"></a>subSysId

Tipo: **uint32_t \***

El identificador PCI del subsistema de hardware del adaptador.

### <a name="revision"></a>revision

Tipo: **uint32_t \***

El identificador PCI del número de revisión del adaptador.

## <a name="see-also"></a>Vea también

[Referencia de DXCore,](../dxcore-reference.md) [uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)