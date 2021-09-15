---
title: Signature_Name
description: El atributo \_ Signature Name contiene el nombre en el certificado utilizado para firmar el archivo. Este atributo solo es válido si el atributo Es \_ de confianza está establecido en True.
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
ms.openlocfilehash: af378671a570dd9ffc58021081b3925d3dca21af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570204"
---
# <a name="signature_name"></a>Nombre de \_ la firma

El **atributo \_ Signature Name** contiene el nombre en el certificado utilizado para firmar el archivo. Este atributo solo es válido si [**el atributo Es \_ de**](is-trusted.md) confianza está establecido en True.

## <a name="global-constant"></a>Constante global

g \_ wszWMSignature \_ Name

## <a name="data-type"></a>Tipo de datos

**CADENA DE TIPO WMT \_ \_**

## <a name="remarks"></a>Observaciones

Se trata de un atributo codificado.

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no transmitirá su significado normal a los objetos del SDK Windows Media Format.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




