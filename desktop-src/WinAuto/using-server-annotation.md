---
title: Usar la anotación del servidor
description: En este tema se proporciona información sobre cómo utilizar la anotación de servidor para especificar un objeto de devolución de llamada.
ms.assetid: eeeebddc-2752-4d8f-b4fa-38ce156acc08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb545cd4dd016901d69f67d5ab5cab15dda08875
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695676"
---
# <a name="using-server-annotation"></a>Usar la anotación del servidor

En este tema se proporciona información sobre cómo utilizar la anotación de servidor para especificar un objeto de devolución de llamada.

**Para reemplazar una propiedad que especifica un objeto de devolución de llamada**

1.  Obtener un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) al elemento accesible que se va a anotar.
2.  Llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el elemento accesible para obtener un puntero de interfaz [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) .
3.  Llame a [**IAccIdentity:: GetIdentityString ()**](/windows/desktop/api/Oleacc/nf-oleacc-iaccidentity-getidentitystring) en el puntero de la interfaz [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) para obtener una cadena que identifique de forma única el elemento accesible que se va a anotar.
4.  Use [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) para crear el objeto [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
5.  Cree un objeto de modelo de objetos componentes (COM) que implemente [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver).
6.  Llame a [**IAccPropServices:: SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver), pasando la cadena de identidad, un GUID que indica la propiedad que se va a reemplazar y un puntero al objeto de devolución de llamada [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver) .
7.  Punteros de interfaz de versión y memoria libre.

Cuando un cliente solicita la propiedad del elemento accesible, se llamará al objeto de devolución de llamada y se devolverá el valor al cliente.

Al igual que cuando se especifica un valor, los desarrolladores del servidor pueden usar el método [**IAccPropServices:: ComposeHwndIdentityString**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-composehwndidentitystring) para obtener una cadena de identidad. o bien, pueden usar el método [**IAccPropServices:: SetHwndPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropserver) y especificar los parámetros *hWnd*, *idObject* o *idChild* en lugar de una cadena de identidad.

Cuando se usa [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver) o [**SetHwndPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropserver) en un objeto contenedor, los desarrolladores de servidores pueden especificar opcionalmente que la información de invalidación también debe aplicarse a todos los elementos secundarios de dicho contenedor.

Los servidores pueden borrar explícitamente la anotación en cualquier momento mediante [**IAccPropServices:: ClearProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearprops). Normalmente, esto no es necesario, ya que el servicio de anotaciones limpiará y liberará automáticamente la información de la anotación cuando desaparezca el elemento accesible que se va a anotar.

A continuación se muestra una lista de las propiedades que se pueden anotar mediante este procedimiento.

## <a name="properties-supported-when-specifying-a-callback"></a>Propiedades admitidas al especificar una devolución de llamada

Al especificar una devolución de llamada, se pueden anotar las siguientes propiedades. Actualmente, estas propiedades no se pueden anotar directamente especificando un valor.



| Propiedad                      | Tipo                                                             |
|-------------------------------|------------------------------------------------------------------|
| nombre de la \_ ACC \_             | VT \_ BSTR                                                         |
| Descripción de la definición del PROPID \_ \_      | VT \_ BSTR                                                         |
| rol de PROPID \_ ACC \_             | VT \_ I4                                                           |
| Estado de la ACC de PROPID \_ \_            | VT \_ I4                                                           |
| ayuda de la ACC de PROPID \_ \_             | VT \_ BSTR                                                         |
| KEYBOARDSHORTCUT de la \_ ACC \_ | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ DEFAULTACTION    | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ VALUEMAP         | VT \_ BSTR                                                         |
| ROLEMAP de la \_ ACC \_          | VT \_ BSTR                                                         |
| STATEMAP de la \_ ACC \_         | VT \_ BSTR                                                         |
| el \_ foco de la ACC \_            | distribución de VT \_<br/> VT \_ I4<br/>                        |
| selección de la \_ ACC. \_        | distribución de VT \_<br/> VT \_ I4<br/> VT \_ desconocido<br/> |
| PROPID \_ ACC \_ Parent           | distribución de VT \_                                                     |
| \_parabar \_ \_ de PROPID          | distribución de VT \_<br/> VT \_ I4<br/>                        |
| \_Nº de \_ denav de la ACC \_        | distribución de VT \_<br/> VT \_ I4<br/>                        |
| se \_ ha \_ dejado la ACC de PROPID \_        | distribución de VT \_<br/> VT \_ I4<br/>                        |
| derecho de la ACC de PROPID \_ \_ \_       | distribución de VT \_<br/> VT \_ I4<br/>                        |
| Nº de NAV de la \_ ACC \_ \_ prev        | distribución de VT \_<br/> VT \_ I4<br/>                        |
| \_ \_ \_ siguiente        | distribución de VT \_<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ FIRSTCHILD  | distribución de VT \_<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ LASTCHILD   | distribución de VT \_<br/> VT \_ I4<br/>                        |



 

 

