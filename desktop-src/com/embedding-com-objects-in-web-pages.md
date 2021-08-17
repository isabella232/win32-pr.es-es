---
title: Insertar objetos COM en páginas web
description: Puede usar objetos COM en páginas web. Para ello, cree primero una instancia de ese objeto COM. Después de crear una instancia de objeto, puede usarla en scripts posteriores en esa página web.
ms.assetid: 7e2c9da7-aeae-4206-8be9-1303240b2b1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d13a92bd2de152e71ac4284ce37b977e8305f25dcb2aef5eb94d6019d115812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736896"
---
# <a name="embedding-com-objects-in-web-pages"></a>Insertar objetos COM en páginas web

Puede usar objetos COM en páginas web. Para ello, cree primero una instancia de ese objeto COM. Después de crear una instancia de objeto, puede usarla en scripts posteriores en esa página web.

Para crear una instancia de objeto COM en una página web, puede usar una etiqueta OBJECT. Como alternativa, si el lenguaje de scripting proporciona una manera nativa de crear objetos COM, puede crear una instancia de objeto mediante script.

Tenga en cuenta que la inserción de objetos COM en páginas web solo funciona con exploradores que admiten ActiveX y COM, por ejemplo, Internet Explorer.

En el ejemplo siguiente se muestra cómo usar la etiqueta OBJECT para insertar un objeto COM en una página web:

``` syntax
<OBJECT 
  ID = vid 
  CLASSID = "clsid:31263EC0-2957-11CF-A1E5-00AA9EC79700" 
  BORDER = 0 
  VSPACE = 0 
  HSPACE = 0 
  ALIGN = TOP 
  HEIGHT = 100% 
  WIDTH = 100%
>
</OBJECT>
 
```

También puede crear una instancia de objeto COM en el script, si el lenguaje de scripting proporciona una manera de crear objetos COM. Por ejemplo, VBScript proporciona el método CreateObject y JScript proporciona el objeto ActiveXObject. La creación de objetos en el script se muestra en los ejemplos siguientes.

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Dim objXL
  Set objXL = CreateObject("Excel.Application")
</SCRIPT>
 
<SCRIPT LANGUAGE = "JScript">
  var objXL = new ActiveXObject("Excel.Application");
</SCRIPT>
 
```

Además del método CreateObject y el objeto ActiveXObject, tanto VBScript como JScript proporcionan el método GetObject, que devuelve una instancia de objeto.

Una vez creado un objeto COM, puede hacer referencia a él en scripts posteriores mediante el identificador especificado en el atributo ID de la etiqueta OBJECT. En el ejemplo anterior, este identificador se especificó como "vid". Tenga en cuenta que el script que usa el objeto COM debe aparecer después de la etiqueta OBJECT o el script que crea la instancia del objeto; De lo contrario, el identificador de objeto no está definido. El script siguiente usa el objeto objXL para mostrar la información de versión de Microsoft Excel.

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Msgbox objXL.Version
</SCRIPT>
 
```

Si va a escribir scripts insertados en una página web, el explorador también expone un modelo de objetos al que pueden acceder los scripts. El modelo utilizado por Internet Explorer se ajusta al Document Object Model (DOM) propuesto por el World Wide Web Consortium (W3C).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Scripting con objetos COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




