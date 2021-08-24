---
description: El método GetLangFromLangID recupera una cadena legible cuando se le da un identificador de idioma principal.
ms.assetid: 73cff3df-bfcd-4e51-bd41-51545ed82f09
title: GetLangFromLangID (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6041f12c82f0e659928db9f5aa02fd916d3ff9907bf3114eb40c525b8b1d8d2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756755"
---
# <a name="getlangfromlangid-method"></a>GetLangFromLangID (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El método recupera una cadena legible cuando `GetLangFromLangID` se le da un identificador de idioma principal.

``` syntax
[ sLanguage = ] MSWebDVD.GetLangFromLangID(iPrimaryLangID)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iPrimaryLangID*
</dt> <dd>

Especifica el identificador de idioma principal como entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una representación String del lenguaje que se puede mostrar en la interfaz de usuario de la aplicación.

## <a name="remarks"></a>Comentarios

Aunque este método se denomina , el parámetro que se pasa es realmente el identificador de `GetLangFromLangID` idioma principal, no el identificador de idioma.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetAudioLanguage**](getaudiolanguage-method.md)
</dt> <dt>

[**GetDVDTextLanguageLCID**](getdvdtextlanguagelcid-method.md)
</dt> </dl>

 

 



