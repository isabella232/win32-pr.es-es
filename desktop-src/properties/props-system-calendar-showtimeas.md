---
description: Indica el estado del asistente durante el evento. El usuario puede elegir establecer el estado como disponible, ocupado, provisional o fuera de la oficina.
ms.assetid: ce2a1ab8-2937-446e-ac84-313649a4134d
title: System. Calendar. ShowTimeAs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a5766f459e0280a7c9397b513115c0f0ae9e94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696820"
---
# <a name="systemcalendarshowtimeas"></a>System. Calendar. ShowTimeAs

Indica el estado del asistente durante el evento. El usuario puede elegir establecer el estado como disponible, ocupado, provisional o fuera de la oficina.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Calendar.ShowTimeAs
   shellPKey = PKEY_Calendar_ShowTimeAs
   formatID = 5BF396D4-5EB2-466F-BDE9-2FB3F2361D6E
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Free
            value = 0
            text = Free
            defineToken = CALENDAR_SHOWTIMEAS_FREE
         enum
            name = Tentative
            value = 1
            text = Tentative
            defineToken = CALENDAR_SHOWTIMEAS_TENTATIVE
         enum
            name = Busy
            value = 2
            text = Busy
            defineToken = CALENDAR_SHOWTIMEAS_BUSY
         enum
            name = OOF
            value = 3
            text = OOF
            defineToken = CALENDAR_SHOWTIMEAS_OOF
            mnemonics = Out of Office
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Calendar.ShowTimeAs
   shellPKey = PKEY_Calendar_ShowTimeAs
   formatID = 5BF396D4-5EB2-466F-BDE9-2FB3F2361D6E
   propID = 100
   SearchInfo
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Free
            defineName = CALENDAR_SHOWTIMEAS_FREE
         enum
            value = 1
            text = Tentative
            defineName = CALENDAR_SHOWTIMEAS_TENTATIVE
         enum
            value = 2
            text = Busy
            defineName = CALENDAR_SHOWTIMEAS_BUSY
         enum
            value = 3
            text = OOF
            defineName = CALENDAR_SHOWTIMEAS_OOF
            mnemonics = Out of Office
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

 

 
