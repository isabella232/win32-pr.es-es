---
description: El método GetLangFromLangID recupera una cadena legible cuando se le da un identificador de idioma principal.
ms.assetid: 73cff3df-bfcd-4e51-bd41-51545ed82f09
title: Método GetLangFromLangID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23afddf746852028c26732eb658e786588f7e9ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061121"
---
# <a name="getlangfromlangid-method"></a>Método GetLangFromLangID

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

Devuelve una representación String del idioma que se puede mostrar en la interfaz de usuario de la aplicación.

## <a name="remarks"></a>Observaciones

Aunque este método se denomina , el parámetro que se pasa es realmente el identificador de `GetLangFromLangID` idioma principal, no el identificador de idioma.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**GetAudioLanguage**](getaudiolanguage-method.md)
</dt> <dt>

[**GetDVDTextLanguageLCID**](getdvdtextlanguagelcid-method.md)
</dt> </dl>

 

 



