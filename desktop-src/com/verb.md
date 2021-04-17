---
title: Verbo
description: Especifica los verbos que se van a registrar para una aplicación.
ms.assetid: bfcad36d-a52a-4117-bf0b-6135b197a7ee
keywords:
- Clave del registro Verb COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ef025ee0807ca3e75577f26f81951db22dfb0ac
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105714465"
---
# <a name="verb"></a>Verbo

Especifica los verbos que se van a registrar para una aplicación.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Verb
         1 = verb1
         2 = verb2
         3 = ...
```

## <a name="remarks"></a>Observaciones

Cada verbo es un valor de **reg \_ SZ** con el formato "*nombre*, *\_ marca de menú*, *\_ marca de verbo*". Los verbos se deben numerar consecutivamente.

El *nombre* describe cómo se anexa el verbo mediante una llamada de función [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) . Por ejemplo, "&Play".

El valor de la *\_ marca de menú* indica cómo debe aparecer el verbo en el menú. Se admiten todas las marcas admitidas por [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) , excepto en el caso del \_ elemento emergente MF Bitmap, MF \_ OWNERDRAW y MF \_ Popup.

El valor de *\_ marcador de verbo* describe los atributos de los verbos. Use uno de los valores de [**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)o 0.

Para obtener más información, vea [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**IOleObject::D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)y [**IOleObject:: EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua)
</dt> <dt>

[**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb)
</dt> <dt>

[**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)
</dt> </dl>

 

 