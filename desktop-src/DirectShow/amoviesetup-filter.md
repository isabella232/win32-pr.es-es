---
description: La \_ estructura de filtro AMOVIESETUP contiene información para registrar un filtro.
ms.assetid: 72e58f33-e480-4b32-b3d5-8f6c8eb2d5a3
title: Estructura de AMOVIESETUP_FILTER (ComBase. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661116"
---
# <a name="amoviesetup_filter-structure"></a>AMOVIESETUP \_ estructura de filtro

La estructura de **\_ filtro AMOVIESETUP** contiene información para registrar un filtro.

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



## <a name="members"></a>Miembros

<dl> <dt>

**clsID**
</dt> <dd>

Identificador de clase del filtro.

</dd> <dt>

**strName**
</dt> <dd>

Nombre del filtro.

</dd> <dt>

**dwMerit**
</dt> <dd>

Mérito del filtro. Lo usa la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) al construir un gráfico de filtro. Para obtener una lista de los valores de méritos, vea [mérito](merit.md).

</dd> <dt>

**nPins**
</dt> <dd>

Número de elementos de la matriz *lpPin* . Si *lpPin* es **null**, establezca este miembro en cero.

</dd> <dt>

**lpPin**
</dt> <dd>

Puntero a una matriz de estructuras [**AMOVIESETUP \_ PIN**](amoviesetup-pin.md) , de tamaño *nPins*. Cada miembro de esta matriz describe un PIN en el filtro.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para obtener información acerca del uso de esta estructura, consulte [How to Register DirectShow filters](how-to-register-directshow-filters.md). Use esta estructura solo para los filtros que se registran en la categoría de filtro predeterminada (CLSID \_ LegacyAmFilterCategory). Para registrar un filtro en una categoría diferente, use el método [**IFilterMapper2:: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) , como se describe en [implementación de DllRegisterServer](implementing-dllregisterserver.md).

> [!Note]  
> El archivo de encabezado ComBase. h se proporciona con las [clases base de DirectShow](directshow-base-classes.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>ComBase. h (incluir streams. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de DirectShow](directshow-structures.md)
</dt> </dl>

 

 




