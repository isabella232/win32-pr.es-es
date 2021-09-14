---
description: Puede acceder y usar cualquier servicio web XML, incluso si ese servicio web XML no se creó mediante COM+ o incluso Microsoft Windows, siempre que el servicio web XML publique una descripción WSDL de su sintaxis.
ms.assetid: 5b21ff0c-f3a5-464b-b927-a7872ac54fe2
title: Acceso a servicios web XML en modo WKO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e726f430c47b3202932796455e1cf997e370a022
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073029"
---
# <a name="accessing-xml-web-services-in-wko-mode"></a>Acceso a servicios web XML en modo WKO

Puede acceder y usar cualquier servicio web XML, incluso si ese servicio web XML no se creó mediante COM+ o incluso Microsoft Windows, siempre que el servicio web XML publique una descripción WSDL de su sintaxis. Solo tiene que crear una instancia del componente mediante el moniker soap:wsdl=URL, donde URL es la dirección URL de la descripción wsdl del servicio web XML al que desea acceder. Este es el modo de objeto conocido (WKO) de acceso a los servicios web XML.

Se puede llamar a los métodos del objeto sin ninguna consideración especial. Se accede al servicio web XML a través de una consulta SOAP y la respuesta se interpreta de forma transparente.

## <a name="component-services-administrative-tool"></a>Herramienta administrativa de servicios de componentes

No corresponde.

## <a name="visual-basic"></a>Visual Basic

El siguiente fragmento Visual Basic código de Microsoft muestra el uso de un servicio web XML en modo WKO.


```VB
Set Obj = GetObject("soap:wsdl=https://servername/vroot/progID.soap?WSDL")
output = Obj.Method(input)
```



En este fragmento de código, que muestra el uso de un componente de una aplicación COM+ que se ha expuesto como un servicio web XML, servername es el nombre de dominio completo del servidor que ofrece el servicio web XML; vroot es el directorio raíz virtual de IIS desde el que se expone el servicio web XML; y progID es el ProgID del componente que desea usar.

## <a name="cc"></a>C/C++

En el fragmento de código siguiente se muestra el uso de un servicio web XML en modo WKO.


```C++
HRESULT hr = CoGetObject(
     L"soap:wsdl=https://servername/vroot/progID.soap?WSDL",
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr); 
```



En este fragmento de código, que muestra el uso de un componente de una aplicación COM+ que se ha expuesto como un servicio web XML, servername es el nombre de dominio completo del servidor que ofrece el servicio web XML; vroot es el directorio raíz virtual de IIS desde el que se expone el servicio web XML; y progID es el ProgID del componente que desea usar.

## <a name="remarks"></a>Observaciones

Cuando se accede por primera vez a un servicio web XML en modo WKO, COM+ genera un cliente proxy y lo compila en segundo plano. Esta generación en tiempo de ejecución y la falta de conexiones persistentes en el modo WKO tienen como resultado un rendimiento considerablemente reducido en comparación con el modo DESA.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso a servicios web XML en modo DESA](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Información general sobre el servicio SOAP de COM+](com--soap-service-overview.md)
</dt> <dt>

[Creación de servicios web XML](creating-xml-web-services.md)
</dt> <dt>

[Protección de servicios Web XML](securing-xml-web-services.md)
</dt> </dl>

 

 



