---
title: represent_as atributo)
description: El atributo \ representated \_ as \ ACF asocia un tipo local con nombre en el lenguaje de destino repr-Type con un tipo de transferencia denominado-Type que se transfiere entre el cliente y el servidor.
ms.assetid: ae44d220-e8f3-47a3-8f5e-a2668ac75411
keywords:
- represent_as el atributo MIDL
topic_type:
- apiref
api_name:
- represent_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17d0b8915e75bb3065b394ef76900bd8efb5e0c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076482"
---
# <a name="represent_as-attribute"></a>representar \_ como atributo

El atributo **\[ representa \_ como \]** ACF asocia un tipo local con nombre en el lenguaje de destino *repr-Type* con un tipo *de transferencia denominado-Type* que se transfiere entre el cliente y el servidor.

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

*tipo con nombre* 
</dt> <dd>

Especifica el tipo de datos de transferencia con nombre que se transfiere entre el cliente y el servidor.

</dd> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica uno o más atributos que se aplican al tipo. Separe varios atributos con comas.

</dd> <dt>

*tipo de repr* 
</dt> <dd>

Especifica el tipo local representado en el lenguaje de destino que se presenta a las aplicaciones de cliente y de servidor.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al usar **\[ representar \_ como \]**, debe proporcionar rutinas que conviertan entre los tipos de transferencia local y y que la memoria libre usada para contener los datos convertidos. El atributo **\[ representa \_ como \]** indica al código auxiliar que llame a las rutinas de conversión proporcionadas por el usuario.

El tipo transferido *denominado-Type* debe resolverse en un tipo base de MIDL, un tipo predefinido o en un identificador de tipo. Para obtener más información, vea [tipos base de MIDL](midl-base-types.md).

Debe proporcionar las siguientes rutinas:



| Nombre de rutina                   | Descripción                                                                                                                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *tipo con nombre \_ * * * \_ de \_ local** | Convierte los datos del tipo local al tipo de red. La rutina asigna memoria para el tipo de datos de red, incluida la memoria para los datos a los que hacen referencia los punteros en el tipo de datos de red.              |
| *tipo con nombre \_ * * * \_ a \_ local**   | Convierte los datos del tipo de red al tipo local. La rutina es responsable de la asignación de memoria para los datos a los que hacen referencia los punteros en el tipo local. RPC asigna memoria para el propio tipo local. |
| *tipo con nombre \_ * * \_ * \_ local gratis** | Libera la memoria asignada para los datos a los que hacen referencia los punteros en el tipo local. RPC libera memoria para el propio tipo.                                                                                             |
| *tipo con nombre \_ * * \_ * \_ inst. inst.**  | Libera la memoria asignada para los datos a los que hacen referencia los punteros en el tipo de red y para el propio tipo de red.                                                                                            |



 

El código auxiliar del cliente llama a *denominado-Type * * * \_ desde \_ local** para asignar espacio para el tipo transmitido y para traducir los datos del tipo local al tipo de red. El código auxiliar del servidor asigna espacio para el tipo de datos original y llama al tipo *con nombre * * * \_ a \_ local** para traducir los datos del tipo de red al tipo local.

Al volver del código de la aplicación, el código auxiliar del cliente y del servidor llama a la *función con nombre-tipo * * * \_ Free \_ inst** para desasignar el almacenamiento para el tipo de red. El código auxiliar del cliente llama al *tipo denominado * * * \_ \_ local gratis** para desasignar el almacenamiento devuelto por la rutina.

Los tipos siguientes no pueden tener un atributo **\[ representated \_ as \]** :

-   Matrices conformes, variadas o conformes
-   Estructuras en las que el último miembro es una matriz compatible (una estructura compatible)
-   Punteros o tipos que contienen un puntero
-   Canalizaciones o tipos que contienen canalizaciones
-   Tipos que se usan como tipo base para una canalización
-   Identificador de tipos predefinidos [**\_ t**](handle-t.md), [**void**](void.md)
-   Tipos que tienen el atributo [**\[ Handle \]**](handle.md)

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

[**matrices**](arrays-1.md)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**identificador \_ t**](handle-t.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 




