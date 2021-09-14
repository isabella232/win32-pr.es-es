---
description: El método GetAudioLanguage recupera una cadena que indica qué idioma está disponible en la secuencia de audio especificada.
ms.assetid: 5ff12058-eb00-4a2c-8d39-88282f68f001
title: GetAudioLanguage (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af71ad7943fe5442ded09f0b599c64c4b7215dac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063253"
---
# <a name="getaudiolanguage-method"></a>GetAudioLanguage (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `GetAudioLanguage` método recupera una cadena que indica qué idioma está disponible en la secuencia de audio especificada.

``` syntax
[ slang = ] MSWebDVD.GetAudioLanguage(iStream)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Especifica el número de secuencia de audio del título actual como entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una cadena legible que identifica el idioma de la secuencia de audio en el título actual.

 

 



