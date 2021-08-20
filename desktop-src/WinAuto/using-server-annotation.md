---
title: Usar anotación de servidor
description: En este tema se proporciona información sobre el uso de la anotación de servidor para especificar un objeto de devolución de llamada.
ms.assetid: eeeebddc-2752-4d8f-b4fa-38ce156acc08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b2955d49431b502c8587484208321bc1ab1bc0c8201fabf466b60b68f548a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823911"
---
# <a name="using-server-annotation"></a>Usar anotación de servidor

En este tema se proporciona información sobre el uso de la anotación de servidor para especificar un objeto de devolución de llamada.

**Para invalidar una propiedad que especifica un objeto de devolución de llamada**

1.  Obtenga un [**puntero de interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) al elemento accesible que se va a anotar.
2.  Llame [**a QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el elemento accesible para obtener un puntero de [**interfaz IAccIdentity.**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity)
3.  Llame a [**IAccIdentity::GetIdentityString()**](/windows/desktop/api/Oleacc/nf-oleacc-iaccidentity-getidentitystring) en el puntero de interfaz [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) para obtener una cadena que identifique de forma única el elemento accesible que se va a anotar.
4.  Use [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) para crear el [**objeto IAccPropServices.**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)
5.  Cree un objeto de Modelo de objetos componentes (COM) que implemente [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver).
6.  Llame a [**IAccPropServices::SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver), pasando la cadena de identidad, un GUID que indica la propiedad que se va a invalidar y un puntero al objeto de devolución de llamada [**IAccPropServer.**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver)
7.  Liberar punteros de interfaz y memoria libre.

Cuando un cliente solicita la propiedad del elemento accesible, se llamará al objeto de devolución de llamada y devolverá el valor al cliente.

Al igual que al especificar un valor, los desarrolladores de servidores también pueden usar el método [**IAccPropServices::ComposeHwndIdentityString**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-composehwndidentitystring) para obtener una cadena de identidad; o pueden usar el método [**IAccPropServices::SetHwndPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropserver) y especificar los parámetros *hwnd*, *idObject* o *idChild* en lugar de una cadena de identidad.

Al usar [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver) o [**SetHwndPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropserver) en un objeto contenedor, los desarrolladores de servidores pueden especificar opcionalmente que la información de invalidación también se aplique a todos los elementos secundarios de ese contenedor.

Los servidores pueden borrar explícitamente la anotación en cualquier momento mediante [**IAccPropServices::ClearProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearprops). Esto no suele ser necesario, ya que el servicio de anotación limpiará y liberará automáticamente la información de anotación cuando desaparezca el elemento accesible anotado.

A continuación se muestra una lista de propiedades que se pueden anotar mediante este procedimiento.

## <a name="properties-supported-when-specifying-a-callback"></a>Propiedades admitidas al especificar una devolución de llamada

Al especificar una devolución de llamada, se pueden anotar las siguientes propiedades. Actualmente, estas propiedades no se pueden anotar directamente especificando un valor.



| Propiedad                      | Tipo                                                             |
|-------------------------------|------------------------------------------------------------------|
| NOMBRE DE ACC DE PROPID \_ \_             | VT \_ BSTR                                                         |
| DESCRIPCIÓN DE \_ PROPID ACC \_      | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ ROLE             | VT \_ I4                                                           |
| PROPID \_ ACC \_ STATE            | VT \_ I4                                                           |
| PROPID \_ ACC \_ HELP             | VT \_ BSTR                                                         |
| TECLADO \_ PROPID \_ ACCSHORTCUT | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ DEFAULTACTION    | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ VALUEMAP         | VT \_ BSTR                                                         |
| MAPA DE \_ ROLES DE PROPID ACC \_          | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ STATEMAP         | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ FOCUS            | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ SELECTION        | VT \_ DISPATCH<br/> VT \_ I4<br/> VT \_ UNKNOWN<br/> |
| PROPID \_ ACC \_ PARENT           | VT \_ DISPATCH                                                     |
| PROPID \_ ACC \_ NAV \_ UP          | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| NAVEGACIÓN \_ DE PROPID ACC \_ \_ HACIA ABAJO        | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ LEFT        | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| DERECHA DE \_ NAVEGACIÓN DE PROPID ACC \_ \_       | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ PREV        | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ NEXT        | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ FIRSTCHILD  | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ LASTCHILD   | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |



 

 

