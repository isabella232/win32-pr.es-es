---
description: Representa una descripción de un segmento de textura.
MS-HAID: vspixengine.PixEngineTextureSliceDescriptor
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura PixEngineTextureSliceDescriptor
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
ms.openlocfilehash: 5b80a23a5ec3340b775c314f66651926743249ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152156"
---
# <a name="span-idvspixenginepixenginetextureslicedescriptorspanpixenginetextureslicedescriptor-structure"></a><span id="vspixengine.pixenginetextureslicedescriptor"></span>Estructura PixEngineTextureSliceDescriptor

Representa una descripción de un segmento de textura.

## <a name="syntax"></a>Sintaxis


```C++
} PixEngineTextureSliceDescriptor;
```

## <a name="members"></a>Miembros

**width**  
El ancho (número de muestras en el eje X) del segmento.

**height**  
Alto (número de muestras en el eje Y) del segmento.

**blockRowBytes**  
El número de bytes por fila en cada bloque.

**offset**  
Desplazamiento del segmento dentro de toda la textura.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



