---
title: Uso de objetos COM en Active Server Pages
description: Puede crear scripts de objetos COM en Active Server pages (ASP).
ms.assetid: 3a074360-8b6c-4cb6-813b-73863fe11c46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5d73244ce5bd6c56deeda9bf4e3e4986b3d4039
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568501"
---
# <a name="using-com-objects-in-active-server-pages"></a>Uso de objetos COM en Active Server Pages

Puede crear scripts de objetos COM en Active Server pages (ASP). Para ello, primero debe crear una instancia del objeto mediante la etiqueta OBJECT o llamando al método CreateObject del objeto de servidor ASP. Una vez creado un objeto COM, puede usarlo en scripts posteriores en la página ASP.

Con ASP, puede trabajar con muchos tipos diferentes de motores de scripting, cada uno de los cuales admite un lenguaje de scripting diferente. ASP incluye VBScript y JScript de scripting. También puede conectar motores de scripting desarrollados por otras empresas para admitir lenguajes como PerlScript, PScript, Python y otros.

Si no establece el lenguaje de scripting para una página ASP, VBScript es el valor predeterminado. Para especificar un lenguaje de scripting distinto de VBScript, incluya una línea como la siguiente en la parte superior de cada página ASP:

``` syntax
<%@ LANGUAGE=JScript %>
 
```

Para usar un objeto COM en una página ASP, primero debe crear una instancia de ese objeto. Para ello, use la etiqueta OBJECT y especifique el valor "SERVER" para el atributo RUNAT, como se muestra en el ejemplo siguiente. De forma predeterminada, la etiqueta OBJECT crea una instancia del objeto en el cliente. Establecer el atributo RUNAT en SERVER hace que el objeto se cree en el servidor. El objeto debe ejecutarse en el servidor para que ASP lo utilice.

``` syntax
<OBJECT 
RUNAT=SERVER 
ID=MyAds 
CLASSID="Clsid:1621F7C0-60AC-11CF-9427-444553540000">
</OBJECT> 
 
```

También puede crear una instancia de un objeto COM en una página ASP llamando al método CreateObject del objeto servidor ASP. El uso de Server.CreateObject es más lento que crear el objeto mediante una etiqueta OBJECT, pero es ligeramente más legible porque especifica el identificador de programación en lugar del identificador de clase del objeto COM. ASP expone el objeto Server y no es necesario crearlo. En los ejemplos siguientes se muestra cómo llamar a Server.CreateObject. El primer ejemplo es VBScript:

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

Llamar a CreateObject es más lento que usar la etiqueta OBJECT para crear un objeto COM. En aplicaciones en las que el rendimiento es crítico, debe usar la etiqueta OBJECT.

Después de crear una instancia del objeto COM, puede usarla en scripts. Esto se ilustra en el ejemplo de VBScript siguiente, que establece el valor de la propiedad Border del objeto COM.

``` syntax
<% MyAds.Border = 0 %>
 
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Scripting con objetos COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




