---
title: force_allocate atributo)
description: El atributo ACF \ Force \_ allocate \ obliga a que se asigne un parámetro de puntero mediante \_ \_ la asignación de usuarios de MIDL en lugar de optimizar la asignación.
ms.assetid: 40e3a7d9-7e4f-4e3d-8c82-fb6ef567f293
keywords:
- force_allocate el atributo MIDL
topic_type:
- apiref
api_name:
- force_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f73d0386d786e4d3004c78b1acccda7e9be8fc16
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487583"
---
# <a name="force_allocate-attribute"></a>forzar \_ asignación de atributo

El atributo ACF de \[ **\_ asignación forzada** \] obliga a que se asigne un parámetro de puntero mediante la asignación de [**\_ usuarios \_ de MIDL**](midl-user-allocate-1.md) en lugar de optimizar la asignación.

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ force_allocate [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="parameters"></a>Parámetros

Este atributo no tiene parámetros.

## <a name="remarks"></a>Observaciones

RPC intenta minimizar las asignaciones de memoria en el servidor mediante el suministro de punteros a los búferes de memoria internos. Este enfoque puede provocar problemas en las aplicaciones que intentan llamar directamente al [**usuario de MIDL \_ \_**](midl-user-free-1.md) en punteros proporcionados por RPC, ya que no se puede liberar un puntero que se ha optimizado. Marcar un parámetro con **\[ Force \_ allocate \]** impedirá esta optimización para todos los punteros que lo deriven.

Otro uso común de **\[ forzar \_ asignación \]** es garantizar la alineación de la memoria a la que se señala si una aplicación requiere una alineación mayor que la de la memoria a la que se apunta. Por ejemplo, las aplicaciones a menudo pasan datos en una matriz genérica de bytes en lugar de usar el tipo real, pero solo se garantiza que un byte está alineado en 1, lo que puede causar problemas en las aplicaciones que suponen una alineación mayor. Al marcar el parámetro con **\[ Force \_ allocate \]**, la aplicación puede garantizar que toda la memoria a la que se señala tendrá una alineación igual a la garantizada por la [**asignación de \_ usuarios \_ de MIDL**](midl-user-allocate-1.md).

## <a name="examples"></a>Ejemplos

``` syntax
/* IDL file */
void Func1([in, out, string] char **ppstr);
void Func2([in] long s, [in, size_is(s)] byte *pData);

/* ACF file */

/* e.g. The application wishes to call midl_user_free on *ppstr and supply a new pointer */
Func1([force_allocate] pstr);

/* e.g. pData really points to a structure that needs an alignment greater than 1 */
Func2([force_allocate] pData);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Evitar la ocultación de información](/windows/desktop/WinProg64/avoiding-information-hiding)
</dt> <dt>

[Diseño de interfaces compatibles con 64 bits](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces)
</dt> <dt>

[**\_asignación de usuarios de MIDL \_**](midl-user-allocate-1.md)
</dt> <dt>

[**usuario de MIDL \_ \_ gratis**](midl-user-free-1.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> </dl>

 

 