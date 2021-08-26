---
title: WM/UniqueFileIdentifier
description: El atributo WM/UniqueFileIdentifier contiene un identificador de archivo único para el contenido.
ms.assetid: 3f90dd5c-0f3d-451a-a454-f8d7f25b6201
keywords:
- Formato multimedia de Windows WM/UniqueFileIdentifier
topic_type:
- apiref
api_name:
- WM/UniqueFileIdentifier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df336fd1f2ee8afde2c79672977084893b2929133af790ff6e2f4cbe544e1d53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928845"
---
# <a name="wmuniquefileidentifier"></a>WM/UniqueFileIdentifier

El **atributo WM/UniqueFileIdentifier** contiene un identificador de archivo único para el contenido.

## <a name="global-constant"></a>Constante global

g \_ wszWMUniqueFileIdentifier

## <a name="data-type"></a>Tipo de datos

**CADENA \_ DE TIPO \_ WM**

## <a name="remarks"></a>Comentarios

El identificador de archivo único es una cadena genérica que pueden usar las aplicaciones y los servicios para identificar de forma única el archivo. La cadena contiene valores arbitrarios delimitados por punto y coma. Nunca debe borrar este atributo. Puede anexar valores y quitar sus propios valores, pero todos los demás se deben dejar sin modificar.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




