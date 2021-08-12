---
title: WM_COPYDATA mensaje (Winuser.h)
description: Una aplicación envía el mensaje COPYDATA de WM \_ para pasar datos a otra aplicación.
ms.assetid: d937a260-9fd2-4450-a762-20120f589ab1
keywords:
- WM_COPYDATA mensaje Data Exchange
topic_type:
- apiref
api_name:
- WM_COPYDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb91b2544bf0ebf0e8767a611b422de9aaaf1d73161e47c7bf27768f4acecb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304498"
---
# <a name="wm_copydata-message"></a>Mensaje \_ COPYDATA de WM

Una aplicación envía el **mensaje \_ COPYDATA de WM** para pasar datos a otra aplicación.


```C++
#define WM_COPYDATA                     0x004A
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana que pasa los datos.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) que contiene los datos que se pasan.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la aplicación receptora procesa este mensaje, debe devolver **TRUE**; de lo contrario, debe devolver **FALSE**.

## <a name="remarks"></a>Comentarios

Los datos que se pasan no deben contener punteros u otras referencias a objetos no accesibles para la aplicación que recibe los datos.

Mientras se envía este mensaje, otro subproceso del proceso de envío no debe cambiar los datos a los que se hace referencia.

La aplicación receptora debe tener en cuenta los datos de solo lectura. El *parámetro lParam* solo es válido durante el procesamiento del mensaje. La aplicación receptora no debe liberar la memoria a la que hace referencia *lParam.* Si la aplicación receptora debe tener acceso a los datos después de la devolución de [**SendMessage,**](/windows/desktop/api/winuser/nf-winuser-sendmessage) debe copiar los datos en un búfer local.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, vea [Using Data Copy](using-data-copy.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct)
</dt> </dl>

 

