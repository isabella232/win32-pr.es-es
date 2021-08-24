---
description: Indica el tipo de dispositivo de tableta, como un lápiz, un digitalizador táctil o de mouse.
ms.assetid: 4cca1e09-99c0-4357-a6ef-159bc8d17d57
title: TABLET_DEVICE_KIND enumeración
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_DEVICE_KIND
api_type:
- NA
api_location: ''
ms.openlocfilehash: 784e2393f5470f8abd966ca6dbdce3ac9d9bff734f1245ebd0ef169180c62d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820185"
---
# <a name="tablet_device_kind-enumeration"></a>Enumeración TABLET \_ DEVICE \_ KIND

Indica el tipo de dispositivo de tableta, como un lápiz, un digitalizador táctil o de mouse.

## <a name="syntax"></a>Syntax


```C++
typedef enum _TABLET_DEVICE_KIND { 
  TABLET_DEVICE_MOUSE  = 0,
  TABLET_DEVICE_PEN,
  TABLET_DEVICE_TOUCH
} TABLET_DEVICE_KIND;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**TABLET \_ DEVICE \_ MOUSE**
</dt> <dd>

La tableta es un mouse. Esto incluye los dispositivos táctiles que se encuentran en muchos equipos portátiles.

</dd> <dt>

<span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**LÁPIZ \_ DEL DISPOSITIVO DE \_ TABLETA**
</dt> <dd>

La tableta usa un lápiz y un digitalizador.

</dd> <dt>

<span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**TABLET \_ DEVICE \_ TOUCH**
</dt> <dd>

La tableta usa un digitalizador táctil.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITablet2::GetDeviceKind (Método)**](itablet2-getdevicekind.md)
</dt> </dl>

 

 




