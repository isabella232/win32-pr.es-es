---
title: byte_count atributo)
description: El atributo @ byte \_ Count \ ACF es un atributo de parámetro que asocia un tamaño, en bytes, con el área de memoria indicada por el puntero.
ms.assetid: 7e146888-fe7c-461c-8615-70da1e3b12cd
keywords:
- byte_count el atributo MIDL
topic_type:
- apiref
api_name:
- byte_count
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d82d34a60ea736d10c8ec5ee8a001370c6b64c6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358210"
---
# <a name="byte_count-attribute"></a>byte \_ Count (atributo)

El atributo ACF de **\[ \_ recuento \] de bytes** es un atributo de parámetro que asocia un tamaño, en bytes, con el área de memoria indicada por el puntero.

``` syntax
[ function-attribute-list ] function-name(
    [byte_count(length-variable-name)] parameter-name);
    ...);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*lista de atributos de función* 
</dt> <dd>

Especifica cero o más atributos de función ACF.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función definida en el archivo IDL. El nombre de la función es obligatorio.

</dd> <dt>

*Length-variable-Name* 
</dt> <dd>

Especifica el nombre del parámetro de solo [**\[ en \]**](in.md)que especifica el tamaño, en bytes, del área de memoria a la que hace referencia el *parámetro-name*.

</dd> <dt>

*nombre de parámetro* 
</dt> <dd>

Especifica el nombre del parámetro de puntero de solo [**\[ salida \]**](out-idl.md)definido en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **\[ \_ número \] de bytes** del atributo ACF representa una extensión de Microsoft para DCE IDL. Por lo tanto, este atributo no está disponible cuando se usa el modificador de compilador MIDL [**/OSF**](-osf.md).

> [!Note]  
> El atributo de **\[ recuento \] de bytes** ya no se admite en la sintaxis de NDR64 debido a la dificultad en la estimación del tamaño necesario para todos los parámetros de [**\[ salida \]**](out-idl.md) .

 

La memoria a la que hace referencia el parámetro de puntero es contigua y no la asigna ni libera el código auxiliar del cliente. Esta característica del atributo **\[ \_ recuento \] de bytes** le permite crear un área de búfer persistente en la memoria del cliente que se puede reutilizar durante más de una llamada al procedimiento remoto.

La capacidad de desactivar la asignación de memoria de código auxiliar de cliente permite optimizar la aplicación para mejorar la eficacia. Por ejemplo, las funciones de proveedor de servicios que usan Microsoft RPC pueden utilizar el atributo de **\[ \_ recuento \] de bytes** . Cuando una aplicación de usuario llama a la API del proveedor de servicios y envía un puntero a un búfer, el proveedor de servicios puede pasar el puntero de búfer a la función remota. El proveedor de servicios puede volver a usar el búfer durante varias llamadas remotas sin forzar al usuario a reasignar el área de memoria.

El área de memoria puede contener estructuras de datos complejas que se componen de varios punteros. Dado que el área de memoria es contiguo, la aplicación no tiene que realizar varias llamadas para liberar cada puntero y estructura de forma individual. En su lugar, puede asignar o liberar el área de memoria con una llamada a la asignación de memoria o la rutina libre.

El búfer debe ser un parámetro de solo [**\[ salida \]**](out-idl.md), mientras que la longitud del búfer en bytes debe ser un parámetro solo [**\[ en \]**](in.md).

Especifique un búfer que sea lo suficientemente grande como para contener todos los parámetros de [**\[ salida \]**](out-idl.md) . Debido al relleno oculto, utilice las sobreestimaciones en lugar de los recuentos exactos. Por ejemplo, no se calculan las referencias de los punteros de 4 bytes en un límite alineado de 4 bytes en plataformas de 32 bits y punteros de 8 bytes en un límite de 8 bytes en plataformas de 64 bits. Por lo tanto, el relleno de alineación que realizará el código auxiliar se debe tener en cuenta en el espacio del búfer. Además, los niveles de empaquetado utilizados durante la compilación del lenguaje C pueden variar. Use un valor de recuento de bytes que tenga en cuenta los bytes de empaquetado adicionales agregados para el nivel de empaquetado usado durante la compilación del lenguaje C. Una práctica segura que abarque las plataformas de 32 bits y las plataformas de 64 bits es suponer que cada objeto que entra en el bloque de gran memoria comienza en una dirección que es un múltiplo de 8.

## <a name="examples"></a>Ejemplos

``` syntax
/* IDL file */ 
HRESULT proc1([in] unsigned long length, 
              [out] struct my_struct * pMyStruct); 
 
/* ACF file */ 
proc1([byte_count(length)] pMyStruct);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**de**](in.md)
</dt> <dt>

[**la longitud \_ es**](length-is.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**enuncia**](out-idl.md)
</dt> <dt>

[**el tamaño \_ es**](size-is.md)
</dt> </dl>

 

 




