---
description: Define un servicio que se va a hospedar en una función del generador de host.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: elemento hostedService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96c9f6e010989f4844d93299bb34f1ab8893236
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994792"
---
# <a name="hostedservice-element"></a>elemento hostedService

Define un servicio que se va a hospedar en una función del generador de host.

## <a name="usage"></a>Uso

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                     | Descripción                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Codename**](codename.md)<br/>     | Especifica el nombre que se usará para el tipo de puerto en el código generado. De forma predeterminada, el nombre del código se genera a partir del nombre completo del tipo de puerto.<br/> <br/> |
| [**portType**](porttype.md)<br/>     | Tipo de puerto para el que se va a generar el código.<br/> <br/>                                                                                                       |
| [**proxyClass**](proxyclass.md)<br/> | Nombre de clase que se generará a partir de la función de generador.<br/> <br/>                                                                                                      |
| [**ServiceID**](serviceid.md)<br/>   | URI que representa el identificador de servicio.<br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [**Archivo**](file.md)<br/> | Especificación del archivo de salida para el generador de código.<br/> <br/> |



## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | No            |



 

 




