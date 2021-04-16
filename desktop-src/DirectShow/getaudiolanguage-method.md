---
description: El método GetAudioLanguage recupera una cadena que indica qué idioma está disponible en la secuencia de audio especificada.
ms.assetid: 5ff12058-eb00-4a2c-8d39-88282f68f001
title: Método GetAudioLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af71ad7943fe5442ded09f0b599c64c4b7215dac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536639"
---
# <a name="getaudiolanguage-method"></a>Método GetAudioLanguage

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `GetAudioLanguage` método recupera una cadena que indica qué idioma está disponible en la secuencia de audio especificada.

``` syntax
[ slang = ] MSWebDVD.GetAudioLanguage(iStream)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Especifica el número de secuencia de audio del título actual como un entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una cadena legible para el usuario que identifica el idioma de la secuencia de audio en el título actual.

 

 



