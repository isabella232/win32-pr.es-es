---
title: Atributos de matriz Sized-Pointer matriz
description: MIDL proporciona un amplio conjunto de características para pasar matrices de datos y punteros a datos. Puede usar estos atributos para especificar características de matrices y varios niveles de punteros.
ms.assetid: 482be83f-eb09-40a0-8dd6-a0cbf5dc4485
keywords:
- MIDL de IDL, atributos, matriz y puntero de tamaño
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0f9ba435d5c413ea152c2bc9b492486ccc1be94
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159680"
---
# <a name="array-and-sized-pointer-attributes"></a>Atributos de matriz Sized-Pointer matriz

MIDL proporciona un amplio conjunto de características para pasar matrices de datos y punteros a datos. Puede usar estos atributos para especificar características de matrices y varios niveles de punteros.



| Atributo                       | Uso                                                                                                                                                                                                |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**el \_ tamaño es**](size-is.md)     | Especifica la cantidad de memoria que se va a asignar para punteros de tamaño, punteros de tamaño a punteros de tamaño y matrices multidimensionales o únicas.                                                         |
| [**max \_ is**](max-is.md)       | Valor máximo de un índice de matriz.                                                                                                                                                                |
| [**length \_ es**](length-is.md) | Número de elementos de matriz que se transmitirán.                                                                                                                                                      |
| [**en \_ primer lugar es**](first-is.md)   | Índice del primer elemento de matriz que se va a transmitir.                                                                                                                                              |
| [**el \_ último es**](last-is.md)     | Proporciona el índice del último elemento de matriz que se va a transmitir.                                                                                                                                         |
| [**Cadena**](string.md)        | Indica que la matriz [**unidimensional char**](char-idl.md), [**wchar \_ t**](wchar-t.md), [**byte**](byte.md) (o equivalente), o el puntero a dicha matriz, se va a controlar como una cadena. |
| [**Gama**](range.md)          | Especifica un intervalo de valores permitidos para argumentos o campos cuyos valores se establecen en tiempo de ejecución.                                                                                                       |



 

MIDL admite tres tipos de punteros: punteros de referencia, punteros únicos y punteros completos. Estos punteros se especifican mediante los atributos de puntero [**ref**](ref.md), [**unique**](unique.md)y [**ptr**](ptr.md).

Un atributo de puntero se puede aplicar como atributo de tipo; como atributo de campo que se aplica a un miembro de estructura, miembro de unión o parámetro; o como un atributo de función que se aplica al tipo de valor devuelto de la función. El atributo de puntero también puede aparecer con la palabra [**clave \_ default del**](pointer-default.md) puntero.

Para permitir que un parámetro de puntero cambie de valor durante una función remota, debe proporcionar otro nivel de direccionamiento indirecto mediante el suministro de varios declaradores de puntero. El atributo de puntero explícito aplicado al parámetro solo afecta al declarador de puntero más a la derecha para el parámetro . Cuando hay varios declaradores de puntero en una declaración de parámetro, los demás declaradores tienen como valor predeterminado el atributo de puntero especificado por el atributo [**\_ predeterminado del**](pointer-default.md) puntero. Para aplicar atributos de puntero diferentes a varios declaradores de puntero, debe definir tipos intermedios que especifiquen los atributos de puntero explícitos.

## <a name="default-pointer-attribute-values"></a>Valores de Pointer-Attribute predeterminados

Cuando no hay ningún atributo de puntero asociado a un puntero que es un parámetro, se supone que el puntero es un [**puntero ref.**](ref.md)

Cuando no hay ningún atributo de puntero asociado a un puntero que sea miembro de una estructura o unión, el compilador midl asigna atributos de puntero mediante las siguientes reglas de prioridad (1 es la más alta):

1.  Atributos aplicados explícitamente al tipo de puntero
2.  Atributos aplicados explícitamente al parámetro de puntero o al miembro
3.  Atributo [**predeterminado \_ de**](pointer-default.md) puntero en el archivo IDL que define el tipo
4.  Atributo [**predeterminado \_ de**](pointer-default.md) puntero en el archivo IDL que importa el tipo
5.  [**ptr**](ptr.md) (modo osf); [**unique**](unique.md) (modo predeterminado de RPC de Microsoft)

Cuando el archivo IDL se compila en modo predeterminado, los archivos importados pueden heredar atributos de puntero de la importación de archivos. Esta característica no está disponible cuando se compila mediante el modificador [**/osf.**](-osf.md) Para obtener más información, vea [**importar**](import.md).

## <a name="function-return-types"></a>Tipos devueltos de función

Un puntero devuelto por una función debe ser [**un puntero único**](unique.md) o un puntero completo. El compilador MIDL notifica un error si el resultado de una función es un puntero de referencia, ya sea explícitamente o de forma predeterminada. El puntero devuelto siempre indica un nuevo almacenamiento.

Las funciones que devuelven un valor de puntero pueden especificar un atributo de puntero como atributo de función. Si un atributo de puntero no está presente, el puntero de resultado de función usa el valor proporcionado como atributo [**predeterminado \_ del**](pointer-default.md) puntero.

## <a name="pointer-attributes-in-type-definitions"></a>Atributos de puntero en definiciones de tipo

Cuando se especifica un atributo de puntero en el nivel superior de una instrucción [**typedef,**](typedef.md) el atributo especificado se aplica al declarador de puntero, según lo previsto. Cuando no se especifica ningún atributo de puntero, los declaradores de puntero en el nivel superior de una instrucción typedef heredan el tipo de atributo de puntero cuando se usan.

DCE IDL no permite que el mismo atributo de puntero se aplique explícitamente dos veces, por ejemplo, en la declaración [**typedef**](typedef.md) y la lista de atributos de parámetro. Cuando se usa el modo predeterminado (extensiones de Microsoft) del compilador MIDL, esta restricción es relajada.

Para obtener una explicación del uso de matrices y punteros MIDL en llamadas a procedimientos remotos, vea [Matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).

 

 