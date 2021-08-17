---
title: WM_GETOBJECT mensaje (Winuser.h)
description: Enviados por Microsoft Active Accessibility y Microsoft Automatización de la interfaz de usuario obtener información sobre un objeto accesible contenido en una aplicación de servidor.
ms.assetid: 59350aa1-1697-4110-b9a6-f30ee56c4cff
keywords:
- WM_GETOBJECT de Windows accesibilidad
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
ms.openlocfilehash: 2767a689b87c2e293cb481647c61a29ad40167992e637802d1c0be63d18fc74e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744741"
---
# <a name="wm_getobject-message"></a>Mensaje \_ GETOBJECT de WM

Enviados por Microsoft Active Accessibility y Microsoft Automatización de la interfaz de usuario obtener información sobre un objeto accesible contenido en una aplicación de servidor.

Las aplicaciones nunca envían este mensaje directamente. Microsoft Active Accessibility este mensaje en respuesta a llamadas a [**AccessibleObjectFromPoint,**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)o [**AccessibleObjectFromWindow.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) Sin embargo, las aplicaciones de servidor controlan este mensaje. Automatización de la interfaz de usuario este mensaje en respuesta a las llamadas a [**IUIAutomation::ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)y [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), y al controlar eventos para los que se ha registrado un cliente.


```C++
dwFlags = (WPARAM)(DWORD) wParam;
dwObjId = (LPARAM)(DWORD) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* 
</dt> <dd>

Proporciona información adicional sobre el mensaje y solo lo usa el sistema. Los servidores *pasan dwFlags* como parámetro *wParam* en la llamada a [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) al controlar el mensaje.

</dd> <dt>

*dwObjId* 
</dt> <dd>

Identificador de objeto. Este valor es una de las constantes [de identificador de](object-identifiers.md) objeto o un identificador de objeto personalizado. Una aplicación de servidor debe comprobar este valor para identificar el tipo de información que se solicita. Antes de comparar este valor con los valores OBJID, el servidor debe convertirlo a DWORD; de lo contrario, en el Windows de 64 bits, la extensión de signo de \_ *lParam* puede interferir con la comparación. 

-   Si *dwObjId* es uno de los valores de OBJID, como \_ [**OBJID \_ CLIENT,**](object-identifiers.md)la solicitud es para un objeto Microsoft Active Accessibility que implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).
-   Si *dwObjId* es igual a **UiaRootObjectId,** la solicitud es para un proveedor Automatización de la interfaz de usuario datos. Si el servidor está implementando Automatización de la interfaz de usuario, debe devolver un proveedor mediante la [**función UiaReturnRawElementProvider.**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider)
-   Si *dwObjId* es [**OBJID \_ NATIVEOM,**](object-identifiers.md)la solicitud es para el modelo de objetos subyacente del control. Si el control admite esta solicitud, debe devolver una interfaz COM adecuada llamando a la [**función LresultFromObject.**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
-   Si *dwObjId* es [**OBJID \_ QUERYCLASSNAMEIDX,**](object-identifiers.md)la solicitud es para que el control se identifique como un control Windows estándar o un control común implementado por la biblioteca de controles común (ComCtrl.dll).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la ventana o el control no necesita responder a este mensaje, debe pasar el mensaje a la [**función DefWindowProc;**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) De lo contrario, la ventana o el control deben devolver un valor que se corresponda con la solicitud especificada por *dwObjId*:

-   Si la ventana o el control Automatización de la interfaz de usuario, la ventana o el control deben devolver el valor obtenido por una llamada a la función [**UiaReturnRawElementProvider.**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider)
-   Si *dwObjId* es [**OBJID \_ NATIVEOM**](object-identifiers.md) y la ventana expone un modelo de objetos nativo, las ventanas deben devolver el valor obtenido por una llamada a la función [**LresultFromObject.**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
-   Si *dwObjId* es [**OBJID \_ CLIENT**](object-identifiers.md) y la ventana implementa [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)la ventana debe devolver el valor obtenido por una llamada a la función [**LresultFromObject.**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)

## <a name="remarks"></a>Comentarios

Cuando un cliente llama a [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) o a cualquiera de las otras funciones **AccessibleObjectFrom**_X_ que recuperan una interfaz a un objeto , Microsoft Active Accessibility envía el mensaje **WM \_ GETOBJECT** al procedimiento de ventana adecuado dentro de la aplicación de servidor adecuada. Al procesar **WM \_ GETOBJECT,** las aplicaciones de servidor llaman [**a LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) y usan el valor devuelto de esta función como valor devuelto para el mensaje. Microsoft Active Accessibility, junto con la biblioteca COM, realiza la serialización adecuada y pasa el puntero de interfaz del servidor al cliente.

Los servidores no responden a **WM \_ GETOBJECT antes** de que el objeto se inicialice por completo o después de que comience a cerrarse. Cuando una aplicación crea una nueva ventana, el sistema envía [**EVENT \_ OBJECT \_ CREATE**](event-constants.md) para notificar a los clientes antes de enviar el mensaje [WM \_ CREATE](../winmsg/wm-create.md) al procedimiento de ventana de la aplicación. Dado que muchas aplicaciones usan WM CREATE para iniciar su proceso de inicialización, los servidores no responden al mensaje \_ **WM \_ GETOBJECT** hasta que finalizan el procesamiento **del mensaje WM \_ CREATE.**

Un servidor usa **WM \_ GETOBJECT** para realizar las siguientes tareas:

-   [Crear nuevos objetos accesibles](create-new-accessible-objects.md)
-   [Reutilizar punteros existentes a objetos](reuse-existing-pointers-to-objects.md)
-   [Crear nuevas interfaces para el mismo objeto](create-new-interfaces-to-the-same-object.md)

Para los clientes, esto significa que pueden recibir punteros de interfaz distintos para el mismo elemento de interfaz de usuario, en función de la acción del servidor. Para determinar si dos punteros de interfaz apuntan al mismo elemento de interfaz de usuario, los clientes comparan [**las propiedades IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del objeto. La comparación de punteros no funciona.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Redistribuible<br/>          | Active Accessibility 1.3 RDK en Windows NT 4.0 con SP6 y versiones posteriores y Windows 95<br/>              |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Cómo controlar WM \_ GETOBJECT](how-to-handle-wm-getobject.md)
</dt> <dt>

[Funcionamiento de WM \_ GETOBJECT](how-wm-getobject-works.md)
</dt> <dt>

[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
</dt> </dl>

 

