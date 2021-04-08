---
title: Is_Trusted
description: El \_ atributo is Trusted es un atributo de nivel de archivo que especifica si la dirección URL de adquisición de licencias en el archivo es de confianza.
ms.assetid: 7b383b45-e992-4a07-af0b-9ef220ddd9af
keywords:
- Is_Trusted formato de Windows Media
topic_type:
- apiref
api_name:
- Is_Trusted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e8dd4fdd638bad0908bb1bbf50135cde5bad6c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994776"
---
# <a name="is_trusted"></a>Es de \_ confianza

El atributo **is \_ Trusted** es un atributo de nivel de archivo que especifica si la dirección URL de adquisición de licencias en el archivo es de confianza.

## <a name="global-constant"></a>Constante global

g \_ wszWMTrusted

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ bool**

## <a name="remarks"></a>Observaciones

Se trata de un atributo codificado.

Antes de navegar a una dirección URL de adquisición de licencias incluida en un archivo protegido con DRM, una aplicación debe comprobar primero si esta propiedad es true. Si es false, la aplicación debe notificar al usuario que es posible que la dirección URL se haya alterado.

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no enviará su significado normal a los objetos del SDK de Windows Media Format.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




