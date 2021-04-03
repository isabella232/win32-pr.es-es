---
title: ImageList_SetColorTable función)
description: Establece la tabla de colores de una lista de imágenes.
ms.assetid: 1b62f468-cbc4-479b-b9f8-5553c2bd8c79
keywords:
- ImageList_SetColorTable controles de función de Windows
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
ms.openlocfilehash: 14be5f17d83128933a35730a79726b462436e0c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997192"
---
# <a name="imagelist_setcolortable-function"></a>ImageList \_ SetColorTable función)

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

*himl* \[ de\]
</dt> <dd>

Tipo: **HIMAGELIST**

Identificador de la lista de imágenes.

</dd> <dt>

*iniciar* \[ de\]
</dt> <dd>

Tipo: **int**

Índice de tabla de colores basado en cero que especifica la primera entrada de la tabla de colores que se va a establecer.

</dd> <dt>

*longitud* \[ de\]
</dt> <dd>

Tipo: **int**

Número de entradas de la tabla de colores que se van a establecer.

</dd> <dt>

*prgb* \[ de\]
</dt> <dd>

Tipo: **[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) \** _

Puntero a una matriz de _len estructuras * [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) que contienen información de color nueva para la tabla de colores del Dib.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Si la función se ejecuta correctamente, devuelve el número de entradas de la tabla de colores establecida por la función. Si se produce un error en la función, el valor devuelto es menor o igual que cero.

## <a name="remarks"></a>Observaciones

Solo las listas de imágenes creadas con la marca [**ILC \_ COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) o [**ILC \_ COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) tienen tablas de color. Normalmente, la tabla de colores de una lista de imágenes se establece automáticamente copiando la tabla de colores de la primera imagen agregada a la lista (por ejemplo, a través de la función [**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) ) si la imagen es un Dib. Si la primera imagen agregada a la lista de imágenes no es un DIB, la tabla de colores de la paleta de semitonos se usa para las listas de imágenes de **ILC \_ COLOR8** y la tabla de colores VGA se usa para **ILC \_ COLOR4**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                                  |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                            |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 3,51 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tabla de colores](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)
</dt> </dl>

 

