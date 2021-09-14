---
description: La estructura FILTER de AMOVIESETUP \_ contiene información para registrar un filtro.
ms.assetid: 72e58f33-e480-4b32-b3d5-8f6c8eb2d5a3
title: AMOVIESETUP_FILTER estructura (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMOVIESETUP_FILTER
api_type:
- HeaderDef
api_location:
- combase.h
ms.openlocfilehash: 55a225185733a822591d8f93c2eca3674d51a340
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162310"
---
# <a name="amoviesetup_filter-structure"></a>Estructura FILTER de AMOVIESETUP \_

La **estructura FILTER \_ de AMOVIESETUP** contiene información para registrar un filtro.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _AMOVIESETUP_FILTER {
  const  CLSID           *clsID;
  const  WCHAR           *strName;
  DWORD                  dwMerit;
  UINT                   nPins;
  const  AMOVIESETUP_PIN *lpPin;
} AMOVIESETUP_FILTER, *PAMOVIESETUP_FILTER, *FAR LPAMOVIESETUP_FILTER;
```



## <a name="members"></a>Members

<dl> <dt>

**Clsid**
</dt> <dd>

Identificador de clase del filtro.

</dd> <dt>

**strName**
</dt> <dd>

Nombre del filtro.

</dd> <dt>

**dwMerit**
</dt> <dd>

Filtrar el valor. Usado por la [**interfaz IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) al construir un gráfico de filtro. Para obtener una lista de valores de meritorio, [consulte El valor de la propiedad](merit.md).

</dd> <dt>

**nPins**
</dt> <dd>

Número de elementos de la *matriz lpPin.* Si *lpPin* es **NULL,** establezca este miembro en cero.

</dd> <dt>

**lpPin**
</dt> <dd>

Puntero a una matriz de [**estructuras \_ pin de AMOVIESETUP,**](amoviesetup-pin.md) de tamaño *nPins*. Cada miembro de esta matriz describe un pin en el filtro.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para obtener información sobre el uso de esta estructura, [vea How to Register DirectShow Filters](how-to-register-directshow-filters.md). Use esta estructura solo para los filtros registrados en la categoría de filtro predeterminada (CLSID \_ LegacyAmFilterCategory). Para registrar un filtro en una categoría diferente, use el método [**IFilterMapper2::RegisterFilter,**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) como se describe en [Implementación de DllRegisterServer.](implementing-dllregisterserver.md)

> [!Note]  
> El archivo de encabezado combase.h se proporciona con las [DirectShow base](directshow-base-classes.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[DirectShow Estructuras](directshow-structures.md)
</dt> </dl>

 

 




