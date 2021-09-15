---
description: Un objeto de datos tiene la siguiente definición de sintaxis.
ms.assetid: e636c2eb-3c11-45bf-ab0b-a14ec878742c
title: Datos (formato de archivo X)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efdf799b9f7f155c8d2a0e883c8d5e79f8091156
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566029"
---
# <a name="data-x-file-format-binary-encoding"></a>Datos (formato de archivo X, codificación binaria)

Un objeto de datos tiene la siguiente definición de sintaxis.


```
object                : identifier optional_name TOKEN_OBRACE
                            optional_class_id
                            data_parts_list
                            TOKEN_CBRACE

data_parts_list       : data_part
                      | data_parts_list data_part

data_part             : data_reference
                      | object
                      | number_list
                      | float_list
                      | string_list

number_list           : TOKEN_INTEGER_LIST

float_list            : TOKEN_FLOAT_LIST

string_list           : string_list_1 list_separator

string_list_1         : string
                      | string_list_1 list_separator string

list_separator        : comma
                      | semicolon

string                : token_string

identifier            : name
                      | primitive_type

data_reference        : TOKEN_OBRACE name optional_class_id TOKEN_CBRACE
```



Tenga en cuenta que en los datos de lista de números y de lista flotante en archivos binarios, no se usan TOKEN COMMA ni \_ \_ TOKEN \_ \_ SEMICOLON. La coma y el punto y coma se usan en los datos de \_ la lista de cadenas. Tenga en cuenta también que solo puede usar la referencia de \_ datos para miembros de datos opcionales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificación binaria](binary-encoding.md)
</dt> </dl>

 

 



