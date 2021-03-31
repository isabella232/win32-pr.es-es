---
title: Código de notificación de LVN_GETDISPINFO (commctrl. h)
description: Enviado por un control de vista de lista a su ventana primaria. Es una solicitud para que la ventana primaria proporcione la información necesaria para mostrar u ordenar un elemento de vista de lista. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 04310e39-69bc-45d7-958c-00452279d7a9
keywords:
- LVN_GETDISPINFO controles de código de notificación de Windows
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
ms.openlocfilehash: f1585524dd447c4a1324dc5c7a235490de776fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804153"
---
# <a name="lvn_getdispinfo-notification-code"></a>Código de notificación de GETDISPINFO de LVN \_

Enviado por un control de vista de lista a su ventana primaria. Es una solicitud para que la ventana primaria proporcione la información necesaria para mostrar u ordenar un elemento de vista de lista. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
LVN_GETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . En la entrada, la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) contenida en esta estructura especifica el tipo de información requerida e identifica el elemento o subelemento de interés. Use la estructura **LVITEM** para devolver la información solicitada al control. Si el controlador de mensajes establece la \_ marca LVIF di \_ SETITEM en el miembro **Mask** de la estructura **LVITEM** , el control de vista de lista almacena la información solicitada y no la pedirá de nuevo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El receptor de notificaciones convierte *lParam* para recuperar la estructura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . El parámetro *wParam* contiene el código de notificación.

Un control de vista de lista envía el código de notificación **LVN \_ GETDISPINFO** para recuperar la información de los elementos que almacena la aplicación en lugar del control. La información puede ser información de texto o de icono para un elemento. También puede ser información sobre el estado del elemento. Vea el mensaje [**LVM \_ SETCALLBACKMASK**](lvm-setcallbackmask.md) para obtener más información sobre cómo implementar el estado del elemento en una devolución de llamada.

Para obtener más información sobre las devoluciones de llamada de vista de lista, vea [elementos de devolución de llamada y máscara de devolución de llamada](list-view-controls-overview.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo se puede controlar este código de notificación para establecer el texto de las columnas de una vista de lista. Los datos de cada elemento se guardan en la estructura siguiente.


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



A continuación se indica el \_ controlador de notificaciones de WM en el procedimiento de cuadro de diálogo.


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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVN \_ GETDISPINFOW** (Unicode) y **LVN \_ GETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LVN \_ SETDISPINFO**](lvn-setdispinfo.md)
</dt> </dl>

 

 





