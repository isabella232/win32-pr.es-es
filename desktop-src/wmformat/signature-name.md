---
title: Signature_Name
description: El \_ atributo de nombre de firma contiene el nombre del certificado usado para firmar el archivo. Este atributo solo es válido si el \_ atributo is Trusted está establecido en true.
ms.assetid: 3f3ab10c-731b-4075-8f73-3c2e62e010b9
keywords:
- Signature_Name formato de Windows Media
topic_type:
- apiref
api_name:
- Signature_Name
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af378671a570dd9ffc58021081b3925d3dca21af
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784019"
---
# <a name="signature_name"></a>Nombre de la firma \_

El atributo de **\_ nombre de firma** contiene el nombre del certificado usado para firmar el archivo. Este atributo solo es válido si el atributo [**is \_ Trusted**](is-trusted.md) está establecido en true.

## <a name="global-constant"></a>Constante global

g \_ wszWMSignature \_ nombre

## <a name="data-type"></a>Tipo de datos

**\_cadena de tipo WMT \_**

## <a name="remarks"></a>Observaciones

Se trata de un atributo codificado.

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no enviará su significado normal a los objetos del SDK de Windows Media Format.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




