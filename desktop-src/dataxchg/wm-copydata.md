---
title: Mensaje de WM_COPYDATA (Winuser. h)
description: Una aplicación envía el mensaje de COPYDATA de WM \_ para pasar datos a otra aplicación.
ms.assetid: d937a260-9fd2-4450-a762-20120f589ab1
keywords:
- Intercambio de datos de mensajes de WM_COPYDATA
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
ms.openlocfilehash: 8160c88b11fa109e8bbfaa06f0f6c45c9b7daed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491069"
---
# <a name="wm_copydata-message"></a>Mensaje de COPYDATA de WM \_

Una aplicación envía el mensaje de **\_ COPYDATA de WM** para pasar datos a otra aplicación.


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

Puntero a una estructura [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) que contiene los datos que se van a pasar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la aplicación receptora procesa este mensaje, debe devolver **true**; de lo contrario, debería devolver **false**.

## <a name="remarks"></a>Observaciones

Los datos que se pasan no deben contener punteros u otras referencias a objetos a los que no se puede tener acceso a través de la aplicación que recibe los datos.

Mientras se envía este mensaje, otro subproceso del proceso de envío no debe cambiar los datos a los que se hace referencia.

La aplicación receptora debe tener en cuenta los datos de solo lectura. El parámetro *lParam* solo es válido durante el procesamiento del mensaje. La aplicación receptora no debe liberar la memoria a la que hace referencia *lParam*. Si la aplicación receptora debe tener acceso a los datos después de que se devuelva [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , debe copiar los datos en un búfer local.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, vea uso de la [copia de datos](using-data-copy.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct)
</dt> </dl>

 

