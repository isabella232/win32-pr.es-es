---
title: public (atributo)
description: El atributo \ public\ incluye un alias declarado con la palabra clave typedef en la biblioteca de tipos.
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
ms.openlocfilehash: 9f8e4944404bccc734594f3847c0ff9de17e54d0b5bcc444a56abe9b8f1e0eaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328725"
---
# <a name="public-attribute"></a>public (atributo)

El **\[ atributo public \]** incluye un alias declarado con la palabra clave [**typedef**](typedef.md) en la biblioteca de tipos.

``` syntax
typedef [public] data-type identifier;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*tipo de datos* 
</dt> <dd>

Tipo de datos para el que el identificador será un alias.

</dd> <dt>

*identifier* 
</dt> <dd>

Otro nombre por el *que se conocerá el* tipo de datos en el software.

</dd> </dl>

## <a name="remarks"></a>Comentarios

De forma predeterminada, un alias que se declara con [**typedef**](typedef.md) y no tiene ningún otro atributo se trata como una definición y no se incluye en la biblioteca de tipos. **\#** El uso **\[ del atributo \]** public garantiza que el alias se convierte en parte de la biblioteca de tipos.

> [!Note]  
> El compilador MIDL requiere que aplique explícitamente el atributo **\[ public \]** a cada typedef que desee público.

 

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

[**Interfaz**](interface.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 