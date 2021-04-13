---
title: nocode (atributo)
description: El atributo \ nocode \ se usa en encabezados ACF o con funciones individuales para evitar la generación de código auxiliar de cliente.
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
ms.openlocfilehash: 64f5138dc1794e9b2714e5f64762c1af17b47fb2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104357997"
---
# <a name="nocode-attribute"></a>nocode (atributo)

El atributo **\[ nocode \]** se usa en encabezados ACF o en funciones individuales para evitar la generación de código auxiliar de cliente.

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

*ACF-interfaz-atributos* 
</dt> <dd>

Especifica una lista de uno o más atributos que se aplican a la interfaz en conjunto. Entre los atributos válidos se incluyen el **\[** [**\_ controlador auto**](auto-handle.md) **\]** o el **\[** [**\_ identificador implícito**](implicit-handle.md) **\]** y **\[** [**code**](code.md) **\]** o **\[ \] nocode**. Cuando dos o más atributos de interfaz están presentes, deben separarse con comas.

</dd> <dt>

*nombre de interfaz* 
</dt> <dd>

Especifica el nombre de la interfaz. En el modo de compatibilidad con DCE, el nombre de la interfaz debe coincidir con el nombre de la interfaz especificada en el archivo IDL. Cuando se usa el modificador de compilador de MIDL [**/ACF**](-acf.md), el nombre de la interfaz en ACF y el nombre de la interfaz en el archivo IDL pueden ser diferentes.

</dd> <dt>

*nombre de archivo-lista* 
</dt> <dd>

Especifica una lista de uno o más nombres de archivo de encabezado de lenguaje C, separados por comas. Se debe proporcionar el nombre de archivo completo, incluida la extensión.

</dd> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica una lista de uno o varios atributos, separados por comas, que se aplican al tipo especificado. Entre los atributos de tipo válidos se incluyen **\[** [**asignar**](allocate.md) **\]** .

</dd> <dt>

*nombreDeTipo* 
</dt> <dd>

Especifica un tipo definido en el archivo IDL. Los atributos de tipo de ACF solo se pueden aplicar a los tipos definidos anteriormente en el archivo IDL.

</dd> <dt>

*ACF: atributos de función* 
</dt> <dd>

Especifica los atributos que se aplican a la función en su totalidad, como el **\[** [**\_ Estado de COMM**](comm-status.md) **\]** . Los atributos de función se incluyen entre corchetes. Separe varios atributos de función con comas.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función tal y como se define en el archivo IDL.

</dd> <dt>

*ACF-Parameter-Attributes* 
</dt> <dd>

Especifica los atributos ACF que se aplican a un parámetro. Tenga en cuenta que se pueden aplicar cero o más atributos al parámetro. Separe varios atributos de parámetro con comas. Los atributos del parámetro ACF se incluyen entre corchetes.

</dd> <dt>

*nombre de parámetro* 
</dt> <dd>

Especifica un parámetro de la función tal y como se define en el archivo IDL. Cada parámetro de la función se debe especificar en la misma secuencia y usar el mismo nombre que el definido en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo **\[ nocode \]** puede aparecer en el encabezado ACF, o bien se puede aplicar a una función individual.

Cuando el atributo **\[ \] nocode** aparece en el encabezado ACF, no se genera código auxiliar de cliente para ninguna función remota a menos que tenga el atributo de función de **\[** [**código**](code.md) **\]** . Puede invalidar el atributo **\[ nocode \]** en el encabezado de una función individual especificando el atributo **\[ code \]** como un atributo de función.

Cuando el atributo **\[ nocode \]** aparece en la lista de atributos de la función, no se genera ningún código auxiliar de cliente para la función.

El código auxiliar de cliente no se genera cuando:

-   El encabezado ACF incluye el atributo **\[ nocode \]** .
-   El atributo **\[ nocode \]** se aplica a la función.
-   El **\[** atributo [**local**](local.md) **\]** se aplica a la función en el archivo de interfaz.

**\[** [](code.md) **\]** Puede aparecer código o **\[ nocode \]** en la lista de atributos de una función y el que elija puede aparecer exactamente una vez.

El atributo **\[ nocode \]** se omite cuando se generan códigos auxiliares de servidor. No se puede aplicar al generar códigos auxiliares de servidor en modo de compatibilidad de DCE.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**\_identificador automático**](auto-handle.md)
</dt> <dt>

[**codifica**](code.md)
</dt> <dt>

[**Estado de COMM \_**](comm-status.md)
</dt> <dt>

[**\_identificador implícito**](implicit-handle.md)
</dt> </dl>

 

 




