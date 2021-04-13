---
title: atributo Code
description: El atributo \ Code \ ACF hace que se genere código auxiliar de cliente para las funciones remotas.
ms.assetid: 735a8c25-29d4-4073-a2db-88bc8615ccc1
keywords:
- código MIDL del atributo Code
topic_type:
- apiref
api_name:
- code
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa041859c0bffca2771695b7055105b8ae846221
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358270"
---
# <a name="code-attribute"></a>atributo Code

El atributo ACF de **\[ código \]** hace que se genere código auxiliar de cliente para las funciones remotas.

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

*ACF-interfaz-atributos* 
</dt> <dd>

Especifica una lista de uno o más atributos que se aplican a la interfaz en conjunto. Entre los atributos válidos se incluyen el [**\[ \_ controlador \] auto**](auto-handle.md) o el [**\[ \_ identificador \] implícito**](implicit-handle.md) y **\[ code \]**, [**\[ \] nocode**](nocode.md)u [**\[ Optimize \]**](optimize.md). Cuando dos o más atributos de interfaz están presentes, deben separarse con comas.

</dd> <dt>

*nombre de interfaz* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

*nombre de archivo-lista* 
</dt> <dd>

Especifica una lista de uno o más nombres de archivo de encabezado C, separados por comas. Debe proporcionar el nombre de archivo completo, incluida la extensión.

</dd> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica una lista de uno o varios atributos, separados por comas, que se aplican al tipo especificado. Entre los atributos de tipo válidos se incluyen [**\[ \] asignar**](allocate.md) y [**\[ representar \_ como \]**](represent-as.md).

</dd> <dt>

*nombreDeTipo* 
</dt> <dd>

Especifica un tipo definido en el archivo IDL. Los atributos de tipo de ACF solo se pueden aplicar a los tipos definidos anteriormente en el archivo IDL.

</dd> <dt>

*ACF: atributos de función* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función en su totalidad, como el [**\[ \_ estado \] de COMM**](comm-status.md). Los atributos de función se incluyen entre corchetes. Separe varios atributos de función con comas.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función tal y como se define en el archivo IDL.

</dd> <dt>

*ACF-Parameter-Attributes* 
</dt> <dd>

Especifica los atributos ACF que se aplican a un parámetro. Tenga en cuenta que se pueden aplicar cero, uno o varios atributos al parámetro. Separe varios atributos de parámetro con comas. Los atributos del parámetro ACF se incluyen entre corchetes.

</dd> <dt>

*nombre de parámetro* 
</dt> <dd>

Especifica un parámetro de la función tal y como se define en el archivo IDL. Cada parámetro de la función se debe especificar en la misma secuencia y con el mismo nombre que el definido en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo **\[ code \]** puede aparecer en el encabezado ACF o aplicarse a una función individual.

Cuando el atributo **\[ code \]** aparece en el encabezado ACF, se genera código auxiliar de cliente para todas las funciones remotas que no tienen el atributo de función [**\[ nocode \]**](nocode.md) . Puede invalidar el atributo **\[ code \]** en el encabezado de una función individual especificando el atributo **\[ nocode \]** como un atributo de función.

Cuando el atributo **\[ code \]** aparece en la lista de atributos de la función remota, se genera código auxiliar de cliente para la función. El código auxiliar de cliente no se genera cuando:

-   El encabezado ACF incluye el atributo [**\[ nocode \]**](nocode.md) .
-   El atributo [**\[ nocode \]**](nocode.md) se aplica a la función.
-   El atributo [**\[ local \]**](local.md) se aplica a la función en el archivo de interfaz.

**\[ Code \]** o [**\[ nocode \]**](nocode.md) pueden aparecer en la lista de atributos de interfaz o función, pero el que elija solo puede aparecer una vez en la lista.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**\_identificador automático**](auto-handle.md)
</dt> <dt>

[**Estado de COMM \_**](comm-status.md)
</dt> <dt>

[**\_identificador implícito**](implicit-handle.md)
</dt> <dt>

[**localizar**](local.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**optimiz**](optimize.md)
</dt> <dt>

[**representar \_ como**](represent-as.md)
</dt> </dl>

 

 




