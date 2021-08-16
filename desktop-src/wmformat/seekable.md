---
title: Buscable
description: El atributo Seekable es un atributo de nivel de archivo que especifica si una aplicación puede buscar puntos dentro del contenido.
ms.assetid: 9653e368-4782-4506-9c44-54c9406b61b5
keywords:
- Formato multimedia de Windows que se puede buscar
topic_type:
- apiref
api_name:
- Seekable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a254d06b36230bb6920f2f13d646edc5f1cdac75efe15864e0c84ba847cf50f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699991"
---
# <a name="seekable"></a>Buscable

El **atributo Seekable** es un atributo de nivel de archivo que especifica si una aplicación puede buscar puntos dentro del contenido.

## <a name="global-constant"></a>Constante global

g \_ wszWMSeekable

## <a name="data-type"></a>Tipo de datos

**WMT \_ TYPE \_ BOOL**

## <a name="remarks"></a>Comentarios

Se trata de un atributo codificado.

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no transmitirá su significado normal a los objetos del SDK Windows Media Format.

El valor de este atributo para un archivo puede variar en función del objeto que expone la [**interfaz IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) o [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) utilizada para recuperarlo. Esto se debe a que los objetos de lector (sincrónicos y asincrónicos) realizan una comprobación más exhaustiva que el objeto del editor de metadatos para determinar si se puede buscar un punto en un archivo. El **valor del atributo Seekable** devuelto por un objeto de lector es más preciso.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




