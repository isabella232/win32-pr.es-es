---
title: Mensaje de WM_GETOBJECT (Winuser. h)
description: Lo envían Microsoft Active Accessibility y la automatización de la interfaz de usuario de Microsoft para obtener información sobre un objeto accesible incluido en una aplicación de servidor.
ms.assetid: 59350aa1-1697-4110-b9a6-f30ee56c4cff
keywords:
- WM_GETOBJECT mensaje accesibilidad a Windows
topic_type:
- apiref
api_name:
- WM_GETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcac5c7f6dd8203c32b9f6f3c4eb59144cc3f8ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151214"
---
# <a name="wm_getobject-message"></a>\_Mensaje GETOBJECT de WM

Lo envían Microsoft Active Accessibility y la automatización de la interfaz de usuario de Microsoft para obtener información sobre un objeto accesible incluido en una aplicación de servidor.

Las aplicaciones nunca envían este mensaje directamente. Microsoft Active Accessibility envía este mensaje en respuesta a las llamadas a [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)o [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow). Sin embargo, las aplicaciones de servidor controlan este mensaje. La automatización de la interfaz de usuario envía este mensaje en respuesta a las llamadas a [**IUIAutomation:: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)y [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), y al controlar los eventos para los que se ha registrado un cliente.


```C++
dwFlags = (WPARAM)(DWORD) wParam;
dwObjId = (LPARAM)(DWORD) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* 
</dt> <dd>

Proporciona información adicional sobre el mensaje y solo lo utiliza el sistema. Los servidores pasan *dwFlags* como el parámetro *wParam* en la llamada a [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) al administrar el mensaje.

</dd> <dt>

*dwObjId* 
</dt> <dd>

Identificador de objeto. Este valor es una de las constantes de [identificador de objeto](object-identifiers.md) o un identificador de objeto personalizado. Una aplicación de servidor debe comprobar este valor para identificar el tipo de información que se solicita. Antes de comparar este valor con los valores de OBJID \_ , el servidor debe convertirlo en **DWORD**; de lo contrario, en Windows de 64 bits, la extensión de signo de *lParam* puede interferir con la comparación.

-   Si *dwObjId* es uno de los valores de objid \_ como [**el \_ cliente de objid**](object-identifiers.md), la solicitud es para un objeto de Active Accessibility de Microsoft que implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).
-   Si *dwObjId* es igual a **UiaRootObjectId**, la solicitud es para un proveedor de automatización de la interfaz de usuario. Si el servidor está implementando la automatización de la interfaz de usuario, debe devolver un proveedor mediante la función [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .
-   Si *dwObjId* es [**OBJID \_ NATIVEOM**](object-identifiers.md), la solicitud es para el modelo de objetos subyacente del control. Si el control admite esta solicitud, debe devolver una interfaz COM adecuada llamando a la función [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .
-   Si *dwObjId* es [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md), la solicitud es para que el control se identifique como un control estándar de Windows o un control común implementado por la biblioteca de controles comunes (ComCtrl.dll).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la ventana o el control no necesitan responder a este mensaje, debe pasar el mensaje a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . de lo contrario, la ventana o el control deben devolver un valor que corresponda a la solicitud especificada por *dwObjId*:

-   Si la ventana o el control implementan la automatización de la interfaz de usuario, la ventana o el control deben devolver el valor obtenido mediante una llamada a la función [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .
-   Si *dwObjId* es [**OBJID \_ NATIVEOM**](object-identifiers.md) y la ventana expone un modelo de objetos nativo, las ventanas deben devolver el valor obtenido mediante una llamada a la función [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .
-   Si *dwObjId* es [**el \_ cliente de OBJID**](object-identifiers.md) y la ventana implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), la ventana debe devolver el valor obtenido mediante una llamada a la función [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .

## <a name="remarks"></a>Observaciones

Cuando un cliente llama a [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) o a cualquiera de las otras funciones de **AccessibleObjectFrom**_X_ que recuperan una interfaz en un objeto, Microsoft Active Accessibility envía el mensaje de **WM \_ GETOBJECT** al procedimiento de ventana adecuado en la aplicación de servidor adecuada. Al procesar **WM \_ GETOBJECT**, las aplicaciones de servidor llaman a [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) y usan el valor devuelto de esta función como valor devuelto para el mensaje. Microsoft Active Accessibility, junto con la biblioteca COM, realiza el cálculo de referencias adecuado y pasa el puntero de interfaz del servidor de vuelta al cliente.

Los servidores no responden a **WM \_ GETOBJECT** antes de que el objeto se inicialice por completo o después de que empiece a cerrarse. Cuando una aplicación crea una ventana nueva, el sistema envía [**el \_ objeto \_ de evento Create**](event-constants.md) para notificar a los clientes antes de enviar el mensaje de [ \_ creación de WM](../winmsg/wm-create.md) al procedimiento de ventana de la aplicación. Dado que muchas aplicaciones usan WM \_ Create para iniciar su proceso de inicialización, los servidores no responden al mensaje de la **\_ GETOBJECT de WM** hasta que finaliza el procesamiento del mensaje de **\_ creación de WM** .

Un servidor utiliza **WM \_ GETOBJECT** para realizar las siguientes tareas:

-   [Crear nuevos objetos accesibles](create-new-accessible-objects.md)
-   [Reutilizar punteros existentes a objetos](reuse-existing-pointers-to-objects.md)
-   [Crear nuevas interfaces para el mismo objeto](create-new-interfaces-to-the-same-object.md)

En el caso de los clientes, esto significa que podrían recibir punteros de interfaz distintos para el mismo elemento de la interfaz de usuario, dependiendo de la acción del servidor. Para determinar si dos punteros de interfaz apuntan al mismo elemento de la interfaz de usuario, los clientes comparan las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del objeto. La comparación de punteros no funciona.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Redistribuible<br/>          | Active Accessibility 1,3 RDK en Windows NT 4,0 con SP6 y versiones posteriores y Windows 95<br/>              |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Cómo administrar WM \_ GETOBJECT](how-to-handle-wm-getobject.md)
</dt> <dt>

[Cómo \_ funciona WM GETOBJECT](how-wm-getobject-works.md)
</dt> <dt>

[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
</dt> </dl>

 

