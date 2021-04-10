---
description: Representa una descripción de un formato de textura.
MS-HAID: vspixengine.PixEngineTextureFormatDesc
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura PixEngineTextureFormatDesc
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
ms.openlocfilehash: 960186f0c28be88805c1df65f1a517c4ce4a4c64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997889"
---
# <a name="span-idvspixenginepixenginetextureformatdescspanpixenginetextureformatdesc-structure"></a><span id="vspixengine.pixenginetextureformatdesc"></span>Estructura PixEngineTextureFormatDesc

Representa una descripción de un formato de textura.

## <a name="syntax"></a>Sintaxis


```C++
} PixEngineTextureFormatDesc;
```

## <a name="members"></a>Miembros

**dxgiFormat**  
Formato de DXGI de la textura.

**dataFormat**  
Formato de datos de la textura.

**blockBytes**  
El número de bytes en un bloque de datos.

**blockHeight**  
El alto (número de muestras en el eje Y) del bloque.

**blockWidth**  
El ancho (número de muestras en el eje X) del bloque.

**channelX**  
Describe las propiedades del canal X. Para obtener más información, vea la estructura PixEngineChannelDescription.

**canaly**  
Describe las propiedades del canal Y. Para obtener más información, vea la estructura PixEngineChannelDescription.

**channelZ**  
Describe las propiedades del canal Z. Para obtener más información, vea la estructura PixEngineChannelDescription.

**channelW**  
Describe las propiedades del canal W. Para obtener más información, vea la estructura PixEngineChannelDescription.

**swizzle**  
Describe la swizzle (intercambio de canales) aplicada al ejemplo.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



