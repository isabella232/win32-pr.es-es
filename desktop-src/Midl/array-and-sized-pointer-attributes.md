---
title: Atributos array y Sized-Pointer
description: MIDL proporciona un amplio conjunto de características para pasar matrices de datos y punteros a datos. Puede utilizar estos atributos para especificar características de matrices y varios niveles de punteros.
ms.assetid: 482be83f-eb09-40a0-8dd6-a0cbf5dc4485
keywords:
- MIDL, atributos, matriz y puntero de tamaño IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0f9ba435d5c413ea152c2bc9b492486ccc1be94
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904553"
---
# <a name="array-and-sized-pointer-attributes"></a>Atributos array y Sized-Pointer

MIDL proporciona un amplio conjunto de características para pasar matrices de datos y punteros a datos. Puede utilizar estos atributos para especificar características de matrices y varios niveles de punteros.



| Atributo                       | Uso                                                                                                                                                                                                |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**el tamaño \_ es**](size-is.md)     | Especifica la cantidad de memoria que se va a asignar para los punteros de tamaño, los punteros de tamaño a los punteros de tamaño y las matrices de un solo o multidimensional.                                                         |
| [**Max \_ es**](max-is.md)       | Valor máximo de un índice de matriz.                                                                                                                                                                |
| [**la longitud \_ es**](length-is.md) | El número de elementos de matriz que se van a transmitir.                                                                                                                                                      |
| [**el primero \_ es**](first-is.md)   | Índice del primer elemento de la matriz que se va a transmitir.                                                                                                                                              |
| [**última \_ es**](last-is.md)     | Proporciona el índice del último elemento de la matriz que se va a transmitir.                                                                                                                                         |
| [**string**](string.md)        | Indica que la matriz [**Char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**byte**](byte.md) (o equivalente) unidimensional, o el puntero a dicha matriz, se tratará como una cadena. |
| [**range**](range.md)          | Especifica un intervalo de valores permitidos para los argumentos o campos cuyos valores se establecen en tiempo de ejecución.                                                                                                       |



 

MIDL admite tres tipos de punteros: punteros de referencia, punteros únicos y punteros completos. Estos punteros se especifican mediante los atributos de puntero [**ref**](ref.md), [**Unique**](unique.md)y [**ptr**](ptr.md).

Un atributo de puntero se puede aplicar como atributo de tipo. como atributo de campo que se aplica a un miembro de estructura, miembro de unión o parámetro; o como un atributo de función que se aplica al tipo de valor devuelto de la función. El atributo Pointer también puede aparecer con la palabra clave [**\_ default del puntero**](pointer-default.md) .

Para permitir que un parámetro de puntero cambie de valor durante una función remota, debe proporcionar otro nivel de direccionamiento indirecto proporcionando varios declaradores de puntero. El atributo de puntero explícito que se aplica al parámetro solo afecta al declarador de puntero más a la derecha del parámetro. Cuando hay varios declaradores de puntero en una declaración de parámetro, el otro declarador tiene como valor predeterminado el atributo de puntero especificado por el atributo [**\_ predeterminado del puntero**](pointer-default.md) . Para aplicar distintos atributos de puntero a varios declaradores de puntero, debe definir los tipos intermedios que especifican los atributos de puntero explícitos.

## <a name="default-pointer-attribute-values"></a>Valores de Pointer-Attribute predeterminados

Cuando no hay ningún atributo de puntero asociado a un puntero que es un parámetro, se supone que el puntero es un puntero de [**referencia**](ref.md) .

Cuando no hay ningún atributo de puntero asociado a un puntero que sea miembro de una estructura o Unión, el compilador MIDL asigna atributos de puntero mediante las siguientes reglas de prioridad (1 es la más alta):

1.  Atributos aplicados explícitamente al tipo de puntero
2.  Atributos aplicados explícitamente al parámetro o miembro del puntero
3.  El [**atributo \_ predeterminado del puntero**](pointer-default.md) en el archivo IDL que define el tipo.
4.  El [**atributo \_ predeterminado del puntero**](pointer-default.md) en el archivo IDL que importa el tipo.
5.  [**ptr**](ptr.md) (modo OSF); [**Unique**](unique.md) (modo predeterminado de Microsoft RPC)

Cuando el archivo IDL se compila en modo predeterminado, los archivos importados pueden heredar atributos de puntero de la importación de archivos. Esta característica no está disponible cuando se compila con el conmutador/[**OSF**](-osf.md) . Para obtener más información, consulte [**Import**](import.md).

## <a name="function-return-types"></a>Tipos de valor devueltos de función

Un puntero devuelto por una función debe ser un puntero [**único**](unique.md) o un puntero completo. El compilador MIDL informa de un error si el resultado de una función es un puntero de referencia, ya sea de forma explícita o predeterminada. El puntero devuelto siempre indica un nuevo almacenamiento.

Las funciones que devuelven un valor de puntero pueden especificar un atributo de puntero como atributo de función. Si no hay un atributo de puntero, el puntero de resultado de la función usa el valor proporcionado como atributo [**\_ predeterminado del puntero**](pointer-default.md) .

## <a name="pointer-attributes-in-type-definitions"></a>Atributos de puntero en definiciones de tipo

Cuando se especifica un atributo de puntero en el nivel superior de una instrucción [**typedef**](typedef.md) , el atributo especificado se aplica al declarador de puntero, según lo esperado. Cuando no se especifica ningún atributo de puntero, el declarador de puntero en el nivel superior de una instrucción typedef hereda el tipo de atributo de puntero cuando se usa.

DCE IDL no permite que el mismo atributo de puntero se aplique explícitamente dos veces, por ejemplo, tanto en la declaración de [**definición**](typedef.md) de tipo como en la lista de atributos de parámetros. Cuando se utiliza el modo predeterminado (extensiones de Microsoft) del compilador de MIDL, esta restricción es relajada.

Para obtener una explicación sobre el uso de matrices y punteros MIDL en llamadas a procedimientos remotos, vea [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).

 

 