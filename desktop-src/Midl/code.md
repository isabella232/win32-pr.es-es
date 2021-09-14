---
title: atributo de código
description: El atributo \code\ ACF hace que el código auxiliar de cliente se genere para las funciones remotas.
ms.assetid: 735a8c25-29d4-4073-a2db-88bc8615ccc1
keywords:
- atributo de código MIDL
topic_type:
- apiref
api_name:
- code
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa041859c0bffca2771695b7055105b8ae846221
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159652"
---
# <a name="code-attribute"></a>atributo de código

El **\[ atributo \]** ACF del código hace que se genere código auxiliar de cliente para las funciones remotas.

``` syntax
[
    code [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typenam; ]
  [ [code [ , ACF-function-attributes ]] function-name (
            [ ACF-parameter-attributes ] parameter-name,
        ...);
  ]
    ...
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Atributos de interfaz ACF* 
</dt> <dd>

Especifica una lista de uno o varios atributos que se aplican a la interfaz en su conjunto. Entre los atributos válidos se incluyen el identificador [**\[ \_ automático \]**](auto-handle.md) [**\[ o el identificador \_ implícito \]**](implicit-handle.md) **\[ y el \]** código , la [**\[ codificación nocode \]**](nocode.md)o la [**\[ optimización de \]**](optimize.md). Cuando hay dos o más atributos de interfaz, deben estar separados por comas.

</dd> <dt>

*interface-name* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

*filename-list* 
</dt> <dd>

Especifica una lista de uno o varios nombres de archivo de encabezado C, separados por comas. Debe proporcionar el nombre de archivo completo, incluida la extensión .

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Especifica una lista de uno o varios atributos, separados por comas, que se aplican al tipo especificado. Los atributos de tipo [**\[ válidos incluyen allocate \]**](allocate.md) y represent [**\[ \_ as \]**](represent-as.md).

</dd> <dt>

*Typename* 
</dt> <dd>

Especifica un tipo definido en el archivo IDL. Los atributos de tipo del ACF solo se pueden aplicar a los tipos definidos previamente en el archivo IDL.

</dd> <dt>

*ACF-function-attributes* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función en su conjunto, como [**\[ el estado de \_ comm \]**](comm-status.md). Los atributos de función se incluyen entre corchetes. Separe varios atributos de función con comas.

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre de la función tal como se define en el archivo IDL.

</dd> <dt>

*ACF-parameter-attributes* 
</dt> <dd>

Especifica los atributos de ACF que se aplican a un parámetro. Tenga en cuenta que se pueden aplicar cero, uno o más atributos al parámetro . Separe varios atributos de parámetro con comas. Los atributos de parámetro ACF se incluyen entre corchetes.

</dd> <dt>

*parameter-name* 
</dt> <dd>

Especifica un parámetro de la función tal como se define en el archivo IDL. Cada parámetro de la función debe especificarse en la misma secuencia y con el mismo nombre que se define en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **\[ atributo \]** de código puede aparecer en el encabezado ACF o aplicarse a una función individual.

Cuando el **\[ atributo de \]** código aparece en el encabezado ACF, se genera código auxiliar de cliente para todas las funciones remotas que no tienen el atributo de función [**\[ nocode. \]**](nocode.md) Puede invalidar el atributo **\[ de código \]** en el encabezado de una función individual especificando el atributo **\[ nocode \]** como atributo de función.

Cuando el **\[ atributo de \]** código aparece en la lista de atributos de la función remota, se genera código auxiliar de cliente para la función. El código auxiliar de cliente no se genera cuando:

-   El encabezado ACF incluye el [**\[ atributo nocode. \]**](nocode.md)
-   El [**\[ atributo \] nocode**](nocode.md) se aplica a la función.
-   El [**\[ atributo local \]**](local.md) se aplica a la función en el archivo de interfaz.

El **\[ \] código** o [**\[ el código nocode \]**](nocode.md) pueden aparecer en la lista de atributos de función o interfaz, pero el que elija solo puede aparecer una vez en la lista.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**identificador \_ automático**](auto-handle.md)
</dt> <dt>

[**estado de \_ comm**](comm-status.md)
</dt> <dt>

[**identificador \_ implícito**](implicit-handle.md)
</dt> <dt>

[**Local**](local.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**Optimizar**](optimize.md)
</dt> <dt>

[**representar \_ como**](represent-as.md)
</dt> </dl>

 

 




