---
title: UI_PKEY_Label
description: Identifica la propiedad ui \_ PKEY \_ Label.
ms.assetid: 4d704133-bba7-4c32-a552-d748b66455eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13506d1609f915c2eab9824a3f5256383c5f2aecf73ed5787e3372f17b44b435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706436"
---
# <a name="ui_pkey_label"></a>Etiqueta \_ PKEY de la interfaz de \_ usuario

Identifica la propiedad ui \_ PKEY \_ Label.

```
propertyDescription
   name = UI_PKEY_Label
   shellPKey = UI_PKEY_Label
   formatID = 00000004-7363-696e-8441798acf5aebb7
   propID = 4
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Observaciones

Una aplicación usa ui PKEY Label para consultar el texto de etiqueta de \_ pestañas, grupos, botones, elementos de la galería y otros controles \_ de la cinta de opciones.

> [!Note]  
> Windows 8 y versiones más recientes: la [imagen del botón Menú](windowsribbon-controls-applicationmenu.md) de la aplicación ha cambiado a la etiqueta: **Archivo**. Se recomienda no usar Archivo como etiqueta para ninguna de sus propias pestañas.

 

El valor de propiedad es una cadena restringida a cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.

> [!Note]  
> Use la referencia de caracteres XML de juego de caracteres universales (UCS) `&#xA;` para especificar un salto de línea.

 

No se admite la alineación derecha.

La longitud máxima de la etiqueta PKEY de la interfaz de \_ usuario está sin \_ enlazar.

Si un comando se expone a través de un elemento de menú y el valor de [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) o ui PKEY Label contiene una letra precedida de una y comercial, como se muestra en el ejemplo siguiente, esta letra se trata como una tecla y un acelerador de teclado para ese comando mediante el marco de la cinta \_ \_ de opciones.


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



Para mostrar una y comercial en una etiqueta, escape la designación de caracteres especiales con una y comercial doble ( ) como se muestra `&&` en el ejemplo siguiente.


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del recurso](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md)
</dt> <dt>

[UI \_ PKEY \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 




