---
title: Evento External.OnColorChange (tipo 1)
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. | Evento External.OnColorChange (tipo 1)
ms.assetid: 45e6ec4a-e680-4d50-8fb7-410f12383eef
keywords:
- Evento External.OnColorChange (tipo 1) Reproductor de Windows Media
topic_type:
- apiref
api_name:
- External.OnColorChange Event (Type 1)
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b50f23763827965c80c3c2774f6139ba2345e4e50633966d5debc1f2d4b782e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648785"
---
# <a name="externaloncolorchange-event-type-1"></a>Evento External.OnColorChange (tipo 1)

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **evento OnColorChange** tiene lugar cuando cambia el color del Reproductor de Windows Media interfaz de usuario.

``` syntax
window.external.OnColorChange = FunctionName
```

## <a name="possible-values"></a>Valores posibles

Se trata de una propiedad de solo escritura que especifica el nombre de la función en el script que Reproductor de Windows Media cuando se produce el evento.

## <a name="parameters"></a>Parámetros

La función que controla este evento no toma ningún parámetro.

## <a name="remarks"></a>Comentarios

Los usuarios pueden cambiar el color de la interfaz Reproductor de Windows Media usuario. Puede usar este evento para personalizar la apariencia de la página web hospedada para que coincida con el reproductor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/>                                  |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





