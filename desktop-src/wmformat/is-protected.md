---
title: Is_Protected
description: El atributo Is Protected es un atributo de nivel de archivo que especifica si el contenido del archivo se \_ protegió mediante administración de derechos digitales (DRM).
ms.assetid: 6fe63d9b-67ec-47a8-ba20-657434c7a15b
keywords:
- Is_Protected windows Media Format
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0759dfc781409a1331403c3b02c2645f6ad843925584eab2a55f31a0c8d31af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847422"
---
# <a name="is_protected"></a>Está \_ protegido

El **atributo Is \_ Protected** es un atributo de nivel de archivo que especifica si el contenido del archivo se protegió mediante administración de derechos digitales (DRM).

## <a name="global-constant"></a>Constante global

g \_ wszWMProtected

## <a name="data-type"></a>Tipo de datos

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Comentarios

Se trata de un atributo codificado. Recuperar esta propiedad proporciona la misma información que llamar a [**WMIsContentProtected.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected)

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no transmitirá su significado normal a los objetos del SDK Windows Media Format.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




