---
description: El método IsAudioStreamEnabled recupera un valor que indica si la secuencia de audio especificada está habilitada en el título actual.
ms.assetid: df6c69a7-6eb0-4662-a3aa-f3f895b42cbc
title: Método IsAudioStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92df59479e5729c392eb25b6c6c075a52b4835b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536448"
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

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Especifica la secuencia de audio como un valor entero comprendido entre 0 y 7.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que indica si la secuencia de audio especificada está disponible para el título actual. True significa que está disponible.

## <a name="remarks"></a>Observaciones

Aunque un disco puede contener hasta ocho flujos de audio independientes, cada flujo no está necesariamente disponible para cada título. Por ejemplo, un título de película principal podría tener tres flujos de audio para inglés, español y japonés, pero el título "próxima atracciones" podría tener solo una secuencia de audio en inglés. Compruebe siempre que haya un flujo disponible para un título antes de establecer la propiedad [**CurrentAudioStream**](currentaudiostream-property.md) .

 

 



