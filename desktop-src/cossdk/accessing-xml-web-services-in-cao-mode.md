---
description: Si el servicio Web XML al que desea tener acceso se ha creado mediante la exposición de una aplicación COM+, considere la posibilidad de tener acceso a él en modo de objeto activado en el cliente (CAO), lo que evita la generación en tiempo de ejecución de un proxy y aumenta el rendimiento mediante conexiones persistentes.
ms.assetid: 471de0fa-3429-45f8-abe2-aff0cf6fb350
title: Obtener acceso a los servicios Web XML en el modo de CAO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50f1e15c18a925ba88f1b9c7c8267bfb2ef12292
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686437"
---
# <a name="accessing-xml-web-services-in-cao-mode"></a>Obtener acceso a los servicios Web XML en el modo de CAO

Si el servicio Web XML al que desea tener acceso se ha creado mediante la exposición de una aplicación COM+, considere la posibilidad de tener acceso a él en modo de objeto activado en el cliente (CAO), lo que evita la generación en tiempo de ejecución de un proxy y aumenta el rendimiento mediante conexiones persistentes. Para tener acceso a un servicio Web XML en modo de CAO, primero [exporte](exporting-a-soap-enabled-application.md) la aplicación habilitada para SOAP correspondiente del servidor en modo proxy y, a continuación, [importe](importing-a-soap-enabled-application.md) la aplicación en el cliente desde el que desea obtener acceso a la aplicación como un servicio Web XML. A continuación, se pueden crear instancias de los componentes de la aplicación en el cliente, al igual que los componentes de las aplicaciones locales, por ejemplo, mediante **GetObject** e [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

## <a name="user-interface"></a>Interfaz de usuario

No corresponde.

## <a name="visual-basic"></a>Visual Basic

En el siguiente fragmento de código de Visual Basic se muestra el uso de un componente de una aplicación COM+ que se ha expuesto como un servicio Web XML en modo de CAO.


```VB
Set Obj = GetObject("progID")
output = Obj.Method(input)
```



## <a name="cc"></a>C/C++

En el fragmento de código siguiente se muestra el uso de un componente de una aplicación COM+ que se ha expuesto como un servicio Web XML en modo de CAO.


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

[Obtener acceso a los servicios Web XML en modo WKO](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Introducción al servicio SOAP de COM+](com--soap-service-overview.md)
</dt> <dt>

[Crear servicios Web XML](creating-xml-web-services.md)
</dt> <dt>

[Proteger los servicios Web XML](securing-xml-web-services.md)
</dt> </dl>

 

 
