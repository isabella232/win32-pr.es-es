---
title: Elemento LOGURL
description: El elemento LOGURL indica a Reproductor de Windows Media que envíe los datos de registro a la dirección URL especificada.
ms.assetid: fc1895af-c9d7-43ca-9839-7e884cc219f4
keywords:
- Elemento LOGURL Reproductor de Windows Media
topic_type:
- apiref
api_name:
- LOGURL Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fad38d8272c2f4d8a8e7a8f3f06e4d8db149f0d314e93b32d6f8d330e281f268
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934595"
---
# <a name="logurl-element"></a>Elemento LOGURL

El **elemento LOGURL** indica a Reproductor de Windows Media que envíe los datos de registro a la dirección URL especificada.

``` syntax
<LOGURL
   HREF = "URL"
/>
```

## <a name="attributes"></a>Atributos

**HREF** (obligatorio)

Dirección URL a un host que puede procesar solicitudes de registro.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos           |
|-----------------|--------------------|
| Elementos primarios | **ASX**, **ENTRY** |
| Elementos secundarios  | Ninguno               |



 

## <a name="remarks"></a>Observaciones

El **elemento LOGURL** permite que una lista de reproducción de metarchivo de cliente envíe información de registro adicional a los servidores especificados. La información de registro se envía automáticamente al servidor de origen de una lista de reproducción cuando se abre y a cada **LOGURL** especificado para el elemento **ASX,** si existe alguno. La información de registro también se envía a cada **LOGURL** especificado para un **elemento ENTRY** cuando se alcanza esa entrada. La dirección URL especificada en el **atributo HREF** de un elemento **LOGURL** debe ser la dirección de un host que pueda procesar solicitudes de registro. La dirección URL puede ser cualquier dirección URL HTTP válida. La dirección URL también puede indicar la ubicación de un script CGI.

Los únicos protocolos válidos para **un elemento LOGURL** son HTTP y HTTPS.

Un **elemento LOGURL** dentro del ámbito de un elemento **ASX** solo es aplicable al metarchivo en el que reside, independientemente de si se hace referencia a ese metarchivo desde otro metarchivo. Un **elemento LOGURL** fuerza el envío de datos de registro para todo el contenido transmitido desde su ámbito definido y solo para el contenido transmitido desde su ámbito definido. Los datos de registro se envían al servidor de origen y a todas las direcciones URL enumeradas en cada **elemento LOGURL** del ámbito. Los datos de registro solo se envían una vez a cada dirección URL de la lista, incluso si la misma dirección URL aparece más de una vez en un ámbito determinado. Una repetición de **una entrada daría** lugar a otro envío a las direcciones URL enumeradas.

No hay ningún límite en el número de elementos **LOGURL** en una lista de reproducción de metarchivo.

## <a name="examples"></a>Ejemplos


```XML
<ASX VERSION="3.0">
  <TITLE>Example Media Player Show</TITLE>
  <LOGURL HREF="https://example.microsoft.com/info/showlog.asp?whatsup" />
  <ENTRY>
    <REF href="mms://ucast.proseware.com/Media1.asf" />
    <LOGURL HREF="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal"/>
  </ENTRY>
</ASX>
```



A continuación se muestran ejemplos de direcciones URL válidas.

Dirección URL de una aplicación ISAPI:


```XML
https://www.proseware.com/logs/WMSLogging.dll
```



Dirección URL de un script CGI:


```XML
https://www.proseware.com/cgi-bin/My_WMS_Logging_Script.pl
```



Una dirección URL HTTP válida:


```XML
https://www.proseware.com/some/arbitrary/path/My_WMS_Logging_Page.asp?PubPoint=FooPubPoint&AnotherName=AnotherValue
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 70 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referencia de metarchivo multimedia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





