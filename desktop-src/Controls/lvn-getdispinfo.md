---
title: LVN_GETDISPINFO de notificación (Commctrl.h)
description: Enviado por un control list-view a su ventana primaria. Es una solicitud para que la ventana primaria proporcione la información necesaria para mostrar u ordenar un elemento de vista de lista. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 04310e39-69bc-45d7-958c-00452279d7a9
keywords:
- LVN_GETDISPINFO código de notificación Windows controles
topic_type:
- apiref
api_name:
- LVN_GETDISPINFO
- LVN_GETDISPINFOA
- LVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4f4fc6917b0de699d1ca561f46bc7789aa15eea7c40aa3681fe74991e3a122
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088825"
---
# <a name="lvn_getdispinfo-notification-code"></a>Código de notificación GETDISPINFO de LVN \_

Enviado por un control list-view a su ventana primaria. Es una solicitud para que la ventana primaria proporcione la información necesaria para mostrar u ordenar un elemento de vista de lista. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_GETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMLVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) En la entrada, la [**estructura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) contenida en esta estructura especifica el tipo de información necesaria e identifica el elemento o subelemento de interés. Use la **estructura LVITEM** para devolver la información solicitada al control . Si el controlador de mensajes establece la marca LVIF DI SETITEM en el miembro mask de la estructura \_ \_ **LVITEM,**  el control de vista de lista almacena la información solicitada y no la volverá a pedir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El receptor de notificaciones convierte *lParam* para recuperar la [**estructura NMLVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) El *parámetro wParam* contiene el código de notificación.

Un control de vista de lista envía el código **de notificación LVN \_ GETDISPINFO** para recuperar la información de elemento almacenada por la aplicación en lugar del control . La información puede ser información de texto o icono de un elemento. También puede ser información de estado de elemento. Vea el [**mensaje LVM \_ SETCALLBACKMASK**](lvm-setcallbackmask.md) para obtener más información sobre cómo implementar el estado del elemento en función de la devolución de llamada.

Para obtener más información sobre las devoluciones de llamada de vista de lista, vea Elementos de devolución de [llamada y máscara de devolución de llamada](list-view-controls-overview.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo se puede controlar este código de notificación para establecer el texto en las columnas de una vista de lista. Los datos de cada elemento se mantienen en la estructura siguiente.


```C++
 typedef struct tagPETINFO
{
    TCHAR szName[50];
    TCHAR szBreed[50];
    TCHAR szGender[7];
    TCHAR szPrice[20];
    GroupIds iGroup;
} PETINFO;
            
```



Lo siguiente es del controlador WM \_ NOTIFY en el procedimiento de diálogo.


```C++
    case WM_NOTIFY:
        switch (((LPNMHDR) lParam)->code)
        {
        case LVN_GETDISPINFO:
            {
                NMLVDISPINFO* plvdi = (NMLVDISPINFO*)lParam;    
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // rgPetInfo is an array of PETINFO structures.
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szName;
                    break;

                case 1:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szBreed;
                    break;

                case 2:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szGender;
                    break;

                case 3:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szPrice;
                    break;

                default:
                    break;
                }
                return TRUE;
            }
      // More notifications...
      }
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVN \_ GETDISPINFOW** (Unicode) y **LVN \_ GETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LVN \_ SETDISPINFO**](lvn-setdispinfo.md)
</dt> </dl>

 

 





