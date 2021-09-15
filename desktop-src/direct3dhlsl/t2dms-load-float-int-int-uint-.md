---
title: Función Texture2DMS::Load(int,int,int,uint)
description: Lee los datos de textura y devuelve el estado de la operación. | Función Texture2DMS::Load(int,int,int,uint)
ms.assetid: 4230962C-2968-4030-9770-8318F1760AEB
keywords:
- Carga de la función HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e967d69929c0b20317ffb74fc97c4e60e36c2854
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575205"
---
# <a name="texture2dmsloadintintintuint-function"></a>Función Texture2DMS::Load(int,int,int,uint)

Lee los datos de textura y devuelve el estado de la operación.

## <a name="syntax"></a>Sintaxis


``` syntax
 Load(
  in  int2 Location,
  in  int  sampleindex,
  in  int2 Offset,
  out uint Status
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ubicación* \[ En\]
</dt> <dd>

Tipo: **int2**

Las coordenadas de textura.

</dd> <dt>

*sampleindex* \[ En\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Índice de ejemplo.

</dd> <dt>

*Desplazamiento* \[ En\]
</dt> <dd>

Tipo: **int2**

Desplazamiento aplicado a las coordenadas de textura antes de la carga.

</dd> <dt>

*Estado* \[ out\]
</dt> <dd>

Tipo: **uint**

Estado de la operación. No se puede acceder al estado directamente; en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** devuelve **TRUE** si todos los valores de la operación **Sample**, **Gather** o **Load** correspondientes accedieron a iconos asignados en un recurso [en mosaico.](/windows/desktop/direct3d11/direct3d-11-2-features) Si se tomaron valores de un icono no asociado, **CheckAccessFullyMapped** devuelve **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Escriba:

El tipo de valor devuelto coincide con el tipo de la declaración del [**objeto Texture2DMS.**](sm5-object-texture2dms.md)

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Métodos de carga](texture2dms-load.md)
</dt> <dt>

[**Texture2DMS**](sm5-object-texture2dms.md)
</dt> </dl>

 

 
