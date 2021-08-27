---
description: Representa una descripción de un segmento de textura.
MS-HAID: vspixengine.PixEngineTextureSliceDescriptor
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura De TextoDeScriptor de LaureSlice
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
ms.openlocfilehash: b10d66a7843198f86eeaebcf8f49b13abdd8c100
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625551"
---
# <a name="span-idvspixenginepixenginetextureslicedescriptorspanpixenginetextureslicedescriptor-structure"></a><span id="vspixengine.pixenginetextureslicedescriptor"></span>Estructura Desscriptor deEngineEngineTextureSlice

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

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



