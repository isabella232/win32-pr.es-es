---
description: Esta cadena debe establecerse en la versión fonética del nombre para mostrar tal como se define en System.ItemNameDisplay en las configuraciones regionales de CJK (CHS Pinyin, JPN Hiragana, KOR Hangul, etc.).
ms.assetid: eb491644-bf59-4439-9e9b-bcafde619d66
title: System.ItemNameSortOverride
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64c555007ae7bd2a0c7ca5f16e6e3ad26449942b2c7031b81a03317d0d6212a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117865888"
---
# <a name="systemitemnamesortoverride"></a>System.ItemNameSortOverride

Esta cadena debe establecerse en la versión fonética del nombre para mostrar tal como se define en System.ItemNameDisplay en las configuraciones regionales de CJK (CHS Pinyin, JPN Hiragana, KOR Hangul, etc.). El primer carácter de este campo también se usa para agrupar nombres por primera vez. Para la mayoría de los lenguajes que no son CJK, no es necesario establecer este campo (en cuyo caso se usará System.ItemNameDisplay). Sin embargo, si es conveniente invalidar la letra de agrupación (por ejemplo, para quitar artículos iniciales como "a" y "the"), aquí se puede proporcionar una cadena alternativa.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8

```
propertyDescription
   name = System.ItemNameSortOverride
   shellPKey = PKEY_ItemNameSortOverride
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Comentarios

Los valores PKEY se definen en Propkey.h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
