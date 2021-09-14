---
title: Atributo dllname(str)
description: El atributo \ dllname\ define el nombre del archivo DLL que contiene los puntos de entrada de un módulo.
ms.assetid: dbf062ce-9dcc-4cc6-b7cd-cdc5945e399b
keywords:
- atributo dllname(str) MIDL
topic_type:
- apiref
api_name:
- dllname(str)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 990d277db855c2988021d19a0a756c49454546f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159612"
---
# <a name="dllnamestr-attribute"></a>Atributo dllname(str)

El **\[ atributo \] dllname** define el nombre del archivo DLL que contiene los puntos de entrada de un módulo.

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

*uuid-number* 
</dt> <dd>

Especifica un número de identificación único universal para el [**módulo**](module.md).

</dd> <dt>

*filename* 
</dt> <dd>

Especifica una cadena terminada en NULL que contiene la ruta de acceso completa al archivo Dll.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Especifica una lista de cero o más atributos de interfaz MIDL.

</dd> <dt>

*modulename* 
</dt> <dd>

Especifica el nombre que otros componentes de software pueden usar para hacer referencia al módulo.

</dd> <dt>

*elementlist* 
</dt> <dd>

Especifica una o varias instrucciones de definición de elemento de módulo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **\[ atributo \] dllname** es necesario en un módulo.

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

[**Módulo**](module.md)
</dt> <dt>

[**Entrada**](entry.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 