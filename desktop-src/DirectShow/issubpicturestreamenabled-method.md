---
description: El método IsSubpictureStreamEnabled recupera un valor que indica si la secuencia de subimagen especificada está habilitada en el título actual.
ms.assetid: c6436f77-ca94-464f-9336-f485f5d5d199
title: Método IsSubpictureStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 818b4ff18dac87ea3346a1a503764b2e5e9cd02a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906778"
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

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Especifica el flujo de la subimagen como un entero.



| Value   | Descripción              |
|---------|--------------------------|
| de 0 a 31 | secuencia de subimagen        |
| 63      | secuencia de velocidad de bits baja silenciada |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que indica si la secuencia de audio especificada está disponible en el título actual. True significa que está disponible.

## <a name="remarks"></a>Observaciones

Aunque un disco puede contener hasta 32 secuencias de subimágenes, cada flujo no está necesariamente disponible para cada título. Compruebe siempre que haya un flujo disponible para un título antes de establecer la propiedad [**CurrentSubpictureStream**](currentsubpicturestream-property.md) .

 

 



