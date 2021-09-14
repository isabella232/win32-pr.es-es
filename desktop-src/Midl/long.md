---
title: atributo long
description: La palabra clave long designa un entero de 32 bits.
ms.assetid: 5619e482-e3c3-4898-a70b-afd337d2749a
keywords:
- ATRIBUTO LONG MIDL
topic_type:
- apiref
api_name:
- long
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ea9af3bfac85ff375f6d5433b4e9f3ed37d8f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159507"
---
# <a name="long-attribute"></a>atributo long

La **palabra clave long** designa un entero de 32 bits.

``` syntax
[ signed | unsigned ] long [ int ] declarator-list;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*declarator-list* 
</dt> <dd>

Especifica uno o varios declaradores de C estándar, como identificadores, declaradores de puntero y declaradores de matriz. (Los declaradores de función y las declaraciones de campo de bits no se permiten en estructuras que se transmiten en llamadas a procedimientos remotos. Estos declaradores se permiten en estructuras que no se transmiten). Separe varios declaradores con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **palabra clave long** puede ir precedida de la palabra clave [**signed**](signed.md) o la palabra [**clave unsigned**](unsigned.md). La palabra clave [**int**](int.md) es opcional y se puede omitir. Para el compilador MIDL, un entero largo se firma de forma predeterminada y es sinónimo de **signed long int**. En las plataformas de 32 bits, **long** es sinónimo de **int**.

El **tipo** entero long es uno de los tipos base del lenguaje IDL. El **tipo** entero long puede aparecer como especificador de tipo en declaraciones [**const,**](const.md) declaraciones [**typedef,**](typedef.md) declaraciones generales y declaradores de función (como especificador return-type de función y como especificador de tipo de parámetro). Para obtener el contexto en el que aparecen los especificadores de tipo, vea [Archivo de definición de interfaz (IDL).](interface-definition-idl-file.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[**const**](const.md)
</dt> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**hyper**](hyper.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[**Corto**](short.md)
</dt> <dt>

[**Firmado**](signed.md)
</dt> <dt>

[**Pequeño**](small.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> </dl>

 

 




