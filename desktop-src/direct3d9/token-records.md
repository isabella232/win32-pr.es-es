---
description: En esta sección se describe el formato de los registros de cada uno de los tokens del cojinete de registros. La información se divide en las secciones siguientes.
ms.assetid: 4fdd8339-f660-4389-878a-e7ab067d8508
title: Registros de token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae7e1dcdd36d538ed44205fa51b8e2094d1ff14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714775"
---
# <a name="token-records"></a>Registros de token

En esta sección se describe el formato de los registros de cada uno de los tokens del cojinete de registros. La información se divide en las secciones siguientes.

-   [nombre del TOKEN \_](/windows)
-   [cadena de TOKEN \_](/windows)
-   [entero de TOKEN \_](/windows)
-   [GUID de TOKEN \_](/windows)
-   [lista de enteros de TOKEN \_ \_](/windows)
-   [\_lista de Float de token \_](/windows)

## <a name="token_name"></a>nombre del TOKEN \_

Un registro de longitud variable. El token va seguido de un valor de recuento que especifica el número de bytes que siguen en el campo de nombre. Un nombre ASCII de recuento de longitud completa el registro.



| Campo | Tipo       | Tamaño (bytes) | Contenido                       |
|-------|------------|--------------|--------------------------------|
| token | WORD       | 2            | nombre del token \_                    |
| count | DWORD      | 4            | Longitud del campo de nombre, en bytes |
| name  | Matriz de BYTEs | count        | Nombre ASCII                     |



 

## <a name="token_string"></a>cadena de TOKEN \_

Un registro de longitud variable. El token va seguido de un valor de recuento que especifica el número de bytes que siguen en el campo de cadena. Una cadena ASCII de recuento de longitud continúa el registro, que se completa mediante un token de terminación. La elección del terminador viene determinada por los problemas de sintaxis descritos en otros lugares.



| Campo      | Tipo       | Tamaño (bytes) | Contenido                         |
|------------|------------|--------------|----------------------------------|
| token      | WORD       | 2            | cadena de token \_                    |
| count      | DWORD      | 4            | Longitud del campo de cadena en bytes  |
| String@     | Matriz de BYTEs | count        | Cadena ASCII                     |
| terminado | DWORD      | 4            | \_punto y \_ coma del token |



 

## <a name="token_integer"></a>entero de TOKEN \_

Un registro de longitud fija. El token va seguido del valor entero requerido.



| Campo | Tipo  | Tamaño (bytes) | Contenido       |
|-------|-------|--------------|----------------|
| token | WORD  | 2            | entero de tOKEN \_ |
| Valor | DWORD | 4            | Entero único |



 

## <a name="token_guid"></a>GUID de TOKEN \_

Un registro de longitud fija. El token va seguido de los cuatro campos de datos tal y como se define en el estándar de OSF DCE.



| Campo | Tipo       | Tamaño (bytes) | Contenido          |
|-------|------------|--------------|-------------------|
| token | WORD       | 2            | GUID de tOKEN \_       |
| Data1 | DWORD      | 4            | Campo de datos UUID 1 |
| Data2 | WORD       | 2            | Campo de datos UUID 2 |
| Data3 | WORD       | 2            | Campo de datos UUID 3 |
| Data4 | Matriz de BYTEs | 8            | Campo de datos UUID 4 |



 

## <a name="token_integer_list"></a>lista de enteros de TOKEN \_ \_

Un registro de longitud variable. El token va seguido de un valor de recuento que especifica el número de enteros que siguen en el campo de lista. Por motivos de eficacia, las listas de enteros consecutivas se deben crear en una sola lista.



| Campo | Tipo  | Tamaño (bytes) | Contenido                         |
|-------|-------|--------------|----------------------------------|
| token | WORD  | 2            | lista de enteros de tOKEN \_ \_             |
| count | DWORD | 4            | Número de enteros en el campo de lista |
| list  | DWORD | 4 x recuento    | Lista de enteros                     |



 

## <a name="token_float_list"></a>\_lista de Float de token \_

Un registro de longitud variable. El token va seguido de un valor de recuento que especifica el número de valores float o Double que siguen en el campo de lista. El valor de Float sizespecified en el encabezado de archivo determina el tamaño del valor de punto flotante (float o Double). Por motivos de eficacia, las listas de punto flotante de TOKENs consecutivos \_ \_ deben crearse en una sola lista.



| Campo | Tipo               | Tamaño (bytes)   | Contenido                                  |
|-------|--------------------|----------------|-------------------------------------------|
| token | WORD               | 2              | \_lista de Float de tOKEN \_                        |
| count | DWORD              | 4              | Número de valores float o Double en el campo de lista |
| list  | matriz float/double | número 4 u 8 x | Lista de valores float o Double                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificación binaria](binary-encoding.md)
</dt> </dl>

 

 
