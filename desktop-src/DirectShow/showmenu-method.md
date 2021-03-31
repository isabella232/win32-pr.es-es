---
description: El método ShowMenu muestra el menú especificado en la pantalla.
ms.assetid: 971c5bc3-a327-4840-8f3c-9a6573204ffb
title: Método ShowMenu
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c64b2a08c8881001cc47c972ad8cc865af8a174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806241"
---
# <a name="showmenu-method"></a>Método ShowMenu

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `ShowMenu` método muestra el menú especificado en la pantalla.

``` syntax
MSWebDVD.ShowMenu(iMenuID)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*iMenuID*
</dt> <dd>

Especifica el identificador de menú como un entero.



| Value | Descripción |
|-------|-------------|
| 2     | Título (superior) |
| 3     | Root        |
| 4     | Subimagen  |
| 5     | Audio       |
| 6     | Ángulo       |
| 7     | Capítulo     |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Los nombres de los menús de DVD pueden resultar confusos. El menú de título es otro nombre para el menú administrador de vídeo, el menú principal para todo el disco; en general, se enumeran todos los conjuntos de títulos de vídeo disponibles en el disco. El menú raíz es el menú de un conjunto de títulos de vídeo, que puede contener un título o un grupo de títulos. Todos los títulos de un conjunto de títulos comparten los mismos menús de subimagen, audio y ángulo.

 

 



