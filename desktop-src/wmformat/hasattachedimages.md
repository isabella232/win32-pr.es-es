---
title: HasAttachedImages
description: El atributo HasAttachedImages es un atributo de nivel de archivo que especifica si el archivo es un archivo MP3 con tramas ID3 de APIC conectadas.
ms.assetid: 5c45f61c-3149-4b1b-b5de-f5817cc48c02
keywords:
- HasAttachedImages formato de Windows Media
topic_type:
- apiref
api_name:
- HasAttachedImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b89c8e8260bac7fa22c50460c57a77d4b3033e6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695542"
---
# <a name="hasattachedimages"></a>HasAttachedImages

El atributo **HasAttachedImages** es un atributo de nivel de archivo que especifica si el archivo es un archivo MP3 con tramas ID3 de APIC conectadas.

## <a name="global-constant"></a>Constante global

g \_ wszWMHasAttachedImages

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ bool**

## <a name="remarks"></a>Observaciones

Se trata de un atributo codificado.

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no enviará su significado normal a los objetos del SDK de Windows Media Format.

**HasAttachedImages** se diseñó para informar a una aplicación de que las imágenes estaban presentes para que se pudieran recuperar mediante la interfaz [**IWMImageInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) . Ahora que se admiten las imágenes mediante el atributo [**WM/imagen**](wmpicture.md) , **HasAttachedImages** ya no es necesario.

Para determinar si un archivo contiene imágenes, llame a [**IWMHeaderInfo3:: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) especificando el atributo **WM/imagen** .

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




