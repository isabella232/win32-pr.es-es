---
description: El método GetSubpictureLanguage recupera el idioma de la secuencia de subpicture especificada.
ms.assetid: 2a2e6961-99c3-4200-b462-b381f9e37066
title: GetSubpictureLanguage (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f87d1bf95ee13a1a15e631e2bc53477b62b789a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061105"
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

Especifica el número de secuencia de subimagen cuyo idioma de texto desea recuperar como entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una cadena legible que identifica el idioma de la secuencia de audio en el título actual.

 

 



