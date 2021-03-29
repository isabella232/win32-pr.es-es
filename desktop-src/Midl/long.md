---
title: atributo Long
description: La palabra clave Long designa un entero de 32 bits.
ms.assetid: 5619e482-e3c3-4898-a70b-afd337d2749a
keywords:
- Long (atributo) MIDL
topic_type:
- apiref
api_name:
- long
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ea9af3bfac85ff375f6d5433b4e9f3ed37d8f7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994677"
---
# <a name="long-attribute"></a>atributo Long

La palabra clave **Long** designa un entero de 32 bits.

``` syntax
[ signed | unsigned ] long [ int ] declarator-list;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*lista de declaradores* 
</dt> <dd>

Especifica uno o más declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. (Los declaradores de función y las declaraciones de campo de bits no se permiten en las estructuras que se transmiten en llamadas a procedimientos remotos. Estos declaradores se permiten en estructuras que no se transmiten). Separe varios declaradores con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La palabra clave **Long** puede ir precedida de la palabra clave [**signed**](signed.md) o la palabra clave [**sin signo**](unsigned.md). La palabra clave [**int**](int.md) es opcional y se puede omitir. En el compilador de MIDL, un entero largo está firmado de forma predeterminada y es sinónimo de **signed Long int**. En las plataformas de 32 bits, **Long** es sinónimo de **int**.

El tipo entero **largo** es uno de los tipos base del lenguaje IDL. El tipo de entero **largo** puede aparecer como especificador de tipo en declaraciones [**const**](const.md) , declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como especificador de tipo de valor devuelto de función y como especificador de tipo de parámetro). Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**const**](const.md)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**Thread**](hyper.md)
</dt> <dt>

[**Inter**](int.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**conectado**](signed.md)
</dt> <dt>

[**pequeño**](small.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**sin signo**](unsigned.md)
</dt> </dl>

 

 




