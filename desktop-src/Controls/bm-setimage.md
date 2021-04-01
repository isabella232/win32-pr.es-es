---
title: Mensaje de BM_SETIMAGE (Winuser. h)
description: Asocia una nueva imagen (icono o mapa de bits) al botón.
ms.assetid: bf05e684-63d0-4583-960b-f329edafb151
keywords:
- BM_SETIMAGE controles de mensajes de Windows
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
ms.openlocfilehash: 65d083c4fb509d51eb017bb7d3d38fab07b4c006
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150020"
---
# <a name="bm_setimage-message"></a>Mensaje de el SETIMAGE de BM \_

Asocia una nueva imagen (icono o mapa de bits) al botón.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de imagen que se va a asociar al botón. Este parámetro puede ser uno de los siguientes valores:

-   mapa de bits de imagen \_
-   icono de imagen \_

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador (**HICON** o **hBitmap**) de la imagen que se va a asociar al botón.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un identificador de la imagen asociada previamente al botón, si existe; de lo contrario, es **null**.

## <a name="remarks"></a>Observaciones

La apariencia del texto, un icono o ambos en un control de botón depende del [**\_ icono de BS**](button-styles.md) y de los estilos de [**mapa de \_ bits BS**](button-styles.md) , y de si se llama al mensaje de el **\_ SETIMAGE de BM** . Los resultados posibles son los siguientes:



| \_¿Icono de BS \_ o conjunto de mapas de bits BS? | Se \_ llamó a la BM SETIMAGE? | Resultado              |
|-----------------------------|----------------------|---------------------|
| Sí                         | Sí                  | Mostrar solo el icono.     |
| No                          | Sí                  | Mostrar el icono y el texto. |
| Sí                         | No                   | Mostrar solo texto.     |
| No                          | No                   | Mostrar solo texto      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BM \_ de BM**](bm-getimage.md)
</dt> </dl>

 

 





