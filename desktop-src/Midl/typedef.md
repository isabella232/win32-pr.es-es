---
title: Atributo typedef
description: La palabra clave typedef de IDL permite declaraciones typedef muy similares a las declaraciones typedef del lenguaje C.
ms.assetid: 995a233e-0d07-4051-9f00-d1dc0b563f8f
keywords:
- atributo typedef MIDL
topic_type:
- apiref
api_name:
- typedef
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecfce98e5a83f8d2a5e2499a5ceceba755e68f2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159340"
---
# <a name="typedef-attribute"></a>Atributo typedef

La palabra clave **typedef de** IDL permite declaraciones **typedef** muy similares a las declaraciones **typedef del** lenguaje C.

``` syntax
/* IDL file typedef syntax */
typedef [[ [ idl-type-attribute-list ] ]] type-specifier declarator-list;

/* ACF typedef syntax */
typedef [ acf-type-attribute-list ] typename;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*idl-type-attribute-list* 
</dt> <dd>

Especifica uno o varios atributos que se aplican al tipo. Los atributos de tipo válidos de un archivo IDL incluyen el identificador , el tipo de modificador , transmitir como ; el atributo de puntero **\[** [](handle.md) **\]** **\[** [**\_**](switch-type.md) **\]** **\[** [**\_**](transmit-as.md) **\]** **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md); **\]** **\[** [**\_**](context-handle.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** y el identificador de contexto de atributos de uso , la cadena y omitir . Separe varios atributos con comas.

</dd> <dt>

*type-specifier* 
</dt> <dd>

Especifica un tipo [base,](midl-base-types.md) [**struct**](struct.md), [**union,**](union.md) [**tipo de enumeración**](enum.md) o identificador de tipo. Una especificación de almacenamiento opcional puede *preceder al especificador de tipo*. La [**palabra clave const**](const.md) puede *preceder a type-specifier.*

</dd> <dt>

*declarator-list* 
</dt> <dd>

Especifica declaradores MIDL estándar, como identificadores, declaradores de puntero y declaradores de matriz. Para obtener más información, vea [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers). La *lista de declaradores* consta de uno o varios declaradores, separados por comas.

</dd> <dt>

*acf-type-attribute-list* 
</dt> <dd>

Especifica uno o varios atributos que se aplican al tipo. Los atributos de tipo válidos de un ACF incluyen **\[** [**asignar**](allocate.md) **\]** , **\[** [**codificar**](encode.md)y **\]** **\[** [**descodificar**](decode.md) **\]** .

</dd> <dt>

*Typename* 
</dt> <dd>

Especifica un tipo definido en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La declaración **typedef de** IDL se aumenta para permitirle asociar atributos de tipo a los tipos definidos. Los atributos de tipo válidos incluyen el identificador , el tipo de modificador , transmitir como ; el atributo de puntero **\[** [](handle.md) **\]** **\[** [**\_**](switch-type.md) **\]** **\[** [**\_**](transmit-as.md) **\]** **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md); **\]** **\[** [**\_**](context-handle.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** y el identificador de contexto de los atributos de uso , la cadena y omitir .

La **palabra clave typedef** de un ACF aplica atributos a los tipos definidos en el archivo IDL correspondiente. Por ejemplo, el [**atributo allocate**](allocate.md) type le permite personalizar la asignación y desasignación de memoria tanto por la aplicación como por los códigos auxiliares.

La instrucción **typedef de** ACF aparece como parte del cuerpo de ACF. Tenga en cuenta que la sintaxis **de typedef** de ACF es diferente de la sintaxis de **typedef** de IDL y la sintaxis **typedef del lenguaje** C. No se pueden introducir nuevos tipos en el ACF.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**Matrices**](arrays-1.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**identificador de \_ contexto**](context-handle.md)
</dt> <dt>

[**Decodificar**](decode.md)
</dt> <dt>

[**Codificar**](encode.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**handle**](handle.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Ignorar**](ignore.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Cadena**](string.md)
</dt> <dt>

[**Estructura**](struct.md)
</dt> <dt>

[**tipo \_ de conmutador**](switch-type.md)
</dt> <dt>

[**transmitir \_ como**](transmit-as.md)
</dt> <dt>

[**union**](union.md)
</dt> <dt>

[**Único**](unique.md)
</dt> </dl>

 

 