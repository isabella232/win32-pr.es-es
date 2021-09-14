---
title: TTM_SETDELAYTIME mensaje (Commctrl.h)
description: Establece las duraciones iniciales, emergentes y de volver a mostrar para un control de información sobre herramientas.
ms.assetid: 0a73def0-550c-4d01-9cb1-1eb1f4356fa3
keywords:
- TTM_SETDELAYTIME controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165866"
---
# <a name="ttm_setdelaytime-message"></a>Mensaje \_ SETDELAYTIME de TTM

Establece las duraciones iniciales, emergentes y de volver a mostrar para un control de información sobre herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Marca que especifica el valor de hora que se va a establecer. Este parámetro puede ser uno de los siguientes valores



| Value                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <dt>**AUTOPOP de TTDT \_**</dt> </dl>       | Establezca la cantidad de tiempo que una ventana de información sobre herramientas permanece visible si el puntero está estacionado dentro del rectángulo delimitador de una herramienta. Para devolver el tiempo de retraso de autopop a su valor predeterminado, *establezca lParam* en -1.<br/>                                                                                                                                                         |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <dt>**TTDT \_ INITIAL**</dt> </dl>       | Establezca la cantidad de tiempo que un puntero debe permanecer estacionado dentro del rectángulo delimitador de una herramienta antes de que aparezca la ventana de información sobre herramientas. Para devolver el tiempo de retraso inicial a su valor predeterminado, *establezca lParam* en -1.<br/>                                                                                                                                                    |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <dt>**TTDT \_ RESHOW**</dt> </dl>          | Establezca la cantidad de tiempo que tardan en aparecer las ventanas de información sobre herramientas posteriores a medida que el puntero se mueve de una herramienta a otra. Para devolver el tiempo de retraso de volver a mostrar a su valor predeterminado, *establezca lParam* en -1.<br/>                                                                                                                                                           |
| <span id="TTDT_AUTOMATIC"></span><span id="ttdt_automatic"></span><dl> <dt>**TTDT \_ AUTOMATIC**</dt> </dl> | Establezca las tres veces de retraso en proporciones predeterminadas. El tiempo de autopop será diez veces la hora inicial y la hora de volver a mostrar será una quinta parte de la hora inicial. Si se establece esta marca, use un valor positivo de *lParam* para especificar la hora inicial, en milisegundos. Establezca *lParam en* un valor negativo para devolver las tres veces de retraso a sus valores predeterminados.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

LOWORD [**especifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el tiempo de retraso, en milisegundos. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="remarks"></a>Observaciones

Los tiempos de retraso predeterminados se basan en el tiempo de doble clic. Para el tiempo predeterminado de doble clic de 500 ms, los tiempos de retraso inicial, autopop y reshow son 500 ms, 5000 ms y 100 ms, respectivamente. El fragmento de código siguiente usa la [**función GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) para determinar los tres tiempos de retraso de cualquier sistema.


```
initial = GetDoubleClickTime();

autopop = GetDoubleClickTime() * 10;

reshow = GetDoubleClickTime() / 5;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GETDELAYTIME DE TTM \_**](ttm-getdelaytime.md)
</dt> </dl>

 

