---
title: External.templateBeingDisplayedInLocalLibrary
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. | External.templateBeingDisplayedInLocalLibrary
ms.assetid: a1399c20-804b-4413-be9d-bcf160d75d29
keywords:
- External.templateBeingDisplayedInLocalLibrary Reproductor de Windows Media
topic_type:
- apiref
api_name:
- External.templateBeingDisplayedInLocalLibrary
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8292e2527fe14ec00a2bf7169b4e2ea2ca4c8229672625712ed3ad3a10e421e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648276"
---
# <a name="externaltemplatebeingdisplayedinlocallibrary"></a>External.templateBeingDisplayedInLocalLibrary

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La **propiedad templateBeingDisplayedInLocalLibrary** indica si la fuente representada por la página de detección actual se muestra en el control de vista de árbol de la biblioteca local.

## <a name="syntax"></a>Syntax

``` syntax
window.external.templateBeingDisplayedInLocalLibrary
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un booleano de solo **lectura.** **TRUE** indica que la fuente se muestra en el control de vista de árbol de la biblioteca local.

## <a name="remarks"></a>Comentarios

Una página de detección que representa una fuente para una lista de reproducción dinámica puede mostrar un botón que permite al usuario "guardar" la fuente en su biblioteca local. Guardar la fuente, en este contexto, significa que algunos **metadatos** se guardan en el equipo del usuario y la fuente aparece en el nodo Listas de reproducción del control de vista de árbol de la biblioteca local. El script de la página de detección puede inspeccionar la propiedad **templateBeingDisplayedInLocalLibrary** para determinar si el usuario ya ha guardado la fuente en la biblioteca local. Si el usuario ya ha guardado la fuente, la página de detección no debe mostrar el botón Guardar.

Una página de detección que representa una fuente de radio debe inspeccionar la **propiedad templateBeingDisplayedInLocalLibrary** por el mismo motivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/>                                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





