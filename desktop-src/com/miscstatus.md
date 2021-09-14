---
title: MiscStatus
description: Especifica cómo crear y mostrar un objeto .
ms.assetid: 585b2d1e-3edb-494e-a61e-bbfa6eae2ba1
keywords:
- MiscStatus registry key COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abee49776577df61dc8b7d4e94a0621dfdd8b216
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889044"
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

 

 




