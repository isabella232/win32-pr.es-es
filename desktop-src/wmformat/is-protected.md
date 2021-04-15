---
title: Is_Protected
description: El \_ atributo is Protected es un atributo de nivel de archivo que especifica si el contenido del archivo se protegió mediante la administración de derechos digitales (DRM).
ms.assetid: 6fe63d9b-67ec-47a8-ba20-657434c7a15b
keywords:
- Is_Protected formato de Windows Media
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ec24eb3e805f93bfd46e40954ce64da73ed774
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105714325"
---
# <a name="is_protected"></a>Está \_ protegido

El atributo **is \_ Protected** es un atributo de nivel de archivo que especifica si el contenido del archivo se protegió mediante la administración de derechos digitales (DRM).

## <a name="global-constant"></a>Constante global

g \_ wszWMProtected

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ bool**

## <a name="remarks"></a>Observaciones

Se trata de un atributo codificado. La recuperación de esta propiedad proporciona la misma información que llamar a [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected).

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no enviará su significado normal a los objetos del SDK de Windows Media Format.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




