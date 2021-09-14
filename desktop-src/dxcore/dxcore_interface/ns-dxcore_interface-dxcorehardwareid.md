---
title: DXCoreHardwareID
description: Representa las partes del identificador de hardware pnP de un adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6882d9aa16bf72fb33f9a254a6434becb37f9cb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964599"
---
# <a name="dxcorehardwareid-structure"></a>DXCoreHardwareID (estructura)

Representa las partes del identificador de hardware pnP de un adaptador.

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

## <a name="members"></a>Members

### <a name="vendorid"></a>vendorId

Tipo: **uint32_t \***

El identificador PCI del proveedor de hardware del adaptador.

### <a name="deviceid"></a>deviceId

Tipo: **uint32_t \***

El identificador PCI del dispositivo de hardware del adaptador.

### <a name="subsysid"></a>subSysId

Tipo: **uint32_t \***

El identificador PCI del subsistema de hardware del adaptador.

### <a name="revision"></a>revision

Tipo: **uint32_t \***

El identificador PCI del número de revisión del adaptador.

## <a name="see-also"></a>Consulte también

[Referencia de DXCore,](../dxcore-reference.md) [uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)