---
title: ImageList_SetColorTable función
description: Establece la tabla de colores de una lista de imágenes.
ms.assetid: 1b62f468-cbc4-479b-b9f8-5553c2bd8c79
keywords:
- ImageList_SetColorTable función Windows controles
topic_type:
- apiref
api_name:
- ImageList_SetColorTable
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de1acd8f14d9993bc75ea69b910b365e29156a6386933ccb95251a916c37244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412243"
---
# <a name="imagelist_setcolortable-function"></a>Función ImageList \_ SetColorTable

Establece la tabla de colores de una lista de imágenes.

## <a name="syntax"></a>Sintaxis


```C++
int ImageList_SetColorTable(
  _In_ HIMAGELIST himl,
  _In_ int        start,
  _In_ int        len,
  _In_ RGBQUAD    *prgb
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*himl* \[ En\]
</dt> <dd>

Tipo: **HIMAGELIST**

Identificador de la lista de imágenes.

</dd> <dt>

*start* \[ En\]
</dt> <dd>

Tipo: **int**

Índice de tabla de colores de base cero que especifica la primera entrada de tabla de colores que se debe establecer.

</dd> <dt>

*len* \[ En\]
</dt> <dd>

Tipo: **int**

Número de entradas de tabla de colores que se establecerán.

</dd> <dt>

*prgb* \[ En\]
</dt> <dd>

Tipo: **[ **RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)\***

Puntero a una matriz de estructuras [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) *len* que contienen información de color nueva para la tabla de colores de la DIB.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Si la función se realiza correctamente, devuelve el número de entradas de tabla de colores establecidas por la función. Si se produce un error en la función, el valor devuelto es menor o igual que cero.

## <a name="remarks"></a>Comentarios

Solo las listas de imágenes creadas con las marcas [**ILC \_ COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) [**o ILC \_ COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) tienen tablas de colores. La tabla de colores de esta lista de imágenes normalmente se establece automáticamente copiando la tabla de colores de la primera imagen agregada a la lista (por ejemplo, a través de la función [**ImageList \_ Add)**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) si esa imagen es una DIB. Si la primera imagen agregada a la lista de imágenes no es una DIB, la tabla de colores de la paleta de semitonos se usa para las listas de imágenes **ILC \_ COLOR8** y la tabla de colores VGA para **ILC \_ COLOR4.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                            |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 3.51 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Tabla de colores](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)
</dt> </dl>

 

