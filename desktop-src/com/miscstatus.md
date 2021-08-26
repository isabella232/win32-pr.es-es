---
title: MiscStatus
description: Especifica cómo crear y mostrar un objeto .
ms.assetid: 585b2d1e-3edb-494e-a61e-bbfa6eae2ba1
keywords:
- MiscStatus registry key COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41aa5a5ab7f777eb6aa19d919c69ca219c9364cd1d6e5e9471cb677300d4ebb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992355"
---
# <a name="miscstatus"></a>MiscStatus

Especifica cómo crear y mostrar un objeto .

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      MiscStatus
         (Default) = value
         aspect = value
```

## <a name="remarks"></a>Comentarios

Para obtener más información, vea la [**enumeración OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) [**e IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).

Si no se encuentra ninguna subclave que se corresponda con DVASPECT, se usa el valor predeterminado **de MiscStatus.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)
</dt> </dl>

 

 




