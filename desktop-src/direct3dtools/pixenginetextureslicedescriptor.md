---
description: Representa una descripción de un segmento de textura.
MS-HAID: vspixengine.PixEngineTextureSliceDescriptor
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura DeScriptor deEngineEngineTextureSlice
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1A183AFB-0BEF-4474-A60C-DBCFA4B34604
api_name:
- PixEngineTextureSliceDescriptor
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 915ef0158ca4c38eb6f9bbfe7bd3f1baf400b42a37b8f300e3f042bd610204c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119299"
---
# <a name="span-idvspixenginepixenginetextureslicedescriptorspanpixenginetextureslicedescriptor-structure"></a><span id="vspixengine.pixenginetextureslicedescriptor"></span>Estructura Desscriptor deEngineTextureSlice

Representa una descripción de un segmento de textura.

## <a name="syntax"></a>Sintaxis


```C++
} PixEngineTextureSliceDescriptor;
```

## <a name="members"></a>Miembros

**width**  
Ancho (número de muestras en el eje X) del segmento.

**height**  
Alto (número de muestras en el eje Y) del segmento.

**blockRowBytes**  
Número de bytes por fila de cada bloque.

**offset**  
Desplazamiento del segmento dentro de toda la textura.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



