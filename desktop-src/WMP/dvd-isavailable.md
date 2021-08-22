---
title: DVD.isAvailable
description: La propiedad isAvailable indica si un tipo de información especificado está disponible o se puede realizar una acción especificada. | DVD.isAvailable
ms.assetid: ed34a943-b9c3-40a8-8845-b83f16951a3e
keywords:
- DVD.isAvailable Reproductor de Windows Media
topic_type:
- apiref
api_name:
- DVD.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efb1a240c8df072d0770521f70c526f4e096c26385df85cff7acf0d229fdc252
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996925"
---
# <a name="dvdisavailable"></a>DVD.isAvailable

La **propiedad isAvailable** indica si un tipo de información especificado está disponible o se puede realizar una acción especificada.

``` syntax
player.dvd.isAvailable(
        name
        )
```

## <a name="parameters"></a>Parámetros

*name*

**Cadena** que contiene uno de los valores siguientes.



| String     | Descripción                                                                            |
|------------|----------------------------------------------------------------------------------------|
| atrás       | Determina si el **método back** está disponible.                                   |
| Dvd        | Determina si se carga el DVD.                                                  |
| dvdDecoder | Determina si el descodificador de DVD está instalado en el sistema.                             |
| resume     | Determina si el **método resume** está disponible.                                 |
| titleMenu  | Determina si el **método titleMenu** está disponible.                              |
| topMenu    | Determina si el **método topMenu** está disponible. Normalmente se denomina menú raíz. |



 

## <a name="return-values"></a>Valores devueltos

Este método devuelve un valor **booleano** de solo lectura que indica si el parámetro especificado está disponible.

## <a name="remarks"></a>Comentarios

Las características de DVD Reproductor de Windows Media no funcionarán en equipos que no tengan instalados descodificadores de DVD de terceros. Puede determinar si un descodificador está disponible llamando a **isAvailable**("dvdDecoder").

Cada DVD se ha escrito de forma diferente. Los métodos disponibles durante la reproducción y navegación de DVD dependen de cómo se cree el DVD.

**Reproductor de Windows Media 10 Mobile:** Esta propiedad siempre devuelve **false**.

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

 

 





