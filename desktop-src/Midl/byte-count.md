---
title: byte_count atributo
description: El atributo \ byte count\ ACF es un atributo de parámetro que asocia un tamaño, en bytes, con el área de memoria \_ indicada por el puntero.
ms.assetid: 7e146888-fe7c-461c-8615-70da1e3b12cd
keywords:
- byte_count atributo MIDL
topic_type:
- apiref
api_name:
- byte_count
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffd42e27be4768fc0817aa76bb366429e236b3a82c45d081a05485b8520a23a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807846"
---
# <a name="byte_count-attribute"></a>atributo \_ byte count

El atributo ACF **\[ \_ de \]** recuento de bytes es un atributo de parámetro que asocia un tamaño, en bytes, al área de memoria indicada por el puntero.

``` syntax
[ function-attribute-list ] function-name(
    [byte_count(length-variable-name)] parameter-name);
    ...);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*function-attribute-list* 
</dt> <dd>

Especifica cero o más atributos de función de ACF.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función definida en el archivo IDL. Se requiere el nombre de la función.

</dd> <dt>

*length-variable-name* 
</dt> <dd>

Especifica el nombre del parámetro [**\[ \] in**](in.md)-only que especifica el tamaño, en bytes, del área de memoria a la que hace referencia *el parámetro-name*.

</dd> <dt>

*parameter-name* 
</dt> <dd>

Especifica el nombre del parámetro de puntero [**\[ out \]**](out-idl.md)-only definido en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El recuento de bytes del **\[ atributo \_ \]** ACF representa una extensión de Microsoft para DCE IDL. Por lo tanto, este atributo no está disponible cuando se usa el modificador del compilador MIDL [**/osf**](-osf.md).

> [!Note]  
> El **\[ atributo \] de recuento** de bytes ya no se admite en la sintaxis BYTE64 debido a la dificultad para calcular el tamaño necesario para todos los parámetros [**\[ out. \]**](out-idl.md)

 

La memoria a la que hace referencia el parámetro de puntero es contigua y no se asigna ni libera mediante el código auxiliar del cliente. Esta característica del atributo **\[ de \_ recuento \]** de bytes permite crear un área de búfer persistente en la memoria del cliente que se puede reutilizar durante más de una llamada al procedimiento remoto.

La capacidad de desactivar la asignación de memoria de código auxiliar de cliente le permite optimizar la aplicación para mejorar la eficacia. Por ejemplo, las **\[ funciones del proveedor \_ \]** de servicios que usan RPC de Microsoft pueden usar el atributo de recuento de bytes. Cuando una aplicación de usuario llama a la API del proveedor de servicios y envía un puntero a un búfer, el proveedor de servicios puede pasar el puntero de búfer a la función remota. El proveedor de servicios puede reutilizar el búfer durante varias llamadas remotas sin forzar al usuario a volver a asignación del área de memoria.

El área de memoria puede contener estructuras de datos complejas que constan de varios punteros. Dado que el área de memoria es contigua, la aplicación no tiene que realizar varias llamadas para liberar individualmente cada puntero y estructura. En su lugar, puede asignar o liberar el área de memoria con una llamada a la asignación de memoria o a la rutina libre.

El búfer debe ser un [**\[ parámetro \]**](out-idl.md)de solo salida, mientras que la longitud del búfer en bytes debe ser [**\[ un parámetro in \]**](in.md)-only.

Especifique un búfer lo suficientemente grande como para contener todos los [**\[ parámetros de \]**](out-idl.md) salida. Debido al relleno oculto, use valores sobreestimados en lugar de recuentos exactos. Por ejemplo, los punteros de 4 bytes se desmarshalen en un límite alineado de 4 bytes en plataformas de 32 bits y punteros de 8 bytes en un límite de 8 bytes en plataformas de 64 bits. Por lo tanto, el relleno de alineación que realizarán los códigos auxiliares debe tenerse en cuenta en el espacio del búfer. Además, los niveles de empaquetado usados durante la compilación en lenguaje C pueden variar. Use un valor de recuento de bytes que tiene en cuenta los bytes de empaquetado adicionales agregados para el nivel de empaquetado utilizado durante la compilación en lenguaje C. Una práctica segura que abarca tanto las plataformas de 32 bits como las de 64 bits es suponer que cada objeto que entra en el bloque de memoria grande comienza en una dirección que es un múltiplo de 8.

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

[**En**](in.md)
</dt> <dt>

[**length \_ es**](length-is.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**el \_ tamaño es**](size-is.md)
</dt> </dl>

 

 




