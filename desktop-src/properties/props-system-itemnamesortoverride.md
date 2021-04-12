---
description: Esta cadena debe establecerse en la versión fonética del nombre para mostrar tal como se define en System. ItemNameDisplay en configuraciones regionales CJK (pinyin de CHS, Japonés JPN, hangul KOR, etc.).
ms.assetid: eb491644-bf59-4439-9e9b-bcafde619d66
title: System. ItemNameSortOverride
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79f9bb07eb15eb5d25fbfa1e95d4c0f80b35611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278018"
---
# <a name="systemitemnamesortoverride"></a>System. ItemNameSortOverride

Esta cadena debe establecerse en la versión fonética del nombre para mostrar tal como se define en System. ItemNameDisplay en configuraciones regionales CJK (pinyin de CHS, Japonés JPN, hangul KOR, etc.). El primer carácter de este campo también se utiliza para agrupar los nombres por firstLetter. Para la mayoría de los lenguajes que no sean CJK, no es necesario establecer este campo (en cuyo caso se usará System. ItemNameDisplay). Sin embargo, si es deseable invalidar la letra de agrupación (por ejemplo, para quitar los artículos iniciales como "a" y "el"), se puede proporcionar una cadena alternativa aquí.

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

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey. h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[Requerida](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[Numérico](./propdesc-schema-numberformat.md)
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

[Consulta](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
