---
title: Archivo de extensión de servicio Web
description: En esta sección se describe el archivo de extensión de servicio Web.
ms.assetid: 856d4ff5-2292-4d87-ae7c-19b100fd1cb3
keywords:
- Servicios Web de archivo de extensión de servicio web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0802e31895aa5dd5051c94746e774033a1ebe677
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104359533"
---
# <a name="web-service-extension-file"></a>Archivo de extensión de servicio Web

En esta sección se describe el archivo de extensión de servicio Web.


El archivo WSX (extensión de servicio WCF) es el archivo de extensión que permite a la aplicación manipular comportamientos locales que no afectan a la representación de los datos de conexión. Debe ser extensible que podamos agregar nuevas características en el futuro sin interrumpir la interoperabilidad.

La estructura general de WSX imitaría la estructura del archivo XSD o WSDL, que es un archivo XML que mantiene la misma estructura que el archivo de entrada principal. Los atributos adicionales en el mismo token con nombre en el archivo principal especificarían los atributos que la aplicación desea controlar sobre el comportamiento predeterminado.

Es posible que no haga nada aquí en m3. En la versión 1, se puede ver que se admiten los siguientes atributos:

Uso que especifica el argumento Count o el campo de parámetro.

Se trata de un atributo de elemento, pero aplicable solo al tipo de matriz. El atributo IsCountOf especifica el elemento de la matriz. El campo/parámetro de recuento no aparece en el cable.

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="FooInParam">
  <complexType> 
   <!-- MyArray field is presented in WSDL file as an element -->
    <element name="MyArrayCount" IsCountOf="MyArray"></element>
   </complexType>
  </element>
 </xs:schema>
```

Especificar una devolución de llamada de lectura/escritura para el tipo personalizado

Estos atributos fuerzan wsutil.exe para generar el [**\_ \_ tipo personalizado de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type) para el tipo especificado. \_el atributo ReadCallBack personalizado especifica la rutina de [**devolución de llamada de lectura**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) y writecallback personalizado \_ especifica la rutina de [**devolución de llamada de escritura**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) .

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="mytype" custom_readcallback="myreadcallback" custom_writecallback="mywritecallback"> 
 </element>
</xs:schema>
```

Podemos tener un archivo WSX coincidente para describir su comportamiento local:

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">

 <element name="FooInParam" DataValidationRoutine="MyArrayValidation">
  <complexType> 
   <element name="MyLocalArrayCount" IsCountOf="MyArray"></element> 
  </complexType>
 </element>
</xs:schema>
```

WsUtil.exe genera el siguiente prototipo para la estructura:

``` syntax
typedef struct FooInParam
{
  ULONG MyLocalArrayCount;
  int * MyArray;
};
```

 

 




