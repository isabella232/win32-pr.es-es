---
title: Is_Trusted
description: El atributo Es de confianza es un atributo de nivel de archivo que especifica si la dirección URL de adquisición de \_ licencias del archivo es de confianza.
ms.assetid: 7b383b45-e992-4a07-af0b-9ef220ddd9af
keywords:
- Is_Trusted windows Media Format
topic_type:
- apiref
api_name:
- Is_Trusted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e255c91c5779eb44da8e587601fdfd9264f10888a46a7f216ae2af619ff9f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118198281"
---
# <a name="is_trusted"></a>Es \_ de confianza

El **atributo Es \_ de** confianza es un atributo de nivel de archivo que especifica si la dirección URL de adquisición de licencias del archivo es de confianza.

## <a name="global-constant"></a>Constante global

g \_ wszWMTrusted

## <a name="data-type"></a>Tipo de datos

**WMT \_ TYPE \_ BOOL**

## <a name="remarks"></a>Comentarios

Se trata de un atributo codificado.

Antes de navegar a una dirección URL de adquisición de licencias contenida en un archivo protegido con DRM, una aplicación debe comprobar primero que esta propiedad es true. Si es false, la aplicación debe notificar al usuario que la dirección URL posiblemente se ha alterado.

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no transmitirá su significado normal a los objetos del SDK Windows Media Format.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




