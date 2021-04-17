---
title: Interfaz (COM)
description: Una entrada opcional que especifica todos los identificadores de interfaz (IID) admitidos por la clase asociada.
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- Interfaz de la clave del registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990c06285d60067c9a26faffabffc70cbdd283d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105714524"
---
# <a name="interface-com"></a>Interfaz (COM)

Una entrada opcional que especifica todos los identificadores de interfaz (IID) admitidos por la clase asociada.

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

Si el nombre de una interfaz no está presente en esta lista, la interfaz nunca puede ser compatible con una instancia de esta clase.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clave de interfaz](interface-key.md)
</dt> </dl>

 

 




