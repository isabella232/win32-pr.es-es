---
description: Si el servicio web XML al que desea acceder se creó mediante la exposición de una aplicación COM+, considere la posibilidad de acceder a él en modo de objeto activado por el cliente (DHCP), lo que evita la generación en tiempo de ejecución de un proxy y aumenta el rendimiento mediante conexiones persistentes.
ms.assetid: 471de0fa-3429-45f8-abe2-aff0cf6fb350
title: Acceso a servicios Web XML en modo DESA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50f1e15c18a925ba88f1b9c7c8267bfb2ef12292
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073030"
---
# <a name="accessing-xml-web-services-in-cao-mode"></a>Acceso a servicios Web XML en modo DESA

Si el servicio web XML al que desea acceder se creó mediante la exposición de una aplicación COM+, considere la posibilidad de acceder a él en modo de objeto activado por el cliente (DHCP), lo que evita la generación en tiempo de ejecución de un proxy y aumenta el rendimiento mediante conexiones persistentes. Para tener acceso a un servicio [](exporting-a-soap-enabled-application.md) web XML en modo LDAP, exporte [](importing-a-soap-enabled-application.md) primero la aplicación habilitada para SOAP correspondiente desde el servidor en modo proxy y, a continuación, importe la aplicación en el cliente desde el que desea acceder a la aplicación como un servicio web XML. A continuación, se pueden crear instancias de los componentes de la aplicación en el cliente como los componentes de las aplicaciones locales, por ejemplo, mediante **GetObject** y [**CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)

## <a name="user-interface"></a>Interfaz de usuario

No corresponde.

## <a name="visual-basic"></a>Visual Basic

En el siguiente Visual Basic de código muestra el uso de un componente de una aplicación COM+ que se ha expuesto como un servicio web XML en el modo DESER.


```VB
Set Obj = GetObject("progID")
output = Obj.Method(input)
```



## <a name="cc"></a>C/C++

En el fragmento de código siguiente se muestra el uso de un componente de una aplicación COM+ que se ha expuesto como un servicio web XML en el modo DEER.


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

[Acceso a servicios Web XML en modo WKO](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Información general sobre el servicio SOAP de COM+](com--soap-service-overview.md)
</dt> <dt>

[Creación de servicios Web XML](creating-xml-web-services.md)
</dt> <dt>

[Protección de servicios Web XML](securing-xml-web-services.md)
</dt> </dl>

 

 
