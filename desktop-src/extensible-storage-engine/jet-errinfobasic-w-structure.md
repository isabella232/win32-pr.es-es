---
description: 'Más información acerca de: estructura de JET_ERRINFOBASIC_W'
title: Estructura de JET_ERRINFOBASIC_W
TOCTitle: JET_ERRINFOBASIC_W Structure
ms:assetid: fcc55cb7-718d-419a-a473-15e030c23abd
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475861(v=EXCHG.10)
ms:contentKeyID: 37033567
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 99be77326fe9e037430203bf9744e550e8495fe1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104003996"
---
# <a name="jet_errinfobasic_w-structure"></a>Estructura de JET_ERRINFOBASIC_W


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_errinfobasic_w-structure"></a>Estructura de JET_ERRINFOBASIC_W

La estructura **JET_ERRINFOBASIC_W** define los datos que se devuelven desde el método [JetGetErrorInfo ()](./jetgeterrorinfow-function.md) cuando se pasa el JET_ErrorInfoSpecificErr InfoLevel.

Nota: esta documentación se basa en una versión preliminar del motor de almacenamiento extensible. Esta información está sujeta a cambios.

```cpp
typedef struct { 
    unsigned long cbStruct; 
    JET_ERR errValue; 
    JET_ERRCAT errcatMostSpecific; 
    unsigned char rgCategoricalHierarchy[8]; 
    unsigned long lSourceLine; 
    WCHAR rgszSourceFile[64]; 
} JET_ERRINFOBASIC_W;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño de la estructura, en bytes. Debe establecerse en sizeof (JET_ERRINFOBASIC).

**errValue**

Valor de error que se evaluó, tal y como se pasa para el argumento *pvResult* a [JetGetErrorInfo ()](./jetgeterrorinfow-function.md).

**errcatMostSpecific**

[JET_ERRCAT](./jet-errcat.md) constante de nivel inferior que está asociada al error; es decir, la categoría de nivel de hoja de la jerarquía de categoría documentada en [JET_ERRCAT](./jet-errcat.md).

**rgCategoricalHierarchy \[ 8\]**

La jerarquía de categorías de error que está asociada al error. La posición 0 es el nivel más alto en la jerarquía de [JET_ERRCAT](./jet-errcat.md)y el resto son subcategorías hasta que se establece la categoría más específica, después de la cual se JET_errcatUnknownn todas las categorías.

**lSourceLine**

Reservado.

**rgszSourceFile \[ 64\]**

Reservado.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows 8 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>
