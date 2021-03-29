---
title: atributo de hipertexto
description: La palabra clave Hyper indica un entero de 64 bits que se puede declarar como con signo o sin signo.
ms.assetid: cadcacc7-8eea-4ce2-b69f-98a1d8bafeaa
keywords:
- hiperatributo MIDL
topic_type:
- apiref
api_name:
- hyper
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57da7c0d54e5b9ffcd47f76b22825d13b0a8cff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783605"
---
# <a name="hyper-attribute"></a>atributo de hipertexto

La palabra clave **Hyper** indica un entero de 64 bits que se puede declarar como con signo o sin signo.

``` syntax
[ signed | unsigned ] hyper [ int ] declarator-list;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*lista de declaradores* 
</dt> <dd>

Especifica uno o más declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. (Los declaradores de función y las declaraciones de campo de bits no se permiten en las estructuras que se transmiten en llamadas a procedimientos remotos. Estos declaradores se permiten en estructuras que no se transmiten). Separe varios declaradores con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **hipertipo es uno de los tipos** base del lenguaje de definición de interfaz (IDL). El  hipertipo puede aparecer como un especificador de tipo en declaraciones [**const**](const.md) , declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como un especificador de tipo de valor devuelto de función y como especificador de tipo de parámetro). Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).

> [!Note]  
> En las plataformas de 16 bits, el compilador MIDL reemplaza los hiperenteros sin signo con **MIDL \_ uhyper**. Esto permite definir interfaces con hiperenteros sin signo en plataformas que no admiten directamente enteros de 64 bits. **MIDL \_ uhyper** se define en los archivos de encabezado de RPC.

 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




