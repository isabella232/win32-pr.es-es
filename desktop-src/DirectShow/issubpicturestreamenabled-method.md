---
description: El método IsSubpictureStreamEnabled recupera un valor que indica si la secuencia de subpicture especificada está habilitada en el título actual.
ms.assetid: c6436f77-ca94-464f-9336-f485f5d5d199
title: Método IsSubpictureStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 818b4ff18dac87ea3346a1a503764b2e5e9cd02a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063233"
---
# <a name="issubpicturestreamenabled-method"></a>Método IsSubpictureStreamEnabled

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `IsSubpictureStreamEnabled` método recupera un valor que indica si la secuencia de subimagen especificada está habilitada en el título actual.

``` syntax
[ bEnabled = ] MSWebDVD.IsSubpictureStreamEnabled(iStream)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Especifica la secuencia de subaspección como un entero.



| Value   | Descripción              |
|---------|--------------------------|
| De 0 a 31 | secuencia de subpicture        |
| 63      | secuencia de velocidad de bits baja muted |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que indica si la secuencia de audio especificada está disponible en el título actual. True significa que está disponible.

## <a name="remarks"></a>Observaciones

Aunque un disco puede contener hasta 32 secuencias de subimagen, cada secuencia no está necesariamente disponible para cada título. Compruebe siempre que una secuencia está disponible para un título antes de establecer la [**propiedad CurrentSubpictureStream.**](currentsubpicturestream-property.md)

 

 



