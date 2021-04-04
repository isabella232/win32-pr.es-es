---
title: MiscStatus
description: Especifica cómo crear y mostrar un objeto.
ms.assetid: 585b2d1e-3edb-494e-a61e-bbfa6eae2ba1
keywords:
- Clave del registro MiscStatus COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abee49776577df61dc8b7d4e94a0621dfdd8b216
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075950"
---
# <a name="miscstatus"></a>MiscStatus

Especifica cómo crear y mostrar un objeto.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      MiscStatus
         (Default) = value
         aspect = value
```

## <a name="remarks"></a>Observaciones

Para obtener más información, vea la enumeración [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) y [**IOleObject:: GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).

Si no se encuentra ninguna subclave que corresponda a un DVASPECT, se usa el valor predeterminado de **MiscStatus** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IOleObject:: GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)
</dt> </dl>

 

 




