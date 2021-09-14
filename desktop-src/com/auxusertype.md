---
title: AuxUserType
description: Especifica el nombre para mostrar corto de una aplicación y los nombres de aplicación.
ms.assetid: 3367eb68-01f4-4cb9-b1d0-27554c28b68d
keywords:
- Com de clave del Registro AuxUserType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c66fcfbcdc2886e93d08040659b39c42d47c291
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264564"
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

## <a name="remarks"></a>Observaciones

La longitud máxima recomendada para *ShortDisplayName* es de 15 caracteres. Este nombre se usa en los menús, incluidos los menús emergentes.

*ApplicationName* debe contener el nombre real de la aplicación (por ejemplo, "Acme Draw 2.0"). Este nombre se usa en el campo **Resultados** del **cuadro de diálogo** Pegar especial .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> </dl>

 

 




