---
title: Función de devolución de llamada ReaderScroll
description: Función de devolución de llamada definida por la aplicación que se usa cuando el puntero del mouse se mueve dentro de la parte de la ventana del modo lector que se ha declarado como el área de desplazamiento activa.
ms.assetid: b1feb661-e3bc-4fcd-9acf-ac000c3066bd
keywords:
- ReaderScroll (función de devolución de llamada) controles de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996329"
---
# <a name="readerscroll-callback-function"></a>Función de devolución de llamada ReaderScroll

\[*ReaderScroll* está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

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

*PRMI* \[ de\]
</dt> <dd>

Tipo: **PREADERMODEINFO**

Puntero a la estructura [**READERMODEINFO**](readermodeinfo.md) que se pasó a la función [**DoReaderMode**](doreadermode.md) . Esta estructura define la ventana de modo lector y el área de desplazamiento activa.

</dd> <dt>

*DX* \[ en\]
</dt> <dd>

Tipo: **int**

Distancia que se va a desplazar horizontalmente. Si \_ se establece la marca RMF VERTICALONLY en la estructura [**READERMODEINFO**](readermodeinfo.md) , este valor siempre es 0.

</dd> <dt>

*DY* \[ de\]
</dt> <dd>

Tipo: **int**

Distancia que se va a desplazar verticalmente. Si \_ se establece la marca RMF HORIZONTALONLY en la estructura [**READERMODEINFO**](readermodeinfo.md) , este valor siempre es 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

Esta función siempre debe devolver **true**.

## <a name="remarks"></a>Observaciones

Cuando la aplicación recibe la notificación de esta función, la aplicación es responsable de desplazar la ventana del modo lector en la dirección especificada por los parámetros *DX* y *DY* .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se describe una implementación de esta función con una función personalizada para realizar el desplazamiento.


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
| Cliente mínimo compatible<br/> | Windows Vista, \[ solo aplicaciones de escritorio de Windows Vista\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>          |



 

