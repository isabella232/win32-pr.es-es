---
title: HasAttachedImages
description: El atributo HasAttachedImages es un atributo de nivel de archivo que especifica si el archivo es un archivo MP3 con fotogramas APIC ID3 asociados.
ms.assetid: 5c45f61c-3149-4b1b-b5de-f5817cc48c02
keywords:
- Formato multimedia de Windows HasAttachedImages
topic_type:
- apiref
api_name:
- HasAttachedImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ec38d0961ffc6ffc50434cdecf69e6dde663dfeaff5e331455a9575b3426e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930865"
---
# <a name="hasattachedimages"></a>HasAttachedImages

El **atributo HasAttachedImages** es un atributo de nivel de archivo que especifica si el archivo es un archivo MP3 con fotogramas APIC ID3 asociados.

## <a name="global-constant"></a>Constante global

g \_ wszWMHasAttachedImages

## <a name="data-type"></a>Tipo de datos

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Comentarios

Se trata de un atributo codificado.

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no transmitirá su significado normal a los objetos del SDK Windows Media Format.

**HasAttachedImages** se diseñó para informar a una aplicación de que las imágenes estaban presentes para que se pudieran recuperar mediante la [**interfaz IWMImageInfo.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) Ahora que las imágenes se admiten mediante el [**atributo WM/Picture,**](wmpicture.md) **hasAttachedImages** ya no es necesario.

Para determinar si un archivo contiene imágenes, llame a [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) especificando el **atributo WM/Picture.**

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




