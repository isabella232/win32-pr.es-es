---
title: Agregar caracteres de copyright a metarchivos
description: Es posible que los caracteres de los símbolos de registro de marca comercial y copyright ( \ 169 o \ 174; ) no se muestren correctamente si el metarchivo no está codificado mediante el esquema de codificación UTF-8.
ms.assetid: 9124c8d4-1fc1-4163-ada9-d96af58f8b98
keywords:
- Agregar caracteres de copyright a metarchivos Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Adding Copyright Characters to Metafiles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e71b116a3500fdb4217613c81bd4f041af75a66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374326"
---
# <a name="adding-copyright-characters-to-metafiles"></a>Agregar caracteres de copyright a metarchivos

Es posible que los caracteres de los símbolos de registro de marcas comerciales y copyright (© o ® ) no se muestren correctamente si el metarchivo no está codificado mediante el esquema de codificación UTF-8. En este caso, para mostrar cualquiera de estos símbolos correctamente para todos los usuarios, puede usar los equivalentes ASCII (c) y (r) dentro del elemento **COPYRIGHT,** como se muestra en el código siguiente.


```
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>
```



Si el metarchivo está codificado mediante UTF-8, los símbolos de marca comercial y de copyright se mostrarán correctamente.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




