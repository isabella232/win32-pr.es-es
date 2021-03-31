---
title: Mensaje de TTM_SETDELAYTIME (commctrl. h)
description: Establece las duraciones inicial, emergente y de presentación de un control ToolTip.
ms.assetid: 0a73def0-550c-4d01-9cb1-1eb1f4356fa3
keywords:
- TTM_SETDELAYTIME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_SETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b633dc75baa0a8f385cf8cdb9bf7e9fa254809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996407"
---
# <a name="ttm_setdelaytime-message"></a>TTM \_ SETDELAYTIME

Establece las duraciones inicial, emergente y de presentación de un control ToolTip.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Marca que especifica el valor de tiempo que se va a establecer. Este parámetro puede ser uno de los siguientes valores:



| Value                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <dt>**TTDT \_ AUTOPOP**</dt> </dl>       | Establece la cantidad de tiempo que una ventana de información sobre herramientas permanece visible si el puntero es estacionario dentro del rectángulo delimitador de una herramienta. Para devolver el tiempo de retraso de autopop a su valor predeterminado, establezca *lParam* en-1.<br/>                                                                                                                                                         |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <dt>**TTDT \_ inicial**</dt> </dl>       | Establece la cantidad de tiempo que un puntero debe permanecer estacionario dentro del rectángulo delimitador de una herramienta antes de que aparezca la ventana de información sobre herramientas. Para devolver el tiempo de retraso inicial a su valor predeterminado, establezca *lParam* en-1.<br/>                                                                                                                                                    |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <dt>**TTDT \_ Mostrar**</dt> </dl>          | Establezca la cantidad de tiempo que tardará en aparecer la siguiente ventana de información sobre herramientas cuando el puntero se mueva de una herramienta a otra. Para devolver el tiempo de retraso de la representación a su valor predeterminado, establezca *lParam* en-1.<br/>                                                                                                                                                           |
| <span id="TTDT_AUTOMATIC"></span><span id="ttdt_automatic"></span><dl> <dt>**TTDT \_ automática**</dt> </dl> | Establezca los tres tiempos de retraso en las proporciones predeterminadas. El tiempo de autopop será diez veces la hora inicial y el tiempo de la presentación será una quinta parte de la hora inicial. Si se establece esta marca, use un valor positivo de *lParam* para especificar el tiempo inicial, en milisegundos. Establezca *lParam* en un valor negativo para devolver los tres tiempos de retardo a sus valores predeterminados.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el tiempo de retardo, en milisegundos. El valor de [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto para este mensaje.

## <a name="remarks"></a>Observaciones

Los tiempos de retraso predeterminados se basan en el tiempo de doble clic. Para el tiempo de doble clic predeterminado de 500 ms, los tiempos de retardo inicial, autopop y de representación son 500 ms, 5.000 MS y 100M, respectivamente. En el fragmento de código siguiente se usa la función [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) para determinar los tres tiempos de retraso de cualquier sistema.


```
initial = GetDoubleClickTime();

autopop = GetDoubleClickTime() * 10;

reshow = GetDoubleClickTime() / 5;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TTM \_ GETDELAYTIME**](ttm-getdelaytime.md)
</dt> </dl>

 

