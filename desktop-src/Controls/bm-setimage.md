---
title: BM_SETIMAGE mensaje (Winuser.h)
description: Asocia una nueva imagen (icono o mapa de bits) al botón.
ms.assetid: bf05e684-63d0-4583-960b-f329edafb151
keywords:
- BM_SETIMAGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- BM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8948c73c04d3b01230a47ab91529764c9e20281e4f45803f71d82f59dedb14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674818"
---
# <a name="bm_setimage-message"></a>Mensaje \_ DE BM SETIMAGE

Asocia una nueva imagen (icono o mapa de bits) al botón.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de imagen que se asociará al botón. Este parámetro puede ser uno de los siguientes valores:

-   MAPA DE BITS \_ DE IMAGEN
-   ICONO DE \_ IMAGEN

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador **(HICON** o **HBITMAP)** a la imagen que se asociará con el botón.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un identificador de la imagen previamente asociada al botón, si existe; de lo contrario, es **NULL.**

## <a name="remarks"></a>Observaciones

La apariencia del texto, un icono o ambos en un control de botón depende de los estilos [**BS \_ ICON**](button-styles.md) y [**BS \_ BITMAP,**](button-styles.md) y de si se llama al mensaje **BM \_ SETIMAGE.** Los resultados posibles son los siguientes:



| ¿Icono de BS \_ o conjunto de mapas de bits de BS? \_ | ¿Se \_ llama a BM SETIMAGE? | Resultado              |
|-----------------------------|----------------------|---------------------|
| Sí                         | Sí                  | Mostrar solo icono.     |
| No                          | Sí                  | Mostrar icono y texto. |
| Sí                         | No                   | Mostrar solo texto.     |
| No                          | No                   | Mostrar solo texto      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BM \_ GETIMAGE**](bm-getimage.md)
</dt> </dl>

 

 





