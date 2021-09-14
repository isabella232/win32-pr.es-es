---
title: pointer_default (atributo)
description: El atributo \ pointer default\ especifica el atributo de puntero predeterminado para todos los punteros, excepto los punteros de nivel superior que \_ aparecen en las listas de parámetros.
ms.assetid: a6e83034-8adb-483d-8d1e-432a1aed22c6
keywords:
- pointer_default atributo MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08555358eb0abd42957d60527e18a4fd4f49165a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159421"
---
# <a name="pointer_default-attribute"></a>atributo \_ predeterminado de puntero

El **\[ atributo predeterminado \_ de \]** puntero especifica el atributo de puntero predeterminado para todos los punteros, excepto los punteros de nivel superior que aparecen en las listas de parámetros.

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

[**Interfaz**](interface.md)
</dt> <dt>

[Atributos de matriz Sized-Pointer matriz](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**Matrices**](arrays-1.md)
</dt> <dt>

[Matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Único**](unique.md)
</dt> <dt>

[Tipos de puntero predeterminados](/windows/desktop/Rpc/default-pointer-types)
</dt> </dl>

 

 