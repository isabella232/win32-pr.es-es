---
description: Implementa un asignador que admite la interfaz IMemAllocator.
ms.assetid: c40eccef-d915-4bf3-81b2-b20e000718fb
title: CMemAllocator (clase, Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bb94d5fae92d7494a4ac347591e9d571a7765d2be88072559fd74687eea87e97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915935"
---
# <a name="cmemallocator-class"></a>CMemAllocator (clase)

![Jerarquía de clases cmemallocator](images/filter10.png)

Implementa un asignador que admite la [**interfaz IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)

Esta clase se deriva de [**CBaseAllocator.**](cbaseallocator.md) Para obtener más información sobre los asignadores, consulte la documentación de [**CBaseAllocator**](cbaseallocator.md).



| Variables miembro protegidas                              | Descripción                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [**m \_ pBuffer**](cmemallocator-m-pbuffer.md)           | Puntero al bloque de memoria que contiene los búferes.                   |
| Métodos protegidos                                       | Descripción                                                              |
| [**Gratuito**](cmemallocator-free.md)                      | Método de marcador de posición; se llama durante una operación de confirmación.                  |
| [**ReallyFree**](cmemallocator-reallyfree.md)          | Libera la memoria de los búferes.                                     |
| [**Alloc**](cmemallocator-alloc.md)                    | Asigna memoria para los búferes.                                        |
| Métodos públicos                                          | Descripción                                                              |
| [**CMemAllocator**](cmemallocator-cmemallocator.md)    | Método constructor.                                                      |
| [**~ CMemAllocator**](cmemallocator--cmemallocator.md) | Método destructor.                                                       |
| [**CreateInstance**](cmemallocator-createinstance.md)  | Crea una nueva instancia de la **clase CMemAllocator.**                   |
| Métodos IMemAllocator                                   | Descripción                                                              |
| [**SetProperties**](cmemallocator-setproperties.md)    | Especifica el número de búferes que se asignarán y el tamaño de cada búfer. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Proporcionar un asignador personalizado](providing-a-custom-allocator.md)
</dt> </dl>

 

 




