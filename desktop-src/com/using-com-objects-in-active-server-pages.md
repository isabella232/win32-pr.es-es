---
title: Usar objetos COM en páginas Active Server
description: Puede crear scripts de objetos COM en aplicaciones de Active Server páginas (ASP).
ms.assetid: 3a074360-8b6c-4cb6-813b-73863fe11c46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5d73244ce5bd6c56deeda9bf4e3e4986b3d4039
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356762"
---
# <a name="using-com-objects-in-active-server-pages"></a>Usar objetos COM en páginas Active Server

Puede crear scripts de objetos COM en aplicaciones de Active Server páginas (ASP). Para ello, primero debe crear una instancia del objeto utilizando la etiqueta de objeto o llamando al método CreateObject del objeto de servidor ASP. Una vez creado un objeto COM, puede usarlo en scripts posteriores en la página ASP.

Con ASP, puede trabajar con muchos tipos diferentes de motores de scripts, cada uno de los cuales admite un lenguaje de scripting diferente. ASP incluye los motores de scripting de VBScript y JScript. También puede conectar motores de scripting desarrollados por otras compañías para admitir lenguajes como PerlScript, PScript, Python y otros.

Si no establece el lenguaje de scripting para una página ASP, VBScript es el valor predeterminado. Para especificar un lenguaje de scripting distinto de VBScript, incluya una línea como la siguiente en la parte superior de cada página ASP:

``` syntax
<%@ LANGUAGE=JScript %>
 
```

Para usar un objeto COM en una página ASP, primero debe crear una instancia de ese objeto. Para ello, use la etiqueta OBJECT y especifique el valor "SERVER" para el atributo runas, tal y como se muestra en el ejemplo siguiente. De forma predeterminada, la etiqueta de objeto crea una instancia del objeto en el cliente. Al establecer el atributo RUNAt en SERVER, se crea el objeto en el servidor. El objeto se debe ejecutar en el servidor para que lo use ASP.

``` syntax
<OBJECT 
RUNAT=SERVER 
ID=MyAds 
CLASSID="Clsid:1621F7C0-60AC-11CF-9427-444553540000">
</OBJECT> 
 
```

También puede crear una instancia de un objeto COM en una página ASP llamando al método CreateObject del objeto de servidor ASP. El uso de Server. CreateObject es más lento que la creación del objeto mediante una etiqueta de objeto, pero es ligeramente más legible porque especifica el identificador de programación en lugar del identificador de clase del objeto COM. El objeto de servidor se expone mediante ASP y no es necesario crearlo. Cómo llamar a Server. CreateObject se ilustra en los ejemplos siguientes. El primer ejemplo es VBScript:

``` syntax
<% 
  Set MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

El ejemplo siguiente es JScript:

``` syntax
<% 
  var MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

Llamar a CreateObject es más lento que usar la etiqueta de objeto para crear un objeto COM. En aplicaciones en las que el rendimiento es crítico, debe usar la etiqueta de objeto.

Después de crear una instancia del objeto COM, puede usarla en scripts. Esto se ilustra en el ejemplo de VBScript siguiente, que establece el valor de la propiedad border del objeto COM.

``` syntax
<% MyAds.Border = 0 %>
 
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Scripting con objetos COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




