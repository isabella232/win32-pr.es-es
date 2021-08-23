---
title: force_allocate atributo
description: El atributo ACF \ force allocate\ fuerza la asignación de un parámetro de puntero mediante midl user allocate en lugar de optimizar \_ \_ la \_ asignación.
ms.assetid: 40e3a7d9-7e4f-4e3d-8c82-fb6ef567f293
keywords:
- force_allocate atributo MIDL
topic_type:
- apiref
api_name:
- force_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c82e1665e4c49461c3c7bd1c315b31f4f72c7e3f0e5331d9f0326347d36105
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582165"
---
# <a name="force_allocate-attribute"></a>atributo force \_ allocate

La asignación de fuerza de atributo de ACF fuerza la asignación de un parámetro de puntero mediante la asignación de usuario midl en lugar de optimizar \[ **\_** \] la asignación. [**\_ \_**](midl-user-allocate-1.md)

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ force_allocate [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="parameters"></a>Parámetros

Este atributo no tiene parámetros.

## <a name="remarks"></a>Comentarios

RPC intenta minimizar las asignaciones de memoria en el servidor mediante el suministro de punteros a búferes de memoria internos. Este enfoque puede causar problemas para las aplicaciones que intentan llamar directamente al usuario [**midl \_ \_**](midl-user-free-1.md) libre en punteros proporcionados por RPC, ya que no se puede liberar un puntero que se ha optimizado. Marcar un parámetro con **\[ force allocate \_ impedirá \]** esta optimización para todos los punteros que lo derivan.

Otro uso común de **\[ force \_ allocate \]** es garantizar la alineación de la memoria a la que se apunta si una aplicación requiere una alineación mayor que la de la memoria a la que se apunta. Por ejemplo, las aplicaciones a menudo pasan datos en una matriz genérica de bytes en lugar de usar el tipo real, pero solo se garantiza que un byte esté alineado en 1, lo que puede causar problemas para las aplicaciones que asumen una alineación mayor. Al marcar el parámetro con **\[ force \_ allocate \]**, la aplicación puede garantizar que toda la memoria a la que apunta tendrá una alineación igual a la garantizada por [**midl user \_ \_ allocate**](midl-user-allocate-1.md).

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

[**midl \_ user \_ allocate**](midl-user-allocate-1.md)
</dt> <dt>

[**midl \_ user \_ free**](midl-user-free-1.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> </dl>

 

 