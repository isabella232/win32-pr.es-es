---
title: Interfaz (COM)
description: Entrada opcional que especifica todos los identificadores de interfaz (IID) admitidos por la clase asociada.
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- COM de clave del Registro de interfaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990c06285d60067c9a26faffabffc70cbdd283d1
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369583"
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

## <a name="remarks"></a>Observaciones

Si un nombre de interfaz no está presente en esta lista, una instancia de esta clase nunca puede ser compatible con la interfaz.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clave de interfaz](interface-key.md)
</dt> </dl>

 

 




