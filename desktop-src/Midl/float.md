---
title: atributo float
description: La palabra clave float designa un número de punto flotante de 32 bits.
ms.assetid: dfc94378-13a4-4d34-a254-7ff68f4f9d40
keywords:
- MIDL del atributo float
topic_type:
- apiref
api_name:
- float
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c82d298506c5117c0643df8ecea841832d5f923
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159582"
---
# <a name="float-attribute"></a>atributo float

La **palabra clave float** designa un número de punto flotante de 32 bits.

``` syntax
float identifier-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*identifier-name* 
</dt> <dd>

Especifica un identificador MIDL válido. Los identificadores MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado y deben comenzar con un carácter alfabético o de subrayado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **tipo float** es uno de los tipos base del lenguaje de definición de interfaz (IDL). El **tipo float** puede aparecer como especificador de tipo en declaraciones [**typedef,**](typedef.md) declaraciones generales y declaradores de función (como un especificador function-return-type y un especificador de tipo de parámetro). Para obtener el contexto en el que aparecen los especificadores de tipo, vea [Archivo de definición de interfaz (IDL).](interface-definition-idl-file.md)

El **tipo float** no puede aparecer en las [**declaraciones const.**](const.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**Doble**](double.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 




