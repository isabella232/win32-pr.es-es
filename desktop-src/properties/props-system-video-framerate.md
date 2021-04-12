---
description: Indica la velocidad de fotogramas de la secuencia de vídeo, en fotogramas por 1000 segundos.
ms.assetid: cd5a2ae0-43ef-44e4-aa70-bca33baf2a56
title: System. video. velocidad de fotogramas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcbdee7991186621a9d636e2072cecafc70176d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277640"
---
# <a name="systemvideoframerate"></a>System. video. velocidad de fotogramas

Indica la velocidad de fotogramas de la secuencia de vídeo, en fotogramas por 1000 segundos.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Video.FrameRate
   shellPKey = PKEY_Video_FrameRate
   formatID = 64440491-4C8B-11D1-8B70-080036B11A03
   propID = 6
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Video.FrameRate
   shellPKey = PKEY_Video_FrameRate
   formatID = 64440491-4C8B-11D1-8B70-080036B11A03
   propID = 6
   SearchInfo
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="remarks"></a>Observaciones

Para ayudar a reducir el error de truncamiento, esta propiedad no utiliza la medida de velocidad de fotogramas estándar de fotogramas por segundo (FPS). En su lugar, esta propiedad mide la velocidad de fotogramas como fotogramas por 1000 segundos (FPS multiplicado por 1000). Por ejemplo, [System. video. fotogramas]() expresaría una velocidad de fotogramas de 29,97 fps como valor entero de 29970.

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

 

 
