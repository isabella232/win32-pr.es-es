---
title: AmbientAttributes.tabStop
description: El atributo tabStop especifica o recupera un valor que indica si el control está en el orden de tabulación. Para establecer el orden de tabulación, coloque el control en el script general antes o después de otras etiquetas de control.
ms.assetid: 3d4b7fe4-1032-44e1-bae5-f253d00881bf
keywords:
- AmbientAttributes.tabStop Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.tabStop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 772e4a35d94f49cdbaa2be3053beb28f899654ed69961101e63bb1d6ab531641
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469895"
---
# <a name="ambientattributestabstop"></a>AmbientAttributes.tabStop

El **atributo tabStop** especifica o recupera un valor que indica si el control está en el orden de tabulación. Para establecer el orden de tabulación, coloque el control en el script general antes o después de otras etiquetas de control.

``` syntax
        elementID.tabStop
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un valor booleano de lectura **y escritura.**



| Value | Descripción                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| true  | El control está en el orden de tabulación (el control tendrá un tabulador: requisito de accesibilidad). |
| false | El control no está en el orden de tabulación.                                                       |



 

## <a name="remarks"></a>Observaciones

El **atributo tabStop** no es aplicable al **elemento EFFECTS.**

El valor predeterminado de este atributo es true para todos los elementos excepto **AUTOMENU** y **TEXT**, que tienen un valor predeterminado de false.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos ambientales**](ambient-attributes.md)
</dt> </dl>

 

 





