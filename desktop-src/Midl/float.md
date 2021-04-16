---
title: Float (atributo)
description: La palabra clave Float designa un número de punto flotante de 32 bits.
ms.assetid: dfc94378-13a4-4d34-a254-7ff68f4f9d40
keywords:
- atributo Float de MIDL
topic_type:
- apiref
api_name:
- float
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c82d298506c5117c0643df8ecea841832d5f923
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105685628"
---
# <a name="float-attribute"></a>Float (atributo)

La palabra clave **float** designa un número de punto flotante de 32 bits.

``` syntax
float identifier-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador: nombre* 
</dt> <dd>

Especifica un identificador de MIDL válido. Los identificadores de MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado, y deben comenzar por un carácter alfabético o de subrayado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El tipo **float** es uno de los tipos base del lenguaje de definición de interfaz (IDL). El tipo **float** puede aparecer como un especificador de tipo en declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como un especificador de tipo de valor devuelto de función y un especificador de tipo de parámetro). Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).

El tipo **float** no puede aparecer en las declaraciones [**const**](const.md) .

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**double**](double.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




