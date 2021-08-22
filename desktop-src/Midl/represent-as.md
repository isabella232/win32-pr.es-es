---
title: represent_as atributo
description: El atributo \ represent as\ ACF asocia un tipo local con nombre en el repr-type del idioma de destino a un tipo de transferencia denominado-type que se transfiere entre el cliente \_ y el servidor.
ms.assetid: ae44d220-e8f3-47a3-8f5e-a2668ac75411
keywords:
- represent_as atributo MIDL
topic_type:
- apiref
api_name:
- represent_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c76576a7d6710c54573ff78186b3cf6d347afc8c4c242fd6e4c1d49865fb521f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146368"
---
# <a name="represent_as-attribute"></a>representar \_ como atributo

El **\[ atributo representar \_ como \]** ACF asocia un tipo local con nombre en el *repr-type* del idioma de destino a un tipo de transferencia *denominado-type* que se transfiere entre el cliente y el servidor.

``` syntax
typedef [represent_as(repr-type) [[ , type-attribute-list ]] ] named-type; 
void __RPC_USER named-type_from_local (
  repr-type __RPC_FAR * ,
  named-type __RPC_FAR * __RPC_FAR * );
void __RPC_USER named-type_to_local (
  named-type __RPC_FAR * ,
  repr-type __RPC_FAR * ); void __RPC_USER named-type _free_inst ( named-type __RPC_FAR * ); void __RPC_USER named-type _free_local ( repr-type __RPC_FAR * );
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*named-type* 
</dt> <dd>

Especifica el tipo de datos de transferencia con nombre que se transfiere entre el cliente y el servidor.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Especifica uno o varios atributos que se aplican al tipo. Separe varios atributos con comas.

</dd> <dt>

*repr-type* 
</dt> <dd>

Especifica el tipo local representado en el idioma de destino que se presenta a las aplicaciones cliente y servidor.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Cuando se **\[ usa representar \_ como \]**, debe proporcionar rutinas que se conviertan entre los tipos de transferencia local y y la memoria libre usada para contener los datos convertidos. El **\[ atributo represent \_ as \]** indica a los códigos auxiliares que llamen a las rutinas de conversión proporcionadas por el usuario.

El tipo con *nombre transferido* debe resolverse en un tipo base MIDL, un tipo predefinido o un identificador de tipo. Para obtener más información, vea [MidL Base Types](midl-base-types.md).

Debe proporcionar las rutinas siguientes:



| Nombre de rutina                   | Descripción                                                                                                                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *named \_ type** \_ de \_ local** | Convierte los datos del tipo local al tipo de red. La rutina asigna memoria para el tipo de datos de red, incluida la memoria para los datos a los que hacen referencia los punteros en el tipo de datos de red.              |
| *named \_ type** \_ a \_ local**   | Convierte los datos del tipo de red al tipo local. La rutina es responsable de asignar memoria para los datos a los que hacen referencia los punteros en el tipo local. RPC asigna memoria para el propio tipo local. |
| *named \_ type** \_ local \_ gratis** | Libera la memoria asignada para los datos a los que hacen referencia los punteros del tipo local. RPC libera memoria para el propio tipo.                                                                                             |
| *named \_ type" \_ free \_ inst**  | Libera la memoria asignada para los datos a los que hacen referencia los punteros en el tipo de red y para el propio tipo de red.                                                                                            |



 

El código auxiliar de cliente llama a *named-type** desde \_ \_ local** para asignar espacio para el tipo transmitido y traducir los datos del tipo local al tipo de red. El código auxiliar del servidor asigna espacio para el tipo de datos original y llama a *named-type** a \_ \_ local** para traducir los datos del tipo de red al tipo local.

Tras la devolución del código de aplicación, los códigos auxiliares de cliente y servidor llaman a *named-type+ \_ free \_ inst** para desasignar el almacenamiento para el tipo de red. El código auxiliar de cliente *llama a named-type y \_ libera \_ local** para desasignar el almacenamiento devuelto por la rutina.

Los siguientes tipos no pueden tener una **\[ representación \_ como \]** atributo:

-   Matrices conformes, variables o conformes
-   Estructuras en las que el último miembro es una matriz compatible (una estructura compatible)
-   Punteros o tipos que contienen un puntero
-   Canalizaciones o tipos que contienen canalizaciones
-   Tipos que se usan como tipo base para una canalización
-   Los tipos [**predefinidos controlan \_ t**](handle-t.md), [**void**](void.md)
-   Tipos que tienen el [**\[ atributo handle \]**](handle.md)

## <a name="examples"></a>Ejemplos

``` syntax
//these data types defined in .IDL or elsewhere
typedef struct  _lbox 
{ 
    long         data; 
    struct _lbox *next; 
} lbox; 
typedef [ref] lbox *PBOX_LOC; 
typedef long LONG4[4]; 
 
//in .ACF file :
interface iface
{
    typedef  [ represent_as(PBOX_LOC) ]  LONG4; 
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Matrices**](arrays-1.md)
</dt> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**handle \_ t**](handle-t.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 




