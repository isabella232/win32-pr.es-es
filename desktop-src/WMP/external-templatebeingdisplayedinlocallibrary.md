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
ms.openlocfilehash: 9f1d9a93d870882a34014ea2d0d35f29b91f54d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241814"
---
# <a name="externaltemplatebeingdisplayedinlocallibrary"></a>External.templateBeingDisplayedInLocalLibrary

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La **propiedad templateBeingDisplayedInLocalLibrary** indica si la fuente representada por la página de detección actual se muestra en el control de vista de árbol de la biblioteca local.

## <a name="syntax"></a>Sintaxis

``` syntax
window.external.templateBeingDisplayedInLocalLibrary
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un booleano de solo **lectura.** **TRUE** indica que la fuente se muestra en el control de vista de árbol de la biblioteca local.

## <a name="remarks"></a>Observaciones

Una página de detección que representa una fuente para una lista de reproducción dinámica puede mostrar un botón que permite al usuario "guardar" la fuente en su biblioteca local. Guardar la fuente, en este contexto, significa que algunos **metadatos** se guardan en el equipo del usuario y la fuente aparece en el nodo Listas de reproducción del control de vista de árbol de la biblioteca local. El script de la página de detección puede inspeccionar la propiedad **templateBeingDisplayedInLocalLibrary** para determinar si el usuario ya ha guardado la fuente en la biblioteca local. Si el usuario ya ha guardado la fuente, la página de detección no debe mostrar el botón Guardar.

Una página de detección que representa una fuente de radio debe inspeccionar la **propiedad templateBeingDisplayedInLocalLibrary** por el mismo motivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/>                                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





