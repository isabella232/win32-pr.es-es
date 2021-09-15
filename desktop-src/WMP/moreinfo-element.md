---
title: Elemento MOREINFO
description: El elemento MOREINFO especifica una dirección URL a un sitio web, una dirección de correo electrónico o un comando de script asociado a un mensaje de presentación, clip o banner.
ms.assetid: b817ef1d-4ca0-45f4-942b-695eaf537110
keywords:
- Elemento MOREINFO Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359282"
---
# <a name="moreinfo-element"></a>Elemento MOREINFO

El **elemento MOREINFO** especifica una dirección URL a un sitio web, una dirección de correo electrónico o un comando de script asociado a un mensaje de presentación, clip o banner.

``` syntax
<MOREINFO
   HREF = "URL"
   TARGET = "Frame"
/>
```

## <a name="attributes"></a>Atributos

**HREF** (obligatorio)

Dirección URL a un sitio web, dirección de correo electrónico o comando de script.

**OBJETIVO**

Valor que define el marco o la ventana en la que el explorador abrirá la página definida por el **atributo HREF.**

Puede ser una cadena que contiene un nombre de ventana o uno de los siguientes valores.



| Value    | Descripción                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| \_Blanco  | El documento se carga en una nueva ventana del explorador.                                                                              |
| \_self   | El documento se carga en el mismo marco que el documento actual que contiene Reproductor de Windows Media control.                |
| \_Padre | El documento se carga en el marco primario inmediato del marco actual o en el marco actual si no hay ningún marco primario. |
| \_top    | El documento se carga en la ventana completa del explorador, reemplazando todos los demás marcos o documentos.                                  |



 

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos                       |
|-----------------|--------------------------------|
| Elementos primarios | **ASX**, **ENTRY**, **BANNER** |
| Elementos secundarios  | Ninguno                           |



 

## <a name="remarks"></a>Observaciones

Este elemento especifica una dirección URL a un sitio web, una dirección de correo electrónico **o un comando de script. El usuario puede acceder al destino de la dirección URL haciendo clic en el gráfico o texto asociado al elemento MOREINFO.** Los detalles dependen del elemento primario del **elemento MOREINFO:**

-   Si el **elemento MOREINFO** es el elemento secundario de un **elemento ASX,** el usuario puede acceder a la dirección URL haciendo clic en el título para mostrar.
-   Si el **elemento MOREINFO** es el elemento secundario de un **elemento ENTRY,** el usuario puede acceder a la dirección URL haciendo clic en el título del clip.
-   Si el **elemento MOREINFO** es el elemento secundario de un **elemento BANNER,** el usuario puede acceder a la dirección URL haciendo clic en el gráfico del banner.

Si el **atributo HREF** especifica una dirección URL a un sitio web, el explorador se abre y navega a la dirección URL. Si el **atributo HREF** especifica una dirección de correo electrónico, se inicia la aplicación de correo electrónico del usuario. Si el **atributo HREF** especifica un comando de script, el comando de script se ejecuta en el explorador.

**Nota**

Si el **elemento MOREINFO** aparece dentro de un elemento **ASX** o **ENTRY,** cuando el cursor del mouse se mantiene sobre el título de la presentación (para un elemento **ASX)** o clip (para un elemento **ENTRY),** la dirección URL definida en el **atributo HREF** se puede seleccionar y acceder mediante Reproductor de Windows Media.

El **atributo TARGET** define el marco o la ventana en la que el explorador abrirá la página definida por el atributo **HREF.** Los valores de este atributo siguen las definiciones y la sintaxis HTML estándar. En el caso de un control insertado en una página web, si no se define ningún atributo **TARGET,** la dirección URL carga la ventana del explorador actual y reemplaza la página existente, lo que significa que el contenido deja de reproducirse. Por lo tanto, se recomienda especificar siempre un atributo **TARGET** al insertar el control Reproductor de Windows Media en una página web.

Si el metarchivo se abre en el archivo Reproductor de Windows Media independiente, se omite el atributo **TARGET** y la dirección URL se carga en una ventana del explorador existente. Si no hay ninguna ventana del explorador abierta actualmente, la dirección URL se carga en una nueva ventana del explorador.

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
| Versión<br/> | Reproductor de Windows Media versión 70 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referencia de metarchivo multimedia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





