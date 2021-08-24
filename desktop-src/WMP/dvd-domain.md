---
title: DVD.domain
description: La propiedad domain recupera el dominio actual del DVD.
ms.assetid: 74f4a6a3-8518-48c7-b023-f0255a3a62fd
keywords:
- Dvd.domain Reproductor de Windows Media
topic_type:
- apiref
api_name:
- DVD.domain
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0db8e6e212fec11de5f3619c2c1f97a90f579b34515983b0384d0d08ab0ff60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651175"
---
# <a name="dvddomain"></a>DVD.domain

La **propiedad** domain recupera el dominio actual del DVD.

``` syntax
player.dvd.domain
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de solo **lectura** que contiene uno de los valores siguientes.



| String            | Descripción                                                                                                                           |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| firstPlay         | Realizar la inicialización predeterminada de un disco de DVD.                                                                                      |
| videoManagerMenu  | Mostrar menús para todo el disco. También se conoce como topMenu para Reproductor de Windows Media. Normalmente se denomina el menú de título o el menú superior. |
| videoTitleSetMenu | Mostrar menús para el conjunto de títulos actual. También se conoce como titleMenu para Reproductor de Windows Media. Normalmente se denomina menú raíz.              |
| title             | Normalmente se muestra el título actual.                                                                                                 |
| stop              | El navegador de DVD está en el dominio DE DEtenerse de DVD.                                                                                          |
| no definido         | El reproductor no está en ningún dominio de DVD.                                                                                                      |



 

## <a name="remarks"></a>Comentarios

Cada DVD se ha escrito de forma diferente. Algunos DVD no contienen los dominios firstPlay, videoManagerMenu o videoTitleSetMenu.

**Reproductor de Windows Media 10 Mobile:** Esta propiedad siempre devuelve una cadena vacía.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Versión<br/>                  | Reproductor de Windows Media para Windows XP o posterior<br/>                            |
| Archivo DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dvd (objeto)**](dvd-object.md)
</dt> </dl>

 

 





