---
description: El método SelectDefaultAudioLanguage establece el idioma de audio predeterminado actual en el objeto MSWebDVD.
ms.assetid: 7d63b7ef-2b03-4929-822a-c4d11fb7a825
title: SelectDefaultAudioLanguage (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4b649993cc3e110e78ba0a674e414dd4214af982dd44d64fcc1aca7646d1b04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072629"
---
# <a name="selectdefaultaudiolanguage-method"></a>SelectDefaultAudioLanguage (método)

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

Especifica la extensión de lenguaje de audio de DVD como un valor entero.



| Valor | Descripción       |
|-------|-------------------|
| 0     | NotSpecified      |
| 1     | Subtítulos          |
| 2     | VisualmenteAmpaired  |
| 3     | DirectorComments1 |
| 4     | DirectorComments2 |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objeto MSWebDVD](mswebdvd-object.md)
</dt> </dl>

 

 



