---
description: La clase NIC HWConfig \_ es la clase de tipo de evento para los eventos de configuración de tarjetas de interfaz de red. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: e544a27b-17f8-402c-9c92-578cf2a38ca8
title: HWConfig_NIC clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_NIC
- HWConfig_NIC.NICName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1d9b82f8a97c1ca47734b5bb0a1db09167510978c53f86870df01f2acc59b2ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394729"
---
# <a name="hwconfig_nic-class"></a>HwConfig \_ NIC (clase)

La **clase \_ NIC HWConfig** es la clase de tipo de evento para los eventos de configuración de tarjetas de interfaz de red.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(13), EventTypeName("NIC")]
class HWConfig_NIC : HWConfig
{
  string NICName;
};
```

## <a name="members"></a>Miembros

La **clase \_ NIC HWConfig** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ NIC HWConfig** tiene estas propiedades.

<dl> <dt>

NICName
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Nombre de la tarjeta de interfaz de red.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**HWConfig**](hwconfig.md)
</dt> </dl>

 

 




