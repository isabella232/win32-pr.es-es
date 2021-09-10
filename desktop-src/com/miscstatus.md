---
title: MiscStatus
description: Especifica cómo crear y mostrar un objeto .
ms.assetid: 585b2d1e-3edb-494e-a61e-bbfa6eae2ba1
keywords:
- Com de clave del Registro MiscStatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abee49776577df61dc8b7d4e94a0621dfdd8b216
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369592"
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

## <a name="remarks"></a>Observaciones

Para obtener más información, vea la [**enumeración OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) [**e IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).

Si no se encuentra ninguna subclave que se corresponda con DVASPECT, se usa el valor predeterminado **de MiscStatus.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)
</dt> </dl>

 

 




