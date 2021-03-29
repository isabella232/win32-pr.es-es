---
title: typedef (atributo)
description: La palabra clave typedef de IDL permite declaraciones TypeDef que son muy similares a las declaraciones typedef del lenguaje C.
ms.assetid: 995a233e-0d07-4051-9f00-d1dc0b563f8f
keywords:
- typedef (atributo) MIDL
topic_type:
- apiref
api_name:
- typedef
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecfce98e5a83f8d2a5e2499a5ceceba755e68f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790006"
---
# <a name="typedef-attribute"></a>typedef (atributo)

La palabra clave **typedef** de IDL permite declaraciones **typedef** que son muy similares a las declaraciones **typedef** del lenguaje C.

``` syntax
/* IDL file typedef syntax */
typedef [[ [ idl-type-attribute-list ] ]] type-specifier declarator-list;

/* ACF typedef syntax */
typedef [ acf-type-attribute-list ] typename;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*IDL-Type-Attribute-List* 
</dt> <dd>

Especifica uno o más atributos que se aplican al tipo. Los atributos de tipo válidos en un archivo IDL incluyen **\[** [](handle.md) **\]** el identificador, **\[** el [**\_ tipo de conmutador**](switch-type.md) **\]** , **\[** la [**transmisión \_ como**](transmit-as.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; y el identificador de contexto de los atributos de uso, la **\[** [**\_**](context-handle.md) **\]** **\[** [**cadena**](string.md) **\]** y la **\[** [**omisión**](ignore.md) **\]** . Separe varios atributos con comas.

</dd> <dt>

*Type-Specifier* 
</dt> <dd>

Especifica un [tipo base](midl-base-types.md), un [**struct**](struct.md), una [**Unión**](union.md), un tipo de [**enumeración**](enum.md) o un identificador de tipo. Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*. La palabra clave [**const**](const.md) puede preceder *a Type-Specifier*.

</dd> <dt>

*lista de declaradores* 
</dt> <dd>

Especifica los declaradores MIDL estándar, como los identificadores, los declaradores de puntero y los declaradores de matriz. Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers). La *lista de declaradores* consta de uno o varios declaradores, separados por comas.

</dd> <dt>

*ACF-tipo-atributo-lista* 
</dt> <dd>

Especifica uno o más atributos que se aplican al tipo. Los atributos de tipo válidos en ACF incluyen **\[** [**asignar**](allocate.md) **\]** , **\[** [**codificar**](encode.md) **\]** y **\[** [**descodificar**](decode.md) **\]** .

</dd> <dt>

*nombreDeTipo* 
</dt> <dd>

Especifica un tipo definido en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La declaración **typedef** de IDL se amplía para que pueda asociar atributos de tipo a los tipos definidos. Entre los atributos de tipo válidos se incluyen **\[** el [**identificador**](handle.md) **\]** , **\[** el [**\_ tipo de conmutador**](switch-type.md) **\]** , **\[** la [**transmisión \_ como**](transmit-as.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; y el identificador de contexto de los atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[** [**String**](string.md) **\]** y **\[** [**Ignore**](ignore.md) **\]** .

La palabra clave **typedef** en ACF aplica atributos a los tipos que se definen en el archivo IDL correspondiente. Por ejemplo, el atributo de tipo [**allocate**](allocate.md) permite personalizar la asignación y desasignación de memoria por la aplicación y el código auxiliar.

La instrucción **typedef** de ACF aparece como parte del cuerpo ACF. Tenga en cuenta que la sintaxis de **typedef** de ACF es diferente de la sintaxis de **typedef** de IDL y la sintaxis de **typedef** del lenguaje C. No se pueden introducir nuevos tipos en el ACF.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**matrices**](arrays-1.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[**descodificar**](decode.md)
</dt> <dt>

[**codificar**](encode.md)
</dt> <dt>

[**enumeración**](enum.md)
</dt> <dt>

[**asa**](handle.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**omitir**](ignore.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**Destructor**](struct.md)
</dt> <dt>

[**tipo de conmutador \_**](switch-type.md)
</dt> <dt>

[**transmitir \_ como**](transmit-as.md)
</dt> <dt>

[**Unión**](union.md)
</dt> <dt>

[**espeficarse**](unique.md)
</dt> </dl>

 

 