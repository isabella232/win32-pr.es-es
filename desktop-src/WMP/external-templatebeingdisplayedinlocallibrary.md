---
title: External. templateBeingDisplayedInLocalLibrary
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. templateBeingDisplayedInLocalLibrary
ms.assetid: a1399c20-804b-4413-be9d-bcf160d75d29
keywords:
- Media Player de Windows externa. templateBeingDisplayedInLocalLibrary
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699724"
---
# <a name="externaltemplatebeingdisplayedinlocallibrary"></a>External. templateBeingDisplayedInLocalLibrary

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La propiedad **templateBeingDisplayedInLocalLibrary** indica si la fuente representada por la página de detección actual se muestra en el control de vista de árbol de la biblioteca local.

## <a name="syntax"></a>Sintaxis

``` syntax
window.external.templateBeingDisplayedInLocalLibrary
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **valor booleano** de solo lectura. **True** indica que la fuente se muestra en el control de vista de árbol de la biblioteca local.

## <a name="remarks"></a>Observaciones

Una página de detección que representa una fuente para una lista de reproducción dinámica puede mostrar un botón que permite al usuario "guardar" la fuente en su biblioteca local. Guardar la fuente, en este contexto, significa que algunos metadatos se guardan en el equipo del usuario y que la fuente aparece bajo el nodo **listas de reproducción** en el control de vista de árbol de la biblioteca local. El script de la página de detección puede inspeccionar la propiedad **templateBeingDisplayedInLocalLibrary** para determinar si el usuario ya ha guardado la fuente en la biblioteca local. Si el usuario ya ha guardado la fuente, la página de detección no debe mostrar el botón Guardar.

Una página de detección que representa una fuente de radio debe inspeccionar la propiedad **templateBeingDisplayedInLocalLibrary** por la misma razón.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/>                                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para las tiendas en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





