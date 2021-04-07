---
title: UI_PKEY_Label
description: Identifica la \_ propiedad de etiqueta PKEY de la interfaz de usuario \_ .
ms.assetid: 4d704133-bba7-4c32-a552-d748b66455eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245ce8d239e1a0893c907a047aa9a48996cbf606
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903610"
---
# <a name="ui_pkey_label"></a>\_Etiqueta PKEY de IU \_

Identifica la \_ propiedad de etiqueta PKEY de la interfaz de usuario \_ .

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

\_ \_ La etiqueta PKEY de la interfaz de usuario se usa en una aplicación para consultar el texto de la etiqueta de pestañas, grupos, botones, elementos de la galería y otros controles de la cinta de opciones.

> [!Note]  
> Windows 8 y versiones más recientes: imagen del botón de menú de la [aplicación](windowsribbon-controls-applicationmenu.md) cambiada a etiqueta: **archivo**. Se recomienda no usar archivo como etiqueta para ninguna de sus propias pestañas.

 

El valor de propiedad es una cadena restringida a cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.

> [!Note]  
> Use la referencia de caracteres XML del juego de caracteres universal (UCS) `&#xA;` para especificar un salto de línea.

 

No se admite la alineación derecha.

La longitud máxima de la etiqueta PKEY de la interfaz de usuario \_ \_ no está enlazada.

Si un comando se expone a través de un elemento de menú y el valor de la etiqueta [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) o UI \_ PKEY \_ contiene una letra precedida por un símbolo de y comercial, como se muestra en el ejemplo siguiente, esta letra se trata como un KeyTip y una tecla de aceleración para ese comando por el marco de la cinta de opciones.


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



Para mostrar una y comercial en una etiqueta, escape la designación de carácter especial con un signo de y comercial ( `&&` ), tal y como se muestra en el ejemplo siguiente.


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de recursos](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Comando. LabelTitle**](windowsribbon-element-command-labeltitle.md)
</dt> <dt>

[UI \_ PKEY \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 




