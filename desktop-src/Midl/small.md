---
title: atributo small
description: La palabra clave small designa un número entero de 8 bits.
ms.assetid: 368e8836-1baa-4547-a62b-f34ac38bbdb2
keywords:
- MIDL de atributo pequeño
topic_type:
- apiref
api_name:
- small
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec627a083d5f5186a4ce8b6b25b0ebbc7bd56afd3e334e46dc4e4901dde34201
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927405"
---
# <a name="small-attribute"></a>atributo small

La palabra clave **small** designa un número entero de 8 bits.

``` syntax
small identifier-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*identifier-name* 
</dt> <dd>

Especifica un identificador MIDL válido. Los identificadores MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado y deben comenzar con un carácter alfabético o de subrayado.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **palabra** clave small puede ir precedida de la palabra clave [**signed**](signed.md) o la palabra [**clave unsigned**](unsigned.md). La palabra clave [**int**](int.md) es opcional y se puede omitir. Para el compilador MIDL, un entero pequeño se **firma** de forma predeterminada y es sinónimo de **int pequeño con signo.**

El **tipo** entero pequeño es uno de los tipos base del lenguaje IDL. El tipo **entero** pequeño puede aparecer como especificador de tipo en declaraciones [**const,**](const.md) declaraciones [**typedef,**](typedef.md) declaraciones generales y declaradores de función (como especificador return-type de función y como especificador de tipo de parámetro). Para obtener el contexto en el que aparecen los especificadores de tipo, vea [Archivo de definición de interfaz (IDL).](interface-definition-idl-file.md)

El modificador  del compilador MIDL [**/char**](-char.md)puede modificar el signo del tipo pequeño . Para evitar confusiones, especifique el signo del tipo entero con las palabras clave [**signed**](signed.md) [**y unsigned**](unsigned.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**/char**](-char.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**Firmado**](signed.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 




