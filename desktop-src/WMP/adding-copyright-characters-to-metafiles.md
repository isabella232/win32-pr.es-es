---
title: Agregar caracteres de copyright a metarchivos
description: Es posible que los caracteres de los símbolos de registro de marca comercial y copyright ( \169; o \ 174; ) no se muestren correctamente si el metarchivo no está codificado mediante el esquema de codificación UTF-8.
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
ms.openlocfilehash: b0ab5fc4e539331406bb776a4bcdacbed6578a234dd9e84a3c358cdbe9936ad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865165"
---
# <a name="adding-copyright-characters-to-metafiles"></a>Agregar caracteres de copyright a metarchivos

Es posible que los caracteres de los símbolos de registro de marca comercial y copyright (© o ® ) no se muestren correctamente si el metarchivo no está codificado mediante el esquema de codificación UTF-8. En este caso, para mostrar cualquiera de estos símbolos correctamente para todos los usuarios, puede usar los equivalentes ASCII (c) y (r) dentro del elemento **COPYRIGHT,** como se muestra en el código siguiente.


```
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>
```



Si el metarchivo está codificado mediante UTF-8, los símbolos de copyright y marca comercial se mostrarán correctamente.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




