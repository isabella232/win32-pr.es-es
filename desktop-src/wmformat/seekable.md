---
title: En
description: El atributo de búsqueda es un atributo de nivel de archivo que especifica si una aplicación puede buscar puntos dentro del contenido.
ms.assetid: 9653e368-4782-4506-9c44-54c9406b61b5
keywords:
- Formato de Windows Media de búsqueda
topic_type:
- apiref
api_name:
- Seekable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4db701be363c194c75bd698062d79a0c0c407cc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104358761"
---
# <a name="seekable"></a>En

El atributo de **búsqueda** es un atributo de nivel de archivo que especifica si una aplicación puede buscar puntos dentro del contenido.

## <a name="global-constant"></a>Constante global

g \_ wszWMSeekable

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ bool**

## <a name="remarks"></a>Observaciones

Se trata de un atributo codificado.

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no enviará su significado normal a los objetos del SDK de Windows Media Format.

El valor de este atributo para un archivo puede variar en función del objeto que exponga la interfaz [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) o [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) utilizada para recuperarlo. Esto se debe a que los objetos del lector (tanto sincrónicos como asincrónicos) realizan una comprobación más exhaustiva que el objeto del editor de metadatos, para determinar si se puede buscar en un punto de un archivo. El valor del atributo de **búsqueda** devuelto por un objeto lector es más preciso.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




