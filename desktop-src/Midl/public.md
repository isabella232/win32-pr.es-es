---
title: public (atributo)
description: El atributo \ Public \ incluye un alias declarado con la palabra clave typedef en la biblioteca de tipos.
ms.assetid: d4e90165-8b0d-47bb-998d-e515226be935
keywords:
- atributo público MIDL
topic_type:
- apiref
api_name:
- public
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8451ddf77b5074dbea609bfed144340dc877c00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651351"
---
# <a name="public-attribute"></a>public (atributo)

El atributo **\[ \] Public** incluye un alias declarado con la palabra clave [**typedef**](typedef.md) en la biblioteca de tipos.

``` syntax
typedef [public] data-type identifier;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*tipo de datos* 
</dt> <dd>

El tipo de datos para el que el identificador será un alias.

</dd> <dt>

*identifier* 
</dt> <dd>

Otro nombre por el que se conocerá el *tipo de datos* en el software.

</dd> </dl>

## <a name="remarks"></a>Observaciones

De forma predeterminada, un alias declarado con [**typedef**](typedef.md) y que no tiene otros atributos se trata como una **\# definición** y no se incluye en la biblioteca de tipos. El uso del atributo **\[ Public \]** garantiza que el alias se convierte en parte de la biblioteca de tipos.

> [!Note]  
> El compilador MIDL requiere que aplique explícitamente el atributo **\[ público \]** a cada TypeDef que desee que sea público.

 

## <a name="examples"></a>Ejemplos

``` syntax
typedef [public] long MEMBERID;
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**interfaz**](interface.md)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 