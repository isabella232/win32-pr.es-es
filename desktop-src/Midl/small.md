---
title: atributo pequeño
description: La palabra clave Small designa un número entero de 8 bits.
ms.assetid: 368e8836-1baa-4547-a62b-f34ac38bbdb2
keywords:
- pequeño atributo MIDL
topic_type:
- apiref
api_name:
- small
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a0f106f1be1ba6d0acabf877b5dbefab3eaff6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419395"
---
# <a name="small-attribute"></a>atributo pequeño

La palabra clave **Small** designa un número entero de 8 bits.

``` syntax
small identifier-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador: nombre* 
</dt> <dd>

Especifica un identificador de MIDL válido. Los identificadores de MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado, y deben comenzar por un carácter alfabético o de subrayado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La palabra clave **Small** puede ir precedida de la palabra clave [**signed**](signed.md) o la palabra clave [**sin signo**](unsigned.md). La palabra clave [**int**](int.md) es opcional y se puede omitir. En el compilador de MIDL, un pequeño entero está **firmado** de forma predeterminada y es sinónimo de **int pequeño con signo**.

El tipo entero **pequeño** es uno de los tipos base del lenguaje IDL. El tipo entero **pequeño** puede aparecer como especificador de tipo en declaraciones [**const**](const.md) , declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como especificador de tipo de valor devuelto de función y como especificador de tipo de parámetro). Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).

El signo del tipo **pequeño** puede ser modificado por el modificador del compilador de MIDL [**/Char**](-char.md). Para evitar confusiones, especifique el signo del tipo entero con las palabras clave con [**signo**](signed.md) y sin [**signo**](unsigned.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**/Char**](-char.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Inter**](int.md)
</dt> <dt>

[**tal**](long.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**conectado**](signed.md)
</dt> <dt>

[**sin signo**](unsigned.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




