---
description: El método GetSubpictureLanguage recupera el idioma de la secuencia de subpicture especificada.
ms.assetid: 2a2e6961-99c3-4200-b462-b381f9e37066
title: GetSubpictureLanguage (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdedc90789efb331b1438744a0f64a42782bf1d1e363170ce626ed023d2e542a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536935"
---
# <a name="getsubpicturelanguage-method"></a>GetSubpictureLanguage (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `GetSubpictureLanguage` método recupera el idioma de la secuencia de subimagen especificada.

``` syntax
[ sLang = ] MSWebDVD.GetSubpictureLanguage(iStream)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Especifica el número de secuencia de subaspección cuyo idioma de texto desea recuperar como entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una cadena legible que identifica el idioma de la secuencia de audio en el título actual.

 

 



