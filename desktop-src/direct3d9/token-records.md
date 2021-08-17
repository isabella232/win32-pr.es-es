---
description: En esta sección se describe el formato de los registros para cada uno de los tokens que llevan registros. La información se divide en las secciones siguientes.
ms.assetid: 4fdd8339-f660-4389-878a-e7ab067d8508
title: Registros de token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 456ee591f15cac6e6a3d2fecaad3dfca9f0709b39a63d20fe198e591a199f4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797427"
---
# <a name="token-records"></a>Registros de token

En esta sección se describe el formato de los registros para cada uno de los tokens que llevan registros. La información se divide en las secciones siguientes.

-   [NOMBRE DEL \_ TOKEN](/windows)
-   [CADENA DE \_ TOKEN](/windows)
-   [ENTERO \_ DE TOKEN](/windows)
-   [GUID \_ de TOKEN](/windows)
-   [LISTA \_ DE ENTEROS \_ DE TOKEN](/windows)
-   [LISTA \_ DE FLOTANTES \_ DE TOKEN](/windows)

## <a name="token_name"></a>NOMBRE DEL \_ TOKEN

Un registro de longitud variable. El token va seguido de un valor de recuento que especifica el número de bytes siguientes en el campo de nombre. Un nombre ASCII de recuento de longitud completa el registro.



| Campo | Tipo       | Tamaño (bytes) | Contenido                       |
|-------|------------|--------------|--------------------------------|
| token | WORD       | 2            | nombre del \_ token                    |
| recuento | DWORD      | 4            | Longitud del campo de nombre, en bytes |
| name  | Matriz BYTE | recuento        | Nombre ASCII                     |



 

## <a name="token_string"></a>CADENA DE \_ TOKEN

Un registro de longitud variable. El token va seguido de un valor de recuento que especifica el número de bytes que siguen en el campo de cadena. Una cadena ASCII de recuento de longitud continúa el registro, que se completa con un token de terminación. La elección del terminador viene determinada por los problemas de sintaxis que se deban tratar en otra parte.



| Campo      | Tipo       | Tamaño (bytes) | Contenido                         |
|------------|------------|--------------|----------------------------------|
| token      | WORD       | 2            | cadena de \_ token                    |
| recuento      | DWORD      | 4            | Longitud del campo de cadena en bytes  |
| Cadena     | Matriz BYTE | recuento        | Cadena ASCII                     |
| Terminator | DWORD      | 4            | TOKEN \_ SEMICOLON o TOKEN \_ COMMA |



 

## <a name="token_integer"></a>ENTERO \_ DE TOKEN

Un registro de longitud fija. El token va seguido del valor entero requerido.



| Campo | Tipo  | Tamaño (bytes) | Contenido       |
|-------|-------|--------------|----------------|
| token | WORD  | 2            | TOKEN \_ INTEGER |
| Valor | DWORD | 4            | Entero único |



 

## <a name="token_guid"></a>GUID \_ de TOKEN

Un registro de longitud fija. El token va seguido de los cuatro campos de datos definidos por el estándar DCE de OSF.



| Campo | Tipo       | Tamaño (bytes) | Contenido          |
|-------|------------|--------------|-------------------|
| token | WORD       | 2            | GUID de tOKEN \_       |
| Data1 | DWORD      | 4            | Campo de datos UUID 1 |
| Data2 | WORD       | 2            | Campo de datos UUID 2 |
| Data3 | WORD       | 2            | Campo de datos UUID 3 |
| Data4 | Matriz BYTE | 8            | Campo de datos UUID 4 |



 

## <a name="token_integer_list"></a>LISTA \_ DE ENTEROS \_ DE TOKEN

Registro de longitud variable. El token va seguido de un valor count que especifica el número de enteros que siguen en el campo de lista. Para mejorar la eficacia, las listas de enteros consecutivos deben estar compuestas en una sola lista.



| Campo | Tipo  | Tamaño (bytes) | Contenido                         |
|-------|-------|--------------|----------------------------------|
| token | WORD  | 2            | tOKEN \_ INTEGER \_ LISt             |
| recuento | DWORD | 4            | Número de enteros en el campo de lista |
| list  | DWORD | 4 x count    | Lista de enteros                     |



 

## <a name="token_float_list"></a>LISTA \_ FLOTANTE DE \_ TOKENS

Registro de longitud variable. El token va seguido de un valor de recuento que especifica el número de elementos float o double que siguen en el campo de lista. El tamaño del valor de punto flotante (float o double) viene determinado por el valor de float size especificado en el encabezado de archivo. Para mejorar la eficacia, los LIST FLOAT de TOKEN \_ \_ consecutivos deben estar compuestos en una sola lista.



| Campo | Tipo               | Tamaño (bytes)   | Contenido                                  |
|-------|--------------------|----------------|-------------------------------------------|
| token | WORD               | 2              | tOKEN \_ FLOAT \_ LISt                        |
| recuento | DWORD              | 4              | Número de flotantes o dobles en el campo de lista |
| list  | Matriz float/double | Recuento de 4 u 8 x | Lista flotante o doble                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificación binaria](binary-encoding.md)
</dt> </dl>

 

 
