---
title: DVD. dominio
description: La propiedad de dominio recupera el dominio actual del DVD.
ms.assetid: 74f4a6a3-8518-48c7-b023-f0255a3a62fd
keywords:
- DVD. dominio Windows Media Player
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
ms.openlocfilehash: db4a2af92abe533fed7a13e48cb7c0724223bbc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359717"
---
# <a name="dvddomain"></a>DVD. dominio

La propiedad de **dominio** recupera el dominio actual del DVD.

``` syntax
player.dvd.domain
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de solo lectura que contiene uno de los valores siguientes.



| String            | Descripción                                                                                                                           |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| firstPlay         | Realizar la inicialización predeterminada de un disco DVD.                                                                                      |
| videoManagerMenu  | Mostrar menús para todo el disco. También conocido como menú de Media Player para Windows. Normalmente denominado el menú de título o el menú superior. |
| videoTitleSetMenu | Mostrar menús para el conjunto de títulos actual. También conocido como titleMenu para Windows Media Player. Normalmente denominado menú raíz.              |
| title             | Normalmente, mostrando el título actual.                                                                                                 |
| stop              | El navegador de DVD está en el dominio de detención de DVD.                                                                                          |
| no definido         | El reproductor no está en ningún dominio de DVD.                                                                                                      |



 

## <a name="remarks"></a>Observaciones

Cada DVD se crea de forma diferente. Algunos DVDs no contienen los dominios firstPlay, videoManagerMenu o videoTitleSetMenu.

**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve una cadena vacía.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Versión<br/>                  | Windows Media Player para Windows XP o posterior<br/>                            |
| Archivo DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de DVD**](dvd-object.md)
</dt> </dl>

 

 





