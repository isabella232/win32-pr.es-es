---
title: atributo short
description: La palabra clave short designa un entero de 16 bits.
ms.assetid: 622464a3-0d79-421a-8742-8a3746fe1533
keywords:
- MIDL de atributo corto
topic_type:
- apiref
api_name:
- short
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb107b818d2d89717535996d95b580df5a2d49ad0a72aef97de5d6111a0e90d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066745"
---
# <a name="short-attribute"></a>atributo short

La **palabra** clave short designa un entero de 16 bits.

``` syntax
[[ signed | unsigned ]] short [[ int ]] declarator-list;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*declarator-list* 
</dt> <dd>

Especifica uno o varios declaradores de C estándar, como identificadores, declaradores de puntero y declaradores de matriz. (Los declaradores de función y las declaraciones de campo de bits no se permiten en estructuras que se transmiten en llamadas a procedimientos remotos. Estos declaradores se permiten en estructuras que no se transmiten). Separe varios declaradores con comas.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **palabra clave** short puede ir precedida de la palabra clave [**signed**](signed.md) o la palabra [**clave unsigned**](unsigned.md). La palabra clave [**int**](int.md) es opcional y se puede omitir. Para el compilador MIDL, un entero corto se firma de forma predeterminada y es sinónimo de **signed short int**.

El **tipo** entero corto es uno de los tipos base del lenguaje IDL. El **tipo** entero corto puede aparecer como especificador de tipo en declaraciones [**const,**](const.md) declaraciones [**typedef,**](typedef.md) declaraciones generales y declaradores de función (como un especificador function-return-type y un especificador de tipo de parámetro). Para el contexto en el que aparecen los especificadores de tipo, vea Archivo de [definición de interfaz (IDL).](interface-definition-idl-file.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**Firmado**](signed.md)
</dt> <dt>

[**Pequeño**](small.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> </dl>

 

 




