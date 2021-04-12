---
title: Short (atributo)
description: La palabra clave Short designa un entero de 16 bits.
ms.assetid: 622464a3-0d79-421a-8742-8a3746fe1533
keywords:
- atributo abreviado MIDL
topic_type:
- apiref
api_name:
- short
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b993c830c631b5b95246a7a191388ce897dbaafb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358174"
---
# <a name="short-attribute"></a>Short (atributo)

La palabra clave **Short** designa un entero de 16 bits.

``` syntax
[[ signed | unsigned ]] short [[ int ]] declarator-list;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*lista de declaradores* 
</dt> <dd>

Especifica uno o más declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. (Los declaradores de función y las declaraciones de campo de bits no se permiten en las estructuras que se transmiten en llamadas a procedimientos remotos. Estos declaradores se permiten en estructuras que no se transmiten). Separe varios declaradores con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La palabra clave **Short** puede ir precedida de la palabra clave [**signed**](signed.md) o la palabra clave [**sin signo**](unsigned.md). La palabra clave [**int**](int.md) es opcional y se puede omitir. En el compilador MIDL, un entero corto está firmado de forma predeterminada y es sinónimo de **signed Short int**.

El tipo de entero **corto** es uno de los tipos base del lenguaje IDL. El tipo de entero **Short** puede aparecer como un especificador de tipo en declaraciones [**const**](const.md) , declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como un especificador de tipo de valor devuelto de función y un especificador de tipo de parámetro). Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Inter**](int.md)
</dt> <dt>

[**tal**](long.md)
</dt> <dt>

[**conectado**](signed.md)
</dt> <dt>

[**pequeño**](small.md)
</dt> <dt>

[**sin signo**](unsigned.md)
</dt> </dl>

 

 




