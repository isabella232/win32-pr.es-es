---
title: Especificar recursos de imagen de cinta de opciones
description: Como sistema de presentación de comandos enriquecido, el marco Windows Ribbon está diseñado para admitir ampliamente los recursos de imagen en toda la interfaz de usuario (UI) de la cinta de opciones. Todos los recursos de imagen se declaran en el marcado de la cinta de opciones o se consultan desde una aplicación host de la cinta de opciones.
ms.assetid: 37b57992-8da8-4e6b-869d-72a136f6ad77
keywords:
- Windows Cinta de opciones, recursos de imagen
- Cinta de opciones, recursos de imagen
- Windows Cinta de opciones, transparencia
- Cinta de opciones, transparencia
- Windows Cinta, profundidad de color
- Cinta, profundidad de color
- Windows Cinta de opciones, contraste
- Cinta de opciones, contraste
- recursos de imagen en Windows cinta de opciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c485de9c0d9d1b51b09d4a2b9dba95dd30a778922750a7f388c7a5c8963cda6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932600"
---
# <a name="specifying-ribbon-image-resources"></a>Especificar recursos de imagen de cinta de opciones

Como sistema de presentación de comandos enriquecido, el marco Windows Ribbon está diseñado para admitir ampliamente los recursos de imagen en toda la interfaz de usuario (UI) de la cinta de opciones. Todos los recursos de imagen se declaran en el [marcado de la](windowsribbon-schema.md) cinta de opciones o se consultan desde una aplicación host de la cinta de opciones.

Para Windows 8 y versiones posteriores, el marco de la cinta de opciones admite los siguientes formatos gráficos: archivos de mapa de bits ARGB (BMP) de 32 bits y archivos de gráficos de red portátiles (PNG) con transparencia.

Para Windows 7 y versiones anteriores, los recursos de imagen deben ajustarse al formato de gráfico BMP estándar que se usa en Windows.

> [!Note]  
> Puede producirse un error de compilación si se proporciona un formato de imagen no compatible al marco.

 

## <a name="image-sizes"></a>Tamaños de imagen

Para proporcionar mayor flexibilidad a los diseños de control de la cinta de opciones al cambiar el tamaño de una ventana de aplicación, el marco de la cinta de opciones acepta y representa imágenes en uno de estos dos tamaños: grande o pequeño.

Las imágenes siguientes ilustran una aplicación de cinta de opciones que admite varios tamaños de cinta a través de diseños de control flexibles y el reemplazo de imágenes grandes por imágenes pequeñas cuando estén disponibles.

En la siguiente captura de pantalla se muestra la cinta de opciones con imágenes grandes para los controles zoom.

![captura de pantalla que muestra una cinta de opciones que usa imágenes grandes para los controles de zoom.](images/overviews/imageresources-largeimage.png)

En la siguiente captura de pantalla se muestra el mismo tamaño de cinta con imágenes pequeñas para los controles de zoom.

![captura de pantalla que muestra una cinta de opciones que usa imágenes pequeñas para los controles de zoom.](images/overviews/imageresources-smallimage.png)

En la siguiente captura de pantalla se muestra la cinta en estado oculto. La cinta de opciones está oculta cuando se han agotado todos los diseños de control potenciales y la cinta de opciones no se puede representar con un área de trabajo de aplicación utilizable.

![captura de pantalla que muestra una cinta de opciones contraigada.](images/overviews/imageresources-noimage.png)

Para cualquier imagen, el tamaño exacto de los píxeles depende de la resolución de la pantalla, o de los puntos por pulgada (ppp) del monitor que se usa. A 96 ppp, las imágenes grandes tienen un tamaño de 32 x 32 píxeles y las imágenes pequeñas tienen un tamaño de 16 x 16 píxeles. Los tamaños de imagen aumentan de forma lineal en relación con ppp, como se muestra en la tabla siguiente.



| ppp     | Imagen pequeña  | Imagen grande  |
|---------|--------------|--------------|
| 96 ppp  | 16 x 16 píxeles | 32 x 32 píxeles |
| 120 ppp | 20 x 20 píxeles | 40 x 40 píxeles |
| 144 ppp | 24 x 24 píxeles | 48 x 48 píxeles |
| 192 ppp | 32 x 32 píxeles | 64 x 64 píxeles |



 

El marco de la cinta escala los recursos de imagen según sea necesario. Sin embargo, dado que el cambio de tamaño puede producir artefactos no deseados y degradación de la imagen, se recomienda encarecidamente que la aplicación proporcione un pequeño conjunto de recursos de imagen que abarquen varias configuraciones de ppp de uso frecuente. Si no se encuentra una coincidencia exacta, la imagen más cercana se escalará o reducirá verticalmente.

Para facilitar esto, los recursos de imagen se pueden declarar en el marcado de la cinta de opciones mediante un conjunto de elementos [**Image**](windowsribbon-element-image.md) para cada [**elemento**](windowsribbon-element-command.md) Command. En tiempo de ejecución, el marco selecciona la imagen que se mostrará en función del *atributo MinDPI* de cada **elemento Image.**

> [!IMPORTANT]
>
> Cuando se proporciona una colección de recursos de imagen diseñados para admitir la configuración de ppp  de pantalla específica al marco de la cinta de opciones a través de un conjunto de elementos [**Image,**](windowsribbon-element-image.md) el marco usa la imagen con un valor de atributo *MinDPI* que coincide con la configuración de ppp de la pantalla actual.
>
> Si no se declara ningún elemento [**Image**](windowsribbon-element-image.md) con un valor *MinDPI* que  coincida con la configuración de ppp de la pantalla actual, el marco elige la imagen que tiene el valor *MinDPI* más próximo menos que el valor de ppp de la pantalla actual y escala verticalmente el recurso de imagen. De lo contrario, si no se declara ningún elemento **Image** con un valor de atributo *MinDPI* menor que el valor de ppp de la pantalla actual, el marco elige el valor *MinDPI* más cercano mayor que el valor de ppp de pantalla actual y escala el recurso de imagen hacia abajo.

 

En el ejemplo siguiente se muestra cómo declarar un conjunto de imágenes para adaptarse a los distintos tamaños de cinta y la configuración del sistema.


```C++
<Command.LargeImages>
  <Image Source="res/CutLargeImage32.bmp" Id="116" Symbol="ID_CUT_LARGEIMAGE1" MinDPI="96" />
  <Image Source="res/CutLargeImage40.bmp" Id="117" Symbol="ID_CUT_LARGEIMAGE2" MinDPI="120" />
  <Image Source="res/CutLargeImage48.bmp" Id="118" Symbol="ID_CUT_LARGEIMAGE3" MinDPI="144" />
  <Image Source="res/CutLargeImage64.bmp" Id="119" Symbol="ID_CUT_LARGEIMAGE4" MinDPI="192" />
</Command.LargeImages>
<Command.SmallImages>
  <Image Source="res/CutSmallImage16.bmp" Id="122" Symbol="ID_CUT_SMALLIMAGE1" MinDPI="96" />
  <Image Source="res/CutSmallImage20.bmp" Id="123" Symbol="ID_CUT_SMALLIMAGE2" MinDPI="120" />
  <Image Source="res/CutSmallImage24.bmp" Id="124" Symbol="ID_CUT_SMALLIMAGE3" MinDPI="144" />
  <Image Source="res/CutSmallImage32.bmp" Id="125" Symbol="ID_CUT_SMALLIMAGE4" MinDPI="192" />
</Command.SmallImages>
<Command.LargeHighContrastImages>
  <Image Source="res/CutLargeImage32HC.bmp" Id="130" Symbol="ID_CUT_LARGEIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutLargeImage40HC.bmp" Id="131" Symbol="ID_CUT_LARGEIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutLargeImage48HC.bmp" Id="132" Symbol="ID_CUT_LARGEIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutLargeImage64HC.bmp" Id="133" Symbol="ID_CUT_LARGEIMAGE4HC" MinDPI="192" />
</Command.LargeHighContrastImages>
<Command.SmallHighContrastImages>
  <Image Source="res/CutSmallImage16HC.bmp" Id="135" Symbol="ID_CUT_SMALLIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutSmallImage20HC.bmp" Id="136" Symbol="ID_CUT_SMALLIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutSmallImage24HC.bmp" Id="137" Symbol="ID_CUT_SMALLIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutSmallImage32HC.bmp" Id="138" Symbol="ID_CUT_SMALLIMAGE4HC" MinDPI="192" />
</Command.SmallHighContrastImages>
```



Si las imágenes declaradas en marcado se invalidan en tiempo de ejecución por cualquier motivo, se consulta la aplicación host para obtener nuevas imágenes. Cuando estas imágenes se generan y se cargan mediante programación, la aplicación debe intentar devolver imágenes con tamaño según los tamaños predeterminados de los iconos del sistema determinados por la métrica del sistema [SM \_ CXICON](/windows/win32/api/winuser/nf-winuser-getsystemmetrics).

> [!Note]  
> Las imágenes grandes tienen un tamaño de SM CXICON de SM CXICON y las imágenes pequeñas tienen un tamaño de \_ \_ SM \_ CXICON/2 por SM \_ CXICON/2.

 

## <a name="color-depth-transparency-and-contrast"></a>Profundidad de color, transparencia y contraste

Se espera que las imágenes normales estén en formato argb de 32 bits por píxel (BPP) y que se escalan al tamaño predeterminado del icono del sistema. Este formato admite transparencia y suavizado de contorno (con 8 bits por canal).

> [!WARNING]
> Muchas herramientas de edición de imágenes no conservan el canal alfa de 8 bits de orden más alto al cargar o guardar 32 imágenes BPP.

 

Para que una imagen se muestre correctamente en modo de contraste alto, debe tener un formato de píxel de paleta de 4 BPP. Cuando se representa la imagen, el marco de la cinta de opciones reasigna colores específicos en función del contexto de contraste alto de la imagen.

En la tabla siguiente se muestra el comportamiento de representación de color de contraste alto del marco.



Color de píxel

Valor RGB

Comportamiento

Fondo blanco

Fondo oscuro

Magenta

800080

Transparente

Transparente

Negro

000000

COLOR \_ WINDOWTEXT

Blanco

Blanco

FFFFFF

VENTANA DE \_ COLOR

Negro

GRIS OSCURO

808080

COLOR \_ 3DSHADOW

COLOR \_ 3DSHADOW

Gris

C0C0C0

COLOR \_ 3DFACE

COLOR \_ 3DFACE

GRIS CLARO

DFDFDF

COLOR \_ 3DLIGHT

COLOR \_ 3DLIGHT

AZUL OSCURO

000080

N/D

Blanco



 

Para obtener más información sobre los formatos de imagen admitidos por el marco de la cinta de opciones, vea lo siguiente:

-   [Estructura BITMAPINFOHEADER:](/previous-versions//dd183376(v=vs.85)) describe el formato de píxel argb de 32 BPP.
-   [Función CreateDIBSection:](/windows/win32/api/wingdi/nf-wingdi-createdibsection) describe cómo crear una imagen de formato de píxel ARGB de 32 BPP.
-   [Función LoadImage:](/windows/win32/api/winuser/nf-winuser-loadimagea) describe cómo cargar una imagen de formato argb de 32 BPP.

## <a name="accessibility"></a>Accesibilidad

Confiar en recursos de imagen para proporcionar información, transmitir la funcionalidad de control y exponer el estado de la aplicación aumenta la necesidad de requisitos de accesibilidad durante el diseño y el desarrollo de aplicaciones.

Para obtener compatibilidad básica con contraste alto, la cinta de opciones permite que se muestre un conjunto independiente de archivos de imagen cuando un tema de contraste alto está activo. Estas imágenes pueden ser 32 BPP o 4 BPP, con colores asignados a una paleta especial donde los colores oscuros y claros se invierten en función de los colores de primer plano y de fondo del tema activo de contraste alto.

En el ejemplo siguiente se muestra cómo se declaran los recursos de imagen de contraste alto en el marcado de la cinta de opciones:


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px.bmp" MinDPI="192" />
      </Command.LargeImages>
      <Command.LargeHighContrastImages>
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px-HC.bmp" MinDPI="192" />
      </Command.LargeHighContrastImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px.bmp" MinDPI="192" />
      </Command.SmallImages>
      <Command.SmallHighContrastImages>
        <Image Source="cmdNew-16px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="192" />
      </Command.SmallHighContrastImages>
    </Command>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Command.SmallImages**](windowsribbon-element-command-smallimages.md)
</dt> <dt>

[UI \_ PKEY \_ SmallImage](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> <dt>

[**Command.LargeImages**](windowsribbon-element-command-largeimages.md)
</dt> <dt>

[UI \_ PKEY \_ LargeImage](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> <dt>

[**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)
</dt> <dt>

[UI \_ PKEY \_ SmallHighContrastImage](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> <dt>

[**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)
</dt> <dt>

[UI \_ PKEY \_ LargeHighContrastImage](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 