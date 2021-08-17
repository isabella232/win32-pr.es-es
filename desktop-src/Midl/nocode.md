---
title: atributo nocode
description: El atributo \nocode\ se usa en encabezados ACF o con funciones individuales para evitar la generación de código auxiliar de cliente.
ms.assetid: d3b6e4c8-103c-4ea2-8748-11d844fdda97
keywords:
- atributo nocode MIDL
topic_type:
- apiref
api_name:
- nocode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86ec4612bc1bd5db1a8cdcbecdced51911591cdf5c482c83381f86deafd66a9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066965"
---
# <a name="nocode-attribute"></a>atributo nocode

El **\[ atributo \] nocode** se usa en encabezados ACF o con funciones individuales para evitar la generación de código auxiliar de cliente.

``` syntax
[ 
    nocode 
    [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typename; ] 
  [ [ nocode [ , ACF-function-attributes ] ] function-name (
        [ ACF-parameter-attributes ] parameter-name ;
        ...);
  ]
    ...
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Atributos de interfaz ACF* 
</dt> <dd>

Especifica una lista de uno o varios atributos que se aplican a la interfaz en su conjunto. Los atributos válidos incluyen el **\[** [**identificador automático \_ o**](auto-handle.md) **\]** el identificador **\[** [**\_ implícito**](implicit-handle.md) y **\]** **\[** [**código**](code.md) **\]** o **\[ codificación \]**. Cuando hay dos o más atributos de interfaz, deben estar separados por comas.

</dd> <dt>

*interface-name* 
</dt> <dd>

Especifica el nombre de la interfaz. En el modo de compatibilidad con DCE, el nombre de la interfaz debe coincidir con el nombre de la interfaz especificada en el archivo IDL. Cuando se usa el modificador del compilador MIDL [**/acf**](-acf.md), el nombre de la interfaz en el ACF y el nombre de interfaz en el archivo IDL pueden ser diferentes.

</dd> <dt>

*filename-list* 
</dt> <dd>

Especifica una lista de uno o varios nombres de archivo de encabezado del lenguaje C, separados por comas. Se debe proporcionar el nombre de archivo completo, incluida la extensión .

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Especifica una lista de uno o varios atributos, separados por comas, que se aplican al tipo especificado. Los atributos de tipo válidos incluyen **\[** [**asignar**](allocate.md) **\]** .

</dd> <dt>

*Typename* 
</dt> <dd>

Especifica un tipo definido en el archivo IDL. Los atributos de tipo del ACF solo se pueden aplicar a los tipos definidos previamente en el archivo IDL.

</dd> <dt>

*ACF-function-attributes* 
</dt> <dd>

Especifica los atributos que se aplican a la función en su conjunto, como **\[** [**el estado de \_ comm**](comm-status.md) **\]** . Los atributos de función se incluyen entre corchetes. Separe varios atributos de función con comas.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función tal como se define en el archivo IDL.

</dd> <dt>

*ACF-parameter-attributes* 
</dt> <dd>

Especifica los atributos de ACF que se aplican a un parámetro. Tenga en cuenta que se pueden aplicar cero o más atributos al parámetro . Separe varios atributos de parámetro con comas. Los atributos de parámetro ACF se incluyen entre corchetes.

</dd> <dt>

*parameter-name* 
</dt> <dd>

Especifica un parámetro de la función tal como se define en el archivo IDL. Cada parámetro de la función debe especificarse en la misma secuencia y con el mismo nombre que se define en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El **\[ atributo \] nocode** puede aparecer en el encabezado ACF o se puede aplicar a una función individual.

Cuando el **\[ atributo nocode \]** aparece en el encabezado ACF, el código auxiliar de cliente no se genera para ninguna función remota a menos que tenga el atributo **\[** [**de**](code.md) función **\]** de código. Puede invalidar el atributo **\[ nocode \]** en el encabezado de una función individual especificando el atributo **\[ de \]** código como atributo de función.

Cuando el **\[ atributo nocode \]** aparece en la lista de atributos de la función, no se genera ningún código auxiliar de cliente para la función.

El código auxiliar de cliente no se genera cuando:

-   El encabezado ACF incluye el **\[ atributo nocode. \]**
-   El **\[ atributo \] nocode** se aplica a la función.
-   El **\[** [**atributo local**](local.md) **\]** se aplica a la función en el archivo de interfaz.

El **\[** [**código**](code.md) o **\]** el código **\[ nocode \]** pueden aparecer en la lista de atributos de una función y el que elija puede aparecer exactamente una vez.

El **\[ atributo \] nocode** se omite cuando se generan códigos auxiliares de servidor. No se puede aplicar al generar códigos auxiliares de servidor en modo de compatibilidad con DCE.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**identificador \_ automático**](auto-handle.md)
</dt> <dt>

[**Código**](code.md)
</dt> <dt>

[**estado de \_ comm**](comm-status.md)
</dt> <dt>

[**identificador \_ implícito**](implicit-handle.md)
</dt> </dl>

 

 




