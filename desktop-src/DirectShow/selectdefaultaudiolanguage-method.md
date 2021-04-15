---
description: El método SelectDefaultAudioLanguage establece el idioma de audio predeterminado actual en el objeto MSWebDVD.
ms.assetid: 7d63b7ef-2b03-4929-822a-c4d11fb7a825
title: Método SelectDefaultAudioLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 126de6daf4f5e0337058495a3ee7898594bfd704
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537108"
---
# <a name="selectdefaultaudiolanguage-method"></a>Método SelectDefaultAudioLanguage

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `SelectDefaultAudioLanguage` método establece el idioma de audio predeterminado actual en el objeto MSWebDVD.

``` syntax
MSWebDVD.SelectDefaultAudioLanguage(iLang, iExt)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*
</dt> <dd>

Especifica el idioma como un valor LCID entero.

</dd> <dt>

<span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*
</dt> <dd>

Especifica la extensión de idioma de audio de DVD como valor entero.



| Value | Descripción       |
|-------|-------------------|
| 0     | NotSpecified      |
| 1     | Subtítulos          |
| 2     | VisuallyImpaired  |
| 3     | DirectorComments1 |
| 4     | DirectorComments2 |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objeto MSWebDVD](mswebdvd-object.md)
</dt> </dl>

 

 



