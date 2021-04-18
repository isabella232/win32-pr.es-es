---
description: El método GetSubpictureLanguage recupera el idioma de la secuencia de subimagen especificada.
ms.assetid: 2a2e6961-99c3-4200-b462-b381f9e37066
title: Método GetSubpictureLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f87d1bf95ee13a1a15e631e2bc53477b62b789a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677043"
---
# <a name="getsubpicturelanguage-method"></a>Método GetSubpictureLanguage

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `GetSubpictureLanguage` método recupera el idioma de la secuencia de subimagen especificada.

``` syntax
[ sLang = ] MSWebDVD.GetSubpictureLanguage(iStream)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Especifica el número de secuencia de la subimagen cuyo idioma de texto desea recuperar como entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una cadena legible para el usuario que identifica el idioma de la secuencia de audio en el título actual.

 

 



