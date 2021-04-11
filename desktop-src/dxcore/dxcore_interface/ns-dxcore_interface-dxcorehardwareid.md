---
title: DXCoreHardwareID
description: Representa las partes de identificador de hardware de PnP para un adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6882d9aa16bf72fb33f9a254a6434becb37f9cb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149339"
---
# <a name="dxcorehardwareid-structure"></a>Estructura DXCoreHardwareID

Representa las partes de identificador de hardware de PnP para un adaptador.

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

IDENTIFICADOR de PCI del proveedor de hardware del adaptador.

### <a name="deviceid"></a>deviceId

Tipo: **uint32_t \***

IDENTIFICADOR de PCI del dispositivo de hardware del adaptador.

### <a name="subsysid"></a>subSysId

Tipo: **uint32_t \***

IDENTIFICADOR de PCI del subsistema de hardware del adaptador.

### <a name="revision"></a>revision

Tipo: **uint32_t \***

IDENTIFICADOR de PCI del número de revisión del adaptador.

## <a name="see-also"></a>Vea también

[Referencia de DXCore](../dxcore-reference.md), [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md)