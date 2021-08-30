---
description: Representa una descripción de un formato de textura.
MS-HAID: vspixengine.PixEngineTextureFormatDesc
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura DesenlazingTextureFormatDesc
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 685DC746-544D-4ACB-AB1F-9FA62C5CF416
api_name:
- PixEngineTextureFormatDesc
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b868c1b248d2d2a37422acbb5cfe1ae3feede804
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622301"
---
# <a name="span-idvspixenginepixenginetextureformatdescspanpixenginetextureformatdesc-structure"></a><span id="vspixengine.pixenginetextureformatdesc"></span>Estructura DesenlazingTextureFormatDesc

Representa una descripción de un formato de textura.

## <a name="syntax"></a>Sintaxis


```C++
} PixEngineTextureFormatDesc;
```

## <a name="members"></a>Miembros

**dxgiFormat**  
Formato DXGI de la textura.

**dataFormat**  
Formato de datos de la textura.

**blockBytes**  
Número de bytes de un bloque de datos.

**blockHeight**  
Alto (ejemplos de número en el eje Y) del bloque.

**blockWidth**  
Ancho (número de muestras en el eje X) del bloque.

**channelX**  
Describe las propiedades del canal X. Para obtener más información, vea la estructura PixelEngineChannelDescription.

**channelY**  
Describe las propiedades del canal Y. Para obtener más información, vea la estructura PixelEngineChannelDescription.

**channelZ**  
Describe las propiedades del canal Z. Para obtener más información, vea la estructura PixelEngineChannelDescription.

**channelW**  
Describe las propiedades del canal W. Para obtener más información, vea la estructura PixelEngineChannelDescription.

**Swizzle**  
Describe el swzzle (intercambio de canales) aplicado al ejemplo.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



