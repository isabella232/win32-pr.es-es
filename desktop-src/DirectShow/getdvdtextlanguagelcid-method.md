---
description: El método GetDVDTextLanguageLCID recupera el identificador de configuración regional (LCID) para el bloque de cadena de texto especificado.
ms.assetid: feaa1db8-2d33-4c32-8491-f3aa5555e3d3
title: Método GetDVDTextLanguageLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66d21b9870982b605d9deeb1e22882a525c5616
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061140"
---
# <a name="getdvdtextlanguagelcid-method"></a>Método GetDVDTextLanguageLCID

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `GetDVDTextLanguageLCID` método recupera el identificador de configuración regional (LCID) para el bloque de cadena de texto especificado.

``` syntax
[ iLCID = ] MSWebDVD.GetDVDTextLanguageLCID(iLangIndex)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*
</dt> <dd>

Especifica el bloque de idioma de texto del disco como entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor LCID que contiene información que especifica el idioma en el que se escriben las cadenas.

## <a name="remarks"></a>Observaciones

Las cadenas de texto complementarias se almacenan en bloques contiguos en el disco. Cada lenguaje tiene un bloque de cadenas. Una aplicación especifica estos bloques por un índice, que debe ser menor que el valor devuelto por [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objeto MSWebDVD](mswebdvd-object.md)
</dt> <dt>

[**GetLangFromLangID**](getlangfromlangid-method.md)
</dt> </dl>

 

 



