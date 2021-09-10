---
title: ICM_DRAW_SUGGESTFORMAT mensaje (Vfw.h)
description: El ICM DRAW SUGGESTFORMAT consulta un controlador de representación para sugerir un formato \_ \_ descomprimido que puede dibujar.
ms.assetid: e3e97790-dbd1-4436-9830-5218ae1f949b
keywords:
- ICM_DRAW_SUGGESTFORMAT mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_SUGGESTFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97c8782b16336427b3832f36b5a06987399df1b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370574"
---
# <a name="icm_draw_suggestformat-message"></a>\_ICM Draw \_ SUGGESTFORMAT message

El **ICM \_ DRAW \_ SUGGESTFORMAT** consulta un controlador de representación para sugerir un formato descomprimido que puede dibujar.


```C++
ICM_DRAW_SUGGESTFORMAT 
wParam = (DWORD_PTR) (LPVOID) &icdrwSuggest; 
lParam = sizeof(ICDRAWSUGGEST); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwSuggest*
</dt> <dd>

Puntero a una [**estructura ICDRAWSUGGEST.**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest)

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Tamaño, en bytes, de [**ICDRAWSUGGEST.**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza correctamente. Si el **miembro lpbiSuggest** de la estructura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) es **NULL,** este mensaje devuelve la cantidad de memoria necesaria para contener el formato sugerido.

## <a name="remarks"></a>Observaciones

El controlador debe examinar el formato especificado en el miembro **lpbiIn** de la estructura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) y usar el miembro **lpbiSuggest** para devolver un formato que pueda dibujar. El formato de salida debe conservar tantos datos como sea posible del formato de entrada.

Opcionalmente, el controlador puede usar el controlador del manipulador instalable pasado en el **miembro hicDecompressor** de [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) para realizar selecciones más complejas. Por ejemplo, si el formato de entrada son datos JPEG de 24 bits, un representador podría consultar el descomprimidor para averiguar si puede descomprimir a un formato YUV (que podría dibujarse de forma más eficaz) antes de seleccionar el formato que se va a sugerir.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





