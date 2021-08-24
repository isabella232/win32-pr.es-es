---
title: Elemento ButtonTip
description: Nota En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. | Elemento ButtonTip
ms.assetid: 93e5d0c8-8d2d-45c1-9d47-bbd0b6eb8b88
keywords:
- Elemento ButtonTip Reproductor de Windows Media
topic_type:
- apiref
api_name:
- ButtonTip Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7fb4a162a8e77fea7548265825af6c6cbda75dbafadf05fe32cb664c4d563f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764305"
---
# <a name="buttontip-element"></a>Elemento ButtonTip

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **elemento ButtonTip** especifica la cadena de texto que se muestra cuando el usuario apunta a un botón del panel de tareas.

``` syntax
<ButtonTip>
   text string
</ButtonTip>
```

## <a name="attributes"></a>Atributos

Este elemento no tiene atributos.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elemento                                              |
|-----------------|------------------------------------------------------|
| Elementos primarios | **ServiceTask1,** **ServiceTask2,** **ServiceTask3** |
| Elementos secundarios  | Ninguno                                                 |



 

## <a name="remarks"></a>Observaciones

Este elemento es opcional para cada instancia de **ServiceTask1,** **ServiceTask2** o **ServiceTask3.** Si no se proporciona este elemento, Reproductor de Windows Media el texto del botón como valor predeterminado.

> [!Note]  
> Reproductor de Windows Media 10 tiene tres paneles de tareas en los que una tienda en línea puede mostrar sus páginas web. La tienda en línea puede optar por usar uno, dos o los tres paneles de tareas. Reproductor de Windows Media 11 solo tiene un panel de tareas, que el usuario puede ver haciendo clic en la pestaña **Tiendas** en línea. Reproductor de Windows Media 11 omite los elementos **ServiceTask2** y **ServiceTask3.**

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 10 o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





