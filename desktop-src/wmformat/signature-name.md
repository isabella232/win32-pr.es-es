---
title: Signature_Name
description: El atributo \_ Signature Name contiene el nombre en el certificado utilizado para firmar el archivo. Este atributo solo es válido si el atributo Is \_ Trusted está establecido en True.
ms.assetid: 3f3ab10c-731b-4075-8f73-3c2e62e010b9
keywords:
- Signature_Name windows Media Format
topic_type:
- apiref
api_name:
- Signature_Name
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bff0516353468733ef5c834d51dddc7bbc85e322d98b82929e092913bc375a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845856"
---
# <a name="signature_name"></a>Nombre de \_ la firma

El **atributo \_ Signature Name** contiene el nombre en el certificado utilizado para firmar el archivo. Este atributo solo es válido si el [**atributo Is \_ Trusted**](is-trusted.md) está establecido en True.

## <a name="global-constant"></a>Constante global

g \_ wszWMSignature \_ Name

## <a name="data-type"></a>Tipo de datos

**CADENA DE TIPO WMT \_ \_**

## <a name="remarks"></a>Comentarios

Se trata de un atributo codificado.

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no transmitirá su significado normal a los objetos del SDK Windows Media Format.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




