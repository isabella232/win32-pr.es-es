---
description: El método IsAudioStreamEnabled recupera un valor que indica si la secuencia de audio especificada está habilitada en el título actual.
ms.assetid: df6c69a7-6eb0-4662-a3aa-f3f895b42cbc
title: Método IsAudioStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92df59479e5729c392eb25b6c6c075a52b4835b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063248"
---
# <a name="isaudiostreamenabled-method"></a>Método IsAudioStreamEnabled

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `IsAudioStreamEnabled` método recupera un valor que indica si la secuencia de audio especificada está habilitada en el título actual.

``` syntax
[bEnabled = ] MSWebDVD.IsAudioStreamEnabled(iStream)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Especifica la secuencia de audio como un valor entero de 0 a 7.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que indica si la secuencia de audio especificada está disponible para el título actual. True significa que está disponible.

## <a name="remarks"></a>Observaciones

Aunque un disco puede contener hasta ocho secuencias de audio independientes, cada secuencia no está necesariamente disponible para cada título. Por ejemplo, un título de película principal podría tener tres secuencias de audio para inglés, español y japonés, pero el título "Próximas carreras" podría tener solo una secuencia de audio en inglés. Compruebe siempre que una secuencia está disponible para un título antes de establecer la [**propiedad CurrentAudioStream.**](currentaudiostream-property.md)

 

 



