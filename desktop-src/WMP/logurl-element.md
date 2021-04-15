---
title: Elemento LOGURL
description: El elemento LOGURL indica a Windows Media Player que envíe los datos de registro a la dirección URL especificada.
ms.assetid: fc1895af-c9d7-43ca-9839-7e884cc219f4
keywords:
- Elemento LOGURL Media Player Windows
topic_type:
- apiref
api_name:
- LOGURL Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f5fc4a5259f009e7298c0609fc4e6fa8c533b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708831"
---
# <a name="logurl-element"></a>Elemento LOGURL

El elemento **LOGURL** indica a Windows Media Player que envíe los datos de registro a la dirección URL especificada.

``` syntax
<LOGURL
   HREF = "URL"
/>
```

## <a name="attributes"></a>Atributos

**Href** (obligatorio)

Dirección URL de un host que puede procesar solicitudes de registro.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos           |
|-----------------|--------------------|
| Elementos primarios | **ASX**, **entrada** |
| Elementos secundarios  | Ninguno               |



 

## <a name="remarks"></a>Observaciones

El elemento **LOGURL** permite que una lista de reproducción de metarchivo de cliente envíe información de registro adicional a los servidores especificados. La información de registro se envía automáticamente al servidor de origen de una lista de reproducción cuando se abre y a cada uno de los **LOGURL** especificados para el elemento **ASX** , si hay alguno. La información de registro también se envía a cada **LOGURL** especificado para un elemento de **entrada** cuando se alcanza dicha entrada. La dirección URL especificada en el atributo **href** de un elemento **LOGURL** debe ser la dirección de un host que pueda procesar solicitudes de registro. La dirección URL puede ser cualquier dirección URL HTTP válida. La dirección URL también puede indicar la ubicación de un script CGI.

Los únicos protocolos válidos para un elemento **LOGURL** son http y https.

Un elemento **LOGURL** dentro del ámbito de un elemento **ASX** solo es aplicable al metarchivo en el que reside, independientemente de si se hace referencia a ese metarchivo desde otro metarchivo. Un elemento **LOGURL** fuerza el envío de datos de registro para todo el contenido transmitido desde dentro de su ámbito definido y solo para el contenido transmitido desde dentro de su ámbito definido. Los datos de registro se enviarán al servidor de origen y a todas las direcciones URL que aparecen en cada elemento **LOGURL** en el ámbito. Los datos de registro se enviarán una sola vez a cada dirección URL indicada, incluso si la misma dirección URL aparece más de una vez en un ámbito determinado. Una repetición de una **entrada** produciría otro envío a las direcciones URL enumeradas.

No hay ningún límite en el número de elementos **LOGURL** de una lista de reproducción de metarchivo.

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
| Versión<br/> | Windows Media Player versión 70 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referencia de metarchivos de Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





