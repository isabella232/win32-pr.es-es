---
title: Elemento MOREINFO
description: El elemento MOREINFO especifica una dirección URL a un sitio web, una dirección de correo electrónico o un comando de script asociado a un programa, un clip o un banner.
ms.assetid: b817ef1d-4ca0-45f4-942b-695eaf537110
keywords:
- Elemento MOREINFO Media Player Windows
topic_type:
- apiref
api_name:
- MOREINFO Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efc54fe9745566ec7eaa87b7f0f4645b07a055f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708261"
---
# <a name="moreinfo-element"></a>Elemento MOREINFO

El elemento **MOREINFO** especifica una dirección URL a un sitio web, una dirección de correo electrónico o un comando de script asociado a un programa, un clip o un banner.

``` syntax
<MOREINFO
   HREF = "URL"
   TARGET = "Frame"
/>
```

## <a name="attributes"></a>Atributos

**Href** (obligatorio)

Dirección URL de un sitio web, una dirección de correo electrónico o un comando de script.

**DIRIGIR**

Valor que define el marco o la ventana en la que el explorador abrirá la página definida por el atributo **href** .

Puede ser una cadena que contenga un nombre de ventana o uno de los valores siguientes.



| Value    | Descripción                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| \_en blanco  | El documento se carga en una nueva ventana del explorador.                                                                              |
| \_self   | El documento se carga en el mismo marco que el documento actual que contiene el control Media Player de Windows.                |
| \_aérea | El documento se carga en el marco primario inmediato del fotograma actual o en el fotograma actual si no hay ningún marco primario. |
| \_Arriba    | El documento se carga en la ventana completa del explorador, reemplazando todos los demás marcos o documentos.                                  |



 

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos                       |
|-----------------|--------------------------------|
| Elementos primarios | **ASX**, **entrada**, **banner** |
| Elementos secundarios  | Ninguno                           |



 

## <a name="remarks"></a>Observaciones

Este elemento especifica una dirección URL a un sitio web, una dirección de correo electrónico **o un comando de script. El usuario puede tener acceso al destino de la dirección URL haciendo clic en el gráfico o en el texto asociado con el elemento MOREINFO** . Los detalles dependen del elemento primario del elemento **MOREINFO** :

-   Si el elemento **MOREINFO** es el elemento secundario de un elemento **ASX** , el usuario puede tener acceso a la dirección URL haciendo clic en el título Mostrar.
-   Si el elemento **MOREINFO** es el elemento secundario de un elemento **entry** , el usuario puede tener acceso a la dirección URL haciendo clic en el título del clip.
-   Si el elemento **MOREINFO** es el elemento secundario de un elemento **banner** , el usuario puede tener acceso a la dirección URL haciendo clic en el gráfico de encabezado.

Si el atributo **href** especifica una dirección URL a un sitio web, el explorador se abrirá y navegará a la dirección URL. Si el atributo **href** especifica una dirección de correo electrónico, se inicia la aplicación de correo electrónico del usuario. Si el atributo **href** especifica un comando de script, el comando de script se ejecuta en el explorador.

**Note**

Si el elemento **MOREINFO** aparece dentro de un elemento **ASX** o **entry** , cuando el cursor del mouse se mantiene sobre el título de la presentación (para un elemento **ASX** ) o un recorte (para un elemento de **entrada** ), Windows Media Player puede seleccionar la dirección URL definida en el atributo **href** y obtener acceso a ella.

El atributo de **destino** define el marco o la ventana en la que el explorador abrirá la página definida por el atributo **href** . Los valores de este atributo siguen la sintaxis y las definiciones HTML estándar. En el caso de un control incrustado en una página web, si no se define ningún atributo de **destino** , la dirección URL carga la ventana del explorador actual y reemplaza la página existente, lo que significa que el contenido deja de reproducirse. Por lo tanto, se recomienda especificar siempre un atributo de **destino** al insertar el control Media Player de Windows en una página web.

Si el metarchivo está abierto en el Media Player de Windows independiente, se omite el atributo de **destino** y la dirección URL se carga en una ventana del explorador existente. Si no hay ninguna ventana del explorador abierta actualmente, la dirección URL se carga en una nueva ventana del explorador.

## <a name="examples"></a>Ejemplos


```XML
<ASX VERSION="3.0">

   <TITLE>Example Media Player Show</TITLE>
   <MOREINFO HREF="https://example.microsoft.com/info/show_info.htm" />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <MOREINFO HREF="https://example.microsoft.com/info/clip1_info.htm" />
      <REF HREF="mms://example.microsoft.com/media.asf" />
   </ENTRY>
   
</ASX>

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

 

 





