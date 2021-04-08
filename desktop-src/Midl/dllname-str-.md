---
title: atributo DllName (STR)
description: El atributo \ DllName \ define el nombre del archivo DLL que contiene los puntos de entrada de un módulo.
ms.assetid: dbf062ce-9dcc-4cc6-b7cd-cdc5945e399b
keywords:
- DllName (STR) atributo MIDL
topic_type:
- apiref
api_name:
- dllname(str)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 990d277db855c2988021d19a0a756c49454546f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077737"
---
# <a name="dllnamestr-attribute"></a>atributo DllName (STR)

El atributo **\[ DllName \]** define el nombre de la dll que contiene los puntos de entrada de un módulo.

``` syntax
[
    uuid(uuid-number), 
    dllname("filename")
    [, optional-attribute-list]
]
module modulename
{
    elementlist
};
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*UUID-número* 
</dt> <dd>

Especifica un número de identificación único universal para el [**módulo**](module.md).

</dd> <dt>

*filename* 
</dt> <dd>

Especifica una cadena terminada en NULL que contiene la ruta de acceso completa al archivo dll.

</dd> <dt>

*opcional-Attribute-List* 
</dt> <dd>

Especifica una lista de cero o más atributos de la interfaz de MIDL.

</dd> <dt>

*ModuleName* 
</dt> <dd>

Especifica el nombre que otros componentes de software pueden usar para hacer referencia al módulo.

</dd> <dt>

*elementlist* 
</dt> <dd>

Especifica una o más instrucciones de definición de elementos de módulo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo **\[ DllName \]** es obligatorio en un módulo.

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("A meaningful comment"),   
    dllname("HANDY.DLL")
] 
module HandyStuff
{
    /* Module content definitions */
};
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**destina**](module.md)
</dt> <dt>

[**movimientos**](entry.md)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 