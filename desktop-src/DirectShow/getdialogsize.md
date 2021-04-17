---
description: La función GetDialogSize recupera el tamaño de un cuadro de diálogo de recursos.
ms.assetid: b6c42f96-0381-493a-9503-f3bd4c6a8e1e
title: Función GetDialogSize (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDialogSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 34eff1882306c85446f7cc7708efea3b17fcf7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653839"
---
# <a name="getdialogsize-function"></a>GetDialogSize función)

La función **GetDialogSize** recupera el tamaño de un cuadro de diálogo de recursos.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI GetDialogSize(
   int     iResourceID,
   DLGPROC pDlgProc,
   LPARAM  lParam,
   SIZE    *pResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iResourceID* 
</dt> <dd>

Identificador de recursos del cuadro de diálogo.

</dd> <dt>

*pDlgProc* 
</dt> <dd>

Puntero al procedimiento del cuadro de diálogo.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor pasado en el mensaje de INITDIALOG de WM \_ enviado al cuadro de diálogo temporal justo después de su creación.

</dd> <dt>

*pResult* 
</dt> <dd>

Puntero a una estructura de **tamaño** que recibe las dimensiones del cuadro de diálogo, en píxeles de pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si se encontró el recurso de cuadro de diálogo o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Las páginas de propiedades pueden usar esta función para devolver el tamaño de presentación real que requieran. La mayoría de las páginas de propiedades son cuadros de diálogo y, como tales, tienen plantillas de cuadro de diálogo almacenadas en archivos de recursos. Las plantillas utilizan unidades del cuadro de diálogo que no se asignan directamente a los píxeles de la pantalla. Sin embargo, la función [**GetPageInfo**](cbasepropertypage-getpageinfo.md) de una página de propiedades debe devolver el tamaño de presentación real en píxeles. La página de propiedades puede llamar `GetDialogSize` a para calcular el tamaño de presentación.

Esta función crea una instancia temporal del cuadro de diálogo. Para evitar que aparezca el cuadro de diálogo en la pantalla, la plantilla de cuadro de diálogo del archivo de recursos no debe tener una propiedad de WS \_ visible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares de páginas de propiedades](property-page-helper-functions.md)
</dt> </dl>

 

 




