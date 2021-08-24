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
ms.openlocfilehash: cd8adfa3d6fa3c59a05331c82ea12100918a4697d9478097a890eedff039d5e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768735"
---
# <a name="direct2d-constants"></a>Constantes de Direct2D

Las siguientes constantes se declaran en los archivos de encabezado `d2d1effectauthor.h` `d2d1.h` , , y `d2d1_1.h` `d2d1effects_2.h` .

## <a name="d2d1_append_aligned_element--1"></a>D2D1_APPEND_ALIGNED_ELEMENT (-1)
Se usa al empaquetar elementos de diseño de entrada. Indica que los elementos deben empaquetarse de forma contigua.

## <a name="d2d1_default_flattening_tolerance-025f"></a>D2D1_DEFAULT_FLATTENING_TOLERANCE (0,25f)
Tolerancia predeterminada para las operaciones de aplanado geométrico.

## <a name="d2d1_invalid_property_index-uint_max"></a>D2D1_INVALID_PROPERTY_INDEX (UINT_MAX)
Define un índice de propiedad no válido.

Esta constante se devuelve de [**ID2D1Properties::GetPropertyIndex**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) para indicar que la propiedad con nombre que proporcionó no tiene un índice en la interfaz de propiedad.

Si pasa esta constante a [**ID2D1Properties::GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) o [**ID2D1Properties::GetValueByName**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32)), se produce un error en la llamada y el búfer de salida se rellena con cero.

## <a name="d2d1_invalid_tag-ulonglong_max"></a>D2D1_INVALID_TAG (ULONGLONG_MAX)
Reservado; no use.

## <a name="d2d1_scene_referred_sdr_white_level-800f"></a>D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80.0f)
Número de nits que usa el espacio de colores sRGB o scRGB para los valores de punto flotante o blanco de SDR de 1,0f. Este valor es constante solo cuando el espacio de colores usa la luminosidad a la que se hace referencia a la escena, lo que se aplica al contenido de alto rango dinámico (HDR). Si en su lugar el espacio de colores usa la luminosidad a la que se hace referencia en pantalla, se debe consultar el nivel de blanco de SDR desde la pantalla.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Cliente mínimo compatible | Windows 7, Windows Vista con SP2 y Platform Update for Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\] |
| Servidor mínimo compatible | Windows Server 2008 R2, Windows Server 2008 con SP2 y Actualización de plataforma para aplicaciones de escritorio de Windows Server 2008 aplicaciones \[ \| para UWP\] |
| Teléfono mínimo compatible | Windows Phone 8.1 Windows Phone Silverlight 8.1 y aplicaciones en tiempo de ejecución de \[ Windows \] , Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\] |
| Header | d2d1effectauthor.h, d2d1.h, d2d1_1.h, d2d1effects_2.h |
