---
description: 'Más información sobre: JET_ERRINFOBASIC_W estructura'
title: JET_ERRINFOBASIC_W estructura
TOCTitle: JET_ERRINFOBASIC_W Structure
ms:assetid: fcc55cb7-718d-419a-a473-15e030c23abd
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475861(v=EXCHG.10)
ms:contentKeyID: 37033567
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 7652bf39f620322d1c5ebc4b806438d182fd7c64
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477171"
---
# <a name="jet_errinfobasic_w-structure"></a>JET_ERRINFOBASIC_W estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_errinfobasic_w-structure"></a>JET_ERRINFOBASIC_W estructura

La **JET_ERRINFOBASIC_W** define los datos que se devuelven desde el método [JetGetErrorInfo()](./jetgeterrorinfow-function.md) cuando se pasa JET_ErrorInfoSpecificErr InfoLevel.

Nota: Esta documentación se basa en una versión preliminar de Extensible Storage Engine. Esta información está sujeta a cambios.

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

Tamaño de la estructura, en bytes. Debe establecerse en sizeof( JET_ERRINFOBASIC ).

**errValue**

Valor de error que se evaluó, tal como se pasó para el *argumento pvResult* a [JetGetErrorInfo().](./jetgeterrorinfow-function.md)

**errcatMostSpecific**

La constante de nivel [JET_ERRCAT](./jet-errcat.md) que está asociada al error; es decir, la categoría de nivel hoja de la jerarquía de categorías documentada [en JET_ERRCAT](./jet-errcat.md).

**rgCategoricalHierarchy \[ 8\]**

Jerarquía de categorías de error asociadas al error. La posición 0 es el nivel más alto de la jerarquía de [JET_ERRCAT](./jet-errcat.md)y el resto son subcategorías hasta que se establece la categoría más específica, después de la cual se JET_errcatUnknown.

**lSourceLine**

Reservado.

**rgszSourceFile \[ 64\]**

Reservado.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows 8.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows 8 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 

