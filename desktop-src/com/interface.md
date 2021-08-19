---
title: Interfaz (COM)
description: Entrada opcional que especifica todos los identificadores de interfaz (IID) admitidos por la clase asociada.
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- COM de clave del Registro de interfaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d8eaa38b97896f623c8d9f245c48f8d12634f930dc193cba14d5a9217a261e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048123"
---
# <a name="interface-com"></a>Interfaz (COM)

Entrada opcional que especifica todos los identificadores de interfaz (IID) admitidos por la clase asociada.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Interface
         {IID1} = name1
         {IID2} = name2
         ...
```

## <a name="remarks"></a>Comentarios

Si un nombre de interfaz no está presente en esta lista, una instancia de esta clase nunca podrá ser compatible con la interfaz.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clave de interfaz](interface-key.md)
</dt> </dl>

 

 




