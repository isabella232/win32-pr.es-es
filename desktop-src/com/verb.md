---
title: Verbo
description: Especifica los verbos que se registrarán para una aplicación.
ms.assetid: bfcad36d-a52a-4117-bf0b-6135b197a7ee
keywords:
- Com de clave del Registro de verbos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ef70e4a3f748b1f00a364f25755d60a3adfd9091cd2df3032e347f53f55519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047723"
---
# <a name="verb"></a>Verbo

Especifica los verbos que se registrarán para una aplicación.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Verb
         1 = verb1
         2 = verb2
         3 = ...
```

## <a name="remarks"></a>Comentarios

Cada verbo es un **valor REG \_ SZ** de la forma "*name*, *menu \_ flag*, *verb \_ flag*". Los verbos deben numerarse consecutivamente.

El *nombre* describe cómo se anexa el verbo mediante una llamada de [**función AppendMenu.**](/windows/win32/api/winuser/nf-winuser-appendmenua) Por ejemplo, "&Play".

El *valor \_ de la* marca de menú indica cómo debe aparecer el verbo en el menú. Se admiten todas las marcas compatibles [**con AppendMenu,**](/windows/win32/api/winuser/nf-winuser-appendmenua) excepto MF \_ BITMAP, MF \_ OWNERDRAW y MF \_ POPUP.

El *valor \_ de marca* de verbo describe los atributos de los verbos. Use uno de los valores de [**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)o 0.

Para obtener más información, [**vea OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**IOleObject::D oVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)e [**IOleObject::EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua)
</dt> <dt>

[**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb)
</dt> <dt>

[**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)
</dt> </dl>

 

 