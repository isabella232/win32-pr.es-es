---
title: Archivo de extensión de servicio web
description: En esta sección se describe el archivo de extensión de servicio web.
ms.assetid: 856d4ff5-2292-4d87-ae7c-19b100fd1cb3
keywords:
- Servicios web de archivo de extensión de servicio web para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1b11e8e871399e1a499a6cfbb68a8e66b152d8f07f4fa5f2cda6585678af8e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707235"
---
# <a name="web-service-extension-file"></a>Archivo de extensión de servicio web

En esta sección se describe el archivo de extensión de servicio web.


El archivo WSX (extensión de servicio WCF) es nuestro archivo de extensión para permitir que la aplicación manipule comportamientos locales que no afecten a la representación de datos de conexión. Debe ser extensible que podamos agregar nuevas características en el futuro sin romper la interoperabilidad.

La estructura general de WSX imitaría la estructura del archivo XSD o WSDL, que es un archivo XML que mantiene la misma estructura que el archivo de entrada principal. Los atributos adicionales del mismo token con nombre del archivo principal especificarían los atributos que la aplicación quiere controlar sobre el comportamiento predeterminado.

Es posible que no haga nada aquí en M3. En V1, puedo ver que se admiten los siguientes atributos:

Uso Especificación del campo count argument/parameter.

Se trata de un atributo de elemento, pero solo se aplica al tipo de matriz. El atributo IsCountOf especifica el elemento de matriz. El campo o parámetro count no aparece en la conexión.

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

Especificación de la devolución de llamada de lectura y escritura para el tipo personalizado

Estos atributos fuerzan wsutil.exe generar [**WS \_ CUSTOM \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type) para el tipo especificado. El atributo de devolución de llamada personalizado especifica la rutina de devolución de llamada de lectura y la devolución de llamada \_ personalizada especifica la rutina de [](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) \_ [**devolución de llamada de**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) escritura.

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="mytype" custom_readcallback="myreadcallback" custom_writecallback="mywritecallback"> 
 </element>
</xs:schema>
```

Podemos tener un archivo WSX correspondiente para describir su comportamiento local:

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

WsUtil.exe genera el siguiente prototipo para la estructura :

``` syntax
typedef struct FooInParam
{
  ULONG MyLocalArrayCount;
  int * MyArray;
};
```

 

 




