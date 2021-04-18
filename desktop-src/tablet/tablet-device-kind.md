---
description: Indica el tipo de dispositivo de Tablet PC, como un lápiz, mouse o digitalizador táctil.
ms.assetid: 4cca1e09-99c0-4357-a6ef-159bc8d17d57
title: Enumeración TABLET_DEVICE_KIND
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
ms.openlocfilehash: 18f691a2fa909ef28059a4788f4f8b4e184a61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678486"
---
# <a name="tablet_device_kind-enumeration"></a>\_Enumeración de tipo de dispositivo de tableta \_

Indica el tipo de dispositivo de Tablet PC, como un lápiz, mouse o digitalizador táctil.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _TABLET_DEVICE_KIND { 
  TABLET_DEVICE_MOUSE  = 0,
  TABLET_DEVICE_PEN,
  TABLET_DEVICE_TOUCH
} TABLET_DEVICE_KIND;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**\_mouse del dispositivo de tableta gráfica \_**
</dt> <dd>

La tableta es un mouse. Esto incluye los paneles táctiles que se encuentran en muchos equipos portátiles.

</dd> <dt>

<span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**\_lápiz del dispositivo TABLET PC \_**
</dt> <dd>

La tableta emplea un lápiz y un digitalizador electromagnéticos.

</dd> <dt>

<span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**\_Touch del dispositivo de tableta \_**
</dt> <dd>

La tableta emplea un digitalizador con distinción de toque.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITablet2:: GetDeviceKind (método)**](itablet2-getdevicekind.md)
</dt> </dl>

 

 




