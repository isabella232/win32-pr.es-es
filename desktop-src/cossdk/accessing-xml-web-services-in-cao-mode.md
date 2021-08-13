---
description: Si el servicio web XML al que desea acceder se creó mediante la exposición de una aplicación COM+, considere la posibilidad de acceder a él en modo de objeto activado por el cliente (DHCP), lo que evita la generación en tiempo de ejecución de un proxy y aumenta el rendimiento mediante conexiones persistentes.
ms.assetid: 471de0fa-3429-45f8-abe2-aff0cf6fb350
title: Acceso a servicios web XML en modo DESA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e3f8dc1fa3c037d03d8b69cf45737c7211d92f7d38e733a97b9be109a2243a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549481"
---
# <a name="accessing-xml-web-services-in-cao-mode"></a>Acceso a servicios web XML en modo DESA

Si el servicio web XML al que desea acceder se creó mediante la exposición de una aplicación COM+, considere la posibilidad de acceder a él en modo de objeto activado por el cliente (DHCP), lo que evita la generación en tiempo de ejecución de un proxy y aumenta el rendimiento mediante conexiones persistentes. Para tener acceso a un servicio [](exporting-a-soap-enabled-application.md) web XML en modo SMTP, exporte [](importing-a-soap-enabled-application.md) primero la aplicación habilitada para SOAP correspondiente desde el servidor en modo proxy y, a continuación, importe la aplicación en el cliente desde el que desea acceder a la aplicación como un servicio web XML. A continuación, se pueden crear instancias de los componentes de la aplicación en el cliente igual que los componentes de las aplicaciones locales, por ejemplo, mediante **GetObject** y [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

## <a name="user-interface"></a>Interfaz de usuario

No corresponde.

## <a name="visual-basic"></a>Visual Basic

En el Visual Basic fragmento de código siguiente se muestra el uso de un componente de una aplicación COM+ que se ha expuesto como un servicio web XML en el modo QR.


```VB
Set Obj = GetObject("progID")
output = Obj.Method(input)
```



## <a name="cc"></a>C/C++

En el fragmento de código siguiente se muestra el uso de un componente de una aplicación COM+ que se ha expuesto como un servicio web XML en el modo QR.


```C++
HRESULT hr = CoCreateInstance(
     CLSID_CObject,  // CLSID of the server component
     NULL,
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso a servicios web XML en modo WKO](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Información general sobre el servicio SOAP de COM+](com--soap-service-overview.md)
</dt> <dt>

[Creación de servicios web XML](creating-xml-web-services.md)
</dt> <dt>

[Protección de servicios Web XML](securing-xml-web-services.md)
</dt> </dl>

 

 
