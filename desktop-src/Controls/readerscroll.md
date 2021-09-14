---
title: Función de devolución de llamada ReaderScroll
description: Función de devolución de llamada definida por la aplicación que se usa cuando el puntero del mouse se mueve dentro de la parte de la ventana del modo lector que se ha declarado como el área de desplazamiento activa.
ms.assetid: b1feb661-e3bc-4fcd-9acf-ac000c3066bd
keywords:
- ReaderScroll callback function Windows Controls
topic_type:
- apiref
api_name:
- ReaderScroll
- PFNREADERSCROLL
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0db5a80b84a30362e3bdbce45fe7485ad0dd6884
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167182"
---
# <a name="readerscroll-callback-function"></a>Función de devolución de llamada ReaderScroll

\[*ReaderScroll está* disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

Función de devolución de llamada definida por la aplicación que se usa cuando el puntero del mouse se mueve dentro de la parte de la ventana del modo lector que se ha declarado como el área de desplazamiento activa.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CALLBACK ReaderScroll(
  _In_ PREADERMODEINFO prmi,
  _In_ int             dx,
  _In_ int             dy
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*prmi* \[ En\]
</dt> <dd>

Tipo: **PREADERMODEINFO**

Puntero a la [**estructura READERMODEINFO**](readermodeinfo.md) que se pasó a la [**función DoReaderMode.**](doreadermode.md) Esta estructura define la ventana del modo de lector y el área de desplazamiento activa.

</dd> <dt>

*dx* \[ en\]
</dt> <dd>

Tipo: **int**

Distancia que se debe desplazar horizontalmente. Si la marca VERTICALONLY de RMF \_ se establece en la estructura [**READERMODEINFO,**](readermodeinfo.md) este valor siempre es 0.

</dd> <dt>

*dy* \[ En\]
</dt> <dd>

Tipo: **int**

Distancia que se debe desplazar verticalmente. Si la marca RMF \_ HORIZONTALONLY está establecida en la [**estructura READERMODEINFO,**](readermodeinfo.md) este valor siempre es 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

Esta función siempre debe devolver **TRUE.**

## <a name="remarks"></a>Observaciones

Cuando la aplicación recibe una notificación de esta función, la aplicación es responsable de desplazar la ventana del modo lector en la dirección especificada por los parámetros *dx* y *dy.*

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se describe una implementación de esta función mediante una función personalizada para realizar el desplazamiento.


```C++
BOOL CALLBACK
ReaderScrollCallback(PREADERMODEINFO prmi, int dx, int dy)
{
    if (prmi == NULL) 
        return FALSE;

    // Call custom ScrollWindow method to scroll the window
    ScrollWindow(prmi->hwnd, dx, dy);
    
    return TRUE;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, solo Windows \[ aplicaciones de escritorio de Vista\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>          |



 

