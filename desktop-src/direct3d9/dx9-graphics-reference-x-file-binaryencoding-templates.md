---
description: Una plantilla tiene la siguiente definición de sintaxis.
ms.assetid: 77eb739d-8da3-4481-8dd1-f9f2f0eda136
title: Plantillas (formato de archivo X)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef9ccca6627e82eaa4fdcc6467fc093000682a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714727"
---
# <a name="templates-x-file-format-binary-encoding"></a><span data-ttu-id="66327-103">Plantillas (formato de archivo X, codificación binaria)</span><span class="sxs-lookup"><span data-stu-id="66327-103">Templates (X file format, binary encoding)</span></span>

<span data-ttu-id="66327-104">Una plantilla tiene la siguiente definición de sintaxis.</span><span class="sxs-lookup"><span data-stu-id="66327-104">A template has the following syntax definition.</span></span>


```
template              : TOKEN_TEMPLATE name TOKEN_OBRACE
                            class_id
                            template_parts
                            TOKEN_CBRACE

template_parts        : template_members_part TOKEN_OBRACKET
                        template_option_info
                        TOKEN_CBRACKET
                      | template_members_list

template_members_part : /* Empty */
                      | template_members_list

template_option_info  : ellipsis
                      | template_option_list

template_members_list :    template_members
                      | template_members_list template_members

template_members      : primitive
                      | array
                      | template_reference

primitive             : primitive_type optional_name TOKEN_SEMICOLON

array                 : TOKEN_ARRAY array_data_type name dimension_list
                        TOKEN_SEMICOLON

template_reference    : name optional_name YT_SEMICOLON

primitive_type        : TOKEN_WORD
                      | TOKEN_DWORD
                      | TOKEN_FLOAT
                      | TOKEN_DOUBLE
                      | TOKEN_CHAR
                      | TOKEN_UCHAR
                      | TOKEN_SWORD
                      | TOKEN_SDWORD
                      | TOKEN_LPSTR
                      | TOKEN_UNICODE
                      | TOKEN_CSTRING

array_data_type       : primitive_type
                      | name

dimension_list        : dimension
                      | dimension_list dimension

dimension             : TOKEN_OBRACKET dimension_size TOKEN_CBRACKET

dimension_size        : TOKEN_INTEGER
                      | name

template_option_list  : template_option_part
                      | template_option_list template_option_part

template_option_part  : name optional_class_id

name                  : TOKEN_NAME

optional_name         : /* Empty */
                      | name

class_id              : TOKEN_GUID

optional_class_id     : /* Empty */
                      | class_id

ellipsis              : TOKEN_DOT TOKEN_DOT TOKEN_DOT
```



## <a name="related-topics"></a><span data-ttu-id="66327-105">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66327-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66327-106">Codificación binaria</span><span class="sxs-lookup"><span data-stu-id="66327-106">Binary Encoding</span></span>](binary-encoding.md)
</dt> </dl>

 

 



