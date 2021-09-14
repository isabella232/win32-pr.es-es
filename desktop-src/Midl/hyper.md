---
title: atributo hyper
description: La palabra clave hyper indica un entero de 64 bits que se puede declarar como con signo o sin signo.
ms.assetid: cadcacc7-8eea-4ce2-b69f-98a1d8bafeaa
keywords:
- MIDL de hyper-attribute
topic_type:
- apiref
api_name:
- hyper
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57da7c0d54e5b9ffcd47f76b22825d13b0a8cff9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159558"
---
# <a name="hyper-attribute"></a>atributo hyper

La palabra **clave hyper** indica un entero de 64 bits que se puede declarar como con signo o sin signo.

``` syntax
[ signed | unsigned ] hyper [ int ] declarator-list;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*declarator-list* 
</dt> <dd>

Especifica uno o varios declaradores de C estándar, como identificadores, declaradores de puntero y declaradores de matriz. (Los declaradores de función y las declaraciones de campo de bits no se permiten en estructuras que se transmiten en llamadas a procedimientos remotos. Estos declaradores se permiten en estructuras que no se transmiten). Separe varios declaradores con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **tipo hyper** es uno de los tipos base del lenguaje de definición de interfaz (IDL). El **tipo hyper** puede aparecer como especificador de tipo en declaraciones [**const,**](const.md) declaraciones [**typedef,**](typedef.md) declaraciones generales y declaradores de función (como un especificador function-return-type y como un especificador de tipo de parámetro). Para el contexto en el que aparecen los especificadores de tipo, vea Archivo de [definición de interfaz (IDL).](interface-definition-idl-file.md)

> [!Note]  
> En el caso de las plataformas de 16 bits, el compilador de MIDL reemplaza los hyper-integer sin signo por **MIDL \_ uhyper**. Esto permite definir interfaces con hiper enteros sin signo en plataformas que no admiten directamente enteros de 64 bits. **MIDL \_ se define en** los archivos de encabezado RPC.

 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 




