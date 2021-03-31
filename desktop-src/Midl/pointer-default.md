---
title: pointer_default (atributo)
description: El atributo \ Pointer \_ default \ especifica el atributo de puntero predeterminado para todos los punteros, excepto los punteros de nivel superior que aparecen en las listas de parámetros.
ms.assetid: a6e83034-8adb-483d-8d1e-432a1aed22c6
keywords:
- pointer_default el atributo MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08555358eb0abd42957d60527e18a4fd4f49165a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077606"
---
# <a name="pointer_default-attribute"></a>\_atributo default del puntero

El atributo **\[ \_ default \] Pointer** especifica el atributo de puntero predeterminado para todos los punteros, excepto los punteros de nivel superior que aparecen en las listas de parámetros.

``` syntax
pointer_default ( ptr | ref | unique )
```

## <a name="parameters"></a>Parámetros

Este atributo no tiene parámetros.

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(6B29FC40-CA47-1067-B31D-00DD010662DA), 
    version(3.3), 
    pointer_default(unique)
] 
interface dictionary 
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**interfaz**](interface.md)
</dt> <dt>

[Atributos array y Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**matrices**](arrays-1.md)
</dt> <dt>

[Matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**espeficarse**](unique.md)
</dt> <dt>

[Tipos de puntero predeterminados](/windows/desktop/Rpc/default-pointer-types)
</dt> </dl>

 

 