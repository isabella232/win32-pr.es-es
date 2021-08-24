---
description: El método GetDVDTextLanguageLCID recupera el identificador de configuración regional (LCID) para el bloque de cadena de texto especificado.
ms.assetid: feaa1db8-2d33-4c32-8491-f3aa5555e3d3
title: Método GetDVDTextLanguageLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c60abedc3a986bfec766cc14c2251d9bed83650ee737762a4e870af9d283a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748725"
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

## <a name="remarks"></a>Comentarios

Las cadenas de texto complementarias se almacenan en bloques contiguos en el disco. Cada lenguaje tiene un bloque de cadenas. Una aplicación especifica estos bloques por un índice, que debe ser menor que el valor devuelto por [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objeto MSWebDVD](mswebdvd-object.md)
</dt> <dt>

[**GetLangFromLangID**](getlangfromlangid-method.md)
</dt> </dl>

 

 



