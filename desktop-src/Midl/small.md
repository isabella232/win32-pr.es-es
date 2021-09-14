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
ms.openlocfilehash: a5a0f106f1be1ba6d0acabf877b5dbefab3eaff6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159382"
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

## <a name="remarks"></a>Observaciones

La palabra clave **small** puede ir precedida de la palabra clave [**signed**](signed.md) o la palabra [**clave unsigned**](unsigned.md). La palabra clave [**int**](int.md) es opcional y se puede omitir. Para el compilador MIDL, un entero pequeño se **firma de** forma predeterminada y es sinónimo de int pequeño **con signo.**

El **tipo** entero pequeño es uno de los tipos base del lenguaje IDL. El tipo **entero** pequeño puede aparecer como especificador de tipo en declaraciones [**const,**](const.md) declaraciones [**typedef,**](typedef.md) declaraciones generales y declaradores de función (como un especificador return-type de función y como un especificador de tipo de parámetro). Para el contexto en el que aparecen los especificadores de tipo, vea Archivo de [definición de interfaz (IDL).](interface-definition-idl-file.md)

El signo del **tipo pequeño** se puede modificar mediante el modificador del compilador MIDL [**/char**](-char.md). Para evitar confusiones, especifique el signo del tipo entero con las palabras clave [**signed**](signed.md) [**y unsigned**](unsigned.md).

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

[**Largo**](long.md)
</dt> <dt>

[**Corto**](short.md)
</dt> <dt>

[**Firmado**](signed.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 




