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
ms.openlocfilehash: 85ec24eb3e805f93bfd46e40954ce64da73ed774
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572176"
---
# <a name="is_protected"></a>Está \_ protegido

El **atributo Is \_ Protected** es un atributo de nivel de archivo que especifica si el contenido del archivo se protegió mediante administración de derechos digitales (DRM).

## <a name="global-constant"></a>Constante global

g \_ wszWMProtected

## <a name="data-type"></a>Tipo de datos

**WMT \_ TYPE \_ BOOL**

## <a name="remarks"></a>Observaciones

Se trata de un atributo codificado. Al recuperar esta propiedad se proporciona la misma información que llamar a [**WMIsContentProtected.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected)

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no transmitirá su significado normal a los objetos del SDK Windows Media Format.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




