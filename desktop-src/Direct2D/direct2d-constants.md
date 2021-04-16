---
title: Constantes de Direct2D
description: Direct2D define la siguiente lista de constantes.
ms.assetid: 98a443af-4bb7-486d-bc87-ff34c3671bdd
topic_type:
- apiref
api_name:
- D2D1_APPEND_ALIGNED_ELEMENT
- D2D1_DEFAULT_FLATTENING_TOLERANCE
- D2D1_INVALID_PROPERTY_INDEX
- D2D1_INVALID_TAG
- D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL
api_location:
- d2d1.h
- d2d1effects_2.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 09/19/2019
ms.openlocfilehash: bc25bf1055b923a383fc580a622e96d787ed13e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658269"
---
# <a name="direct2d-constants"></a>Constantes de Direct2D

Las constantes siguientes se declaran en `d2d1effectauthor.h` los `d2d1.h` archivos de encabezado,, `d2d1_1.h` y `d2d1effects_2.h` .

## <a name="d2d1_append_aligned_element--1"></a>D2D1_APPEND_ALIGNED_ELEMENT (-1)
Se usa al empaquetar elementos de diseño de entrada. Indica que los elementos deben empaquetarse de forma contigua.

## <a name="d2d1_default_flattening_tolerance-025f"></a>D2D1_DEFAULT_FLATTENING_TOLERANCE (0,25 f)
La tolerancia predeterminada para las operaciones de simplificación geométrica.

## <a name="d2d1_invalid_property_index-uint_max"></a>D2D1_INVALID_PROPERTY_INDEX (UINT_MAX)
Define un índice de propiedad no válido.

Esta constante se devuelve desde [**ID2D1Properties:: GetPropertyIndex**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) para indicar que la propiedad con nombre que proporcionó no tiene un índice en la interfaz de propiedad.

Si pasa esta constante a [**ID2D1Properties:: GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) o [**ID2D1Properties:: GetValueByName**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32)), se produce un error en la llamada y el búfer de salida se rellena con ceros.

## <a name="d2d1_invalid_tag-ulonglong_max"></a>D2D1_INVALID_TAG (ULONGLONG_MAX)
Sector No use.

## <a name="d2d1_scene_referred_sdr_white_level-800f"></a>D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80,0 f)
Número de Nits que utiliza el espacio de colores sRGB o scRGB para el blanco de SDR o valores de punto flotante de 1,0 f. Este valor es constante solo cuando el espacio de colores utiliza la luminancia a la que se refiere la escena, lo que es cierto para el contenido de intervalo dinámico alto (HDR). Si en su lugar el espacio de colores utiliza la luminancia a la que se hace referencia, el nivel blanco de SDR debe consultarse desde la pantalla.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Cliente mínimo compatible | Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\] |
| Servidor mínimo compatible | Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\] |
| Teléfono mínimo compatible | Windows Phone 8,1 \[ Windows Phone Windows Runtime aplicaciones de silverlight 8,1 y \] , Windows Phone 8,1 \[ Windows Phone aplicaciones de silverlight 8,1 y Windows Runtime\] |
| Encabezado | d2d1effectauthor. h, d2d1. h, d2d1_1. h, d2d1effects_2. h |
