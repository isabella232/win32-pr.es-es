---
title: force_allocate atributo
description: El atributo ACF \force allocate\ fuerza la asignación de un parámetro de puntero mediante asignación de usuario de nivel medio en lugar de optimizar \_ \_ la \_ asignación.
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
ms.openlocfilehash: f73d0386d786e4d3004c78b1acccda7e9be8fc16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159581"
---
# <a name="force_allocate-attribute"></a>atributo \_ force allocate

La asignación de fuerza del atributo ACF fuerza la asignación de un parámetro de puntero mediante la asignación de usuario de nivel medio en lugar de \[ **\_** optimizar \] la [**\_ \_**](midl-user-allocate-1.md) asignación.

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ force_allocate [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="parameters"></a>Parámetros

Este atributo no tiene parámetros.

## <a name="remarks"></a>Observaciones

RPC intenta minimizar las asignaciones de memoria en el servidor mediante el suministro de punteros a búferes de memoria internos. Este enfoque puede causar problemas para las aplicaciones que intentan llamar directamente al usuario [**midl \_ \_**](midl-user-free-1.md) libre en punteros proporcionados por RPC, ya que no se puede liberar un puntero que se ha optimizado. Marcar un parámetro con **\[ force allocate \_ impedirá \]** esta optimización para todos los punteros que lo derivan.

Otro uso común de **\[ force \_ allocate \]** es garantizar la alineación de la memoria a la que se apunta si una aplicación requiere una alineación mayor que la de la memoria a la que se apunta. Por ejemplo, las aplicaciones a menudo pasan datos en una matriz genérica de bytes en lugar de usar el tipo real, pero solo se garantiza que un byte esté alineado en 1, lo que puede causar problemas para las aplicaciones que asumen una alineación mayor. Al marcar el parámetro con **\[ force \_ allocate \]**, la aplicación puede garantizar que toda la memoria a la que se apunta tendrá una alineación igual a la garantizada por el [**usuario midl \_ \_ asigna**](midl-user-allocate-1.md).

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

[**asignación de usuario midl \_ \_**](midl-user-allocate-1.md)
</dt> <dt>

[**midl \_ user \_ free**](midl-user-free-1.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> </dl>

 

 