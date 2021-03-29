---
description: Puede obtener acceso y utilizar cualquier servicio Web XML, incluso si ese servicio Web XML no se creó con COM+ o incluso Microsoft Windows, siempre y cuando el servicio Web XML publique una descripción WSDL de su sintaxis.
ms.assetid: 5b21ff0c-f3a5-464b-b927-a7872ac54fe2
title: Obtener acceso a los servicios Web XML en modo WKO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e726f430c47b3202932796455e1cf997e370a022
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807297"
---
# <a name="accessing-xml-web-services-in-wko-mode"></a>Obtener acceso a los servicios Web XML en modo WKO

Puede obtener acceso y utilizar cualquier servicio Web XML, incluso si ese servicio Web XML no se creó con COM+ o incluso Microsoft Windows, siempre y cuando el servicio Web XML publique una descripción WSDL de su sintaxis. Basta con crear una instancia del componente mediante el moniker SOAP: WSDL = URL, donde URL es la dirección URL de la descripción WSDL del servicio Web XML al que desea obtener acceso. Este es el modo de objeto conocido (WKO) de tener acceso a los servicios Web XML.

Se puede llamar a los métodos del objeto sin ninguna consideración especial. Se tiene acceso al servicio Web XML a través de una consulta SOAP y la respuesta se interpreta de forma transparente.

## <a name="component-services-administrative-tool"></a>Herramienta administrativa Servicios de componentes

No corresponde.

## <a name="visual-basic"></a>Visual Basic

En el siguiente fragmento de código de Microsoft Visual Basic se muestra el uso de un servicio Web XML en modo WKO.


```VB
Set Obj = GetObject("soap:wsdl=https://servername/vroot/progID.soap?WSDL")
output = Obj.Method(input)
```



En este fragmento de código, que muestra el uso de un componente de una aplicación COM+ que se ha expuesto como un servicio Web XML, ServerName es el nombre de dominio completo del servidor que ofrece el servicio Web XML. vroot es el directorio raíz virtual de IIS desde el que se expone el servicio Web XML. y progID es el ProgID del componente que desea usar.

## <a name="cc"></a>C/C++

En el fragmento de código siguiente se muestra el uso de un servicio Web XML en modo WKO.


```C++
HRESULT hr = CoGetObject(
     L"soap:wsdl=https://servername/vroot/progID.soap?WSDL",
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr); 
```



En este fragmento de código, que muestra el uso de un componente de una aplicación COM+ que se ha expuesto como un servicio Web XML, ServerName es el nombre de dominio completo del servidor que ofrece el servicio Web XML. vroot es el directorio raíz virtual de IIS desde el que se expone el servicio Web XML. y progID es el ProgID del componente que desea usar.

## <a name="remarks"></a>Observaciones

Cuando se obtiene acceso por primera vez a un servicio Web XML en el modo WKO, COM+ genera un cliente proxy y lo compila en segundo plano. Esta generación en tiempo de ejecución y la falta de conexiones persistentes en modo WKO producen un rendimiento significativamente menor en comparación con el modo de CAO.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener acceso a los servicios Web XML en el modo de CAO](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Introducción al servicio SOAP de COM+](com--soap-service-overview.md)
</dt> <dt>

[Crear servicios Web XML](creating-xml-web-services.md)
</dt> <dt>

[Proteger los servicios Web XML](securing-xml-web-services.md)
</dt> </dl>

 

 



