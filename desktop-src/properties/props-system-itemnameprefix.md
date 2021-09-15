---
description: Prefijo de un elemento, que se usa para los mensajes de correo electrónico donde el asunto comienza con el prefijo &\# 0034; Re:&\# 0034;.
ms.assetid: 3c257edc-b7f7-498d-8347-0be4fca41023
title: System.ItemNamePrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf669dd867c8cf60046f226e33dae18f46060cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248126"
---
# <a name="systemitemnameprefix"></a>System.ItemNamePrefix

Prefijo de un elemento, que se usa para los mensajes de correo electrónico en los que el asunto comienza con el prefijo "Re:".

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemNamePrefix
   shellPKey = PKEY_ItemNamePrefix
   formatID = D7313FF1-A77A-401C-8C99-3DBDD68ADD36
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Observaciones

Los valores PKEY se definen en Propkey.h.

Si el elemento es un archivo, el valor de esta propiedad es VT \_ EMPTY. Si el elemento es un mensaje, el valor de esta propiedad son los prefijos de reenvío o respuesta (incluidos los dos puntos delimitadores, pero ningún espacio en blanco) o VT EMPTY si no hay ningún \_ prefijo.

Valores de ejemplo:



| System.ItemNamePrefix | System.ItemName  | System.ItemNameDisplay |
|-----------------------|------------------|------------------------|
| VT \_ EMPTY             | "Buen día"      | "Buen día"            |
| "Re:"                 | "Buen día"      | "Re: Great day"        |
| "Fwd: "               | "Presupuesto mensual" | "Fwd: Presupuesto mensual"  |
| VT \_ EMPTY             | accounts.xls     | accounts.xls           |



 

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

 

 
