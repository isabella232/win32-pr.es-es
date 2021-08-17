---
title: AuxUserType
description: Especifica el nombre para mostrar corto de una aplicación y los nombres de aplicación.
ms.assetid: 3367eb68-01f4-4cb9-b1d0-27554c28b68d
keywords:
- Tecla del Registro AuxUserType COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1dbec8e873e6f6cfcb5fdb29468c1f09c0a7a6935280054e129ddac0b49e282
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550729"
---
# <a name="auxusertype"></a>AuxUserType

Especifica el nombre para mostrar corto de una aplicación y los nombres de aplicación.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AuxUserType
         2 = ShortDisplayName
         3 = ApplicationName
```

## <a name="remarks"></a>Comentarios

La longitud máxima recomendada para *ShortDisplayName* es de 15 caracteres. Este nombre se usa en los menús, incluidos los menús emergentes.

*ApplicationName* debe contener el nombre real de la aplicación (por ejemplo, "Acme Draw 2.0"). Este nombre se usa en el campo **Resultados** del **cuadro de diálogo** Pegar especial .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> </dl>

 

 




