---
title: Especificar recursos de imagen de cinta
description: Como sistema de presentación de comandos enriquecido, el marco de la cinta de opciones de Windows está diseñado para admitir los recursos de imagen en gran medida a través de la interfaz de usuario (UI) de la cinta. Todos los recursos de imagen se declaran en el marcado de la cinta o se consultan desde una aplicación host de cinta.
ms.assetid: 37b57992-8da8-4e6b-869d-72a136f6ad77
keywords:
- Cinta de Windows, recursos de imagen
- Cinta, recursos de imagen
- Cinta de Windows, transparencia
- Cinta de opciones, transparencia
- Cinta de Windows, profundidad de color
- Cinta, profundidad de color
- Cinta de opciones de Windows, contraste
- Cinta, contraste
- recursos de imagen en la cinta de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e7666126e5b8f7fbe8b610678a8a1d71589373
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488123"
---
# <a name="specifying-ribbon-image-resources"></a>Especificar recursos de imagen de cinta

Como sistema de presentación de comandos enriquecido, el marco de la cinta de opciones de Windows está diseñado para admitir los recursos de imagen en gran medida a través de la interfaz de usuario (UI) de la cinta. Todos los recursos de imagen se declaran en el [marcado de la cinta](windowsribbon-schema.md) o se consultan desde una aplicación host de cinta.

En Windows 8 y versiones posteriores, el marco de la cinta de opciones admite los siguientes formatos de gráficos: archivos de mapa de bits ARGB de 32 bits (BMP) y archivos PNG (Portable Network Graphics) con transparencia.

En Windows 7 y versiones anteriores, los recursos de imagen deben ajustarse al formato de gráficos BMP estándar usado en Windows.

> [!Note]  
> Puede producirse un error de compilación si se proporciona un formato de imagen no compatible al marco.

 

## <a name="image-sizes"></a>Tamaños de imagen

Para proporcionar mayor flexibilidad a los diseños de controles de la cinta al cambiar el tamaño de una ventana de la aplicación, el marco de cinta acepta y representa imágenes en uno de dos tamaños: grande o pequeño.

Las siguientes imágenes ilustran una aplicación de cinta que admite varios tamaños de cinta a través de diseños de control flexibles y la sustitución de imágenes grandes con imágenes pequeñas cuando están disponibles.

En la captura de pantalla siguiente se muestra la cinta de opciones con imágenes grandes para los controles de zoom.

![captura de pantalla que muestra una cinta que usa imágenes grandes para los controles de zoom.](images/overviews/imageresources-largeimage.png)

En la captura de pantalla siguiente se muestra la misma cinta cuyo tamaño se ha cambiado con imágenes pequeñas para los controles de zoom

![captura de pantalla que muestra una cinta que usa imágenes pequeñas para los controles de zoom.](images/overviews/imageresources-smallimage.png)

En la captura de pantalla siguiente se muestra la cinta de opciones en estado oculto. La cinta de opciones se oculta cuando se han agotado todos los diseños de control potenciales y la cinta de opciones no se puede representar con un área de trabajo de aplicación utilizable.

![captura de pantalla que muestra una cinta contraída.](images/overviews/imageresources-noimage.png)

En cualquier imagen, el tamaño exacto en píxeles depende de la resolución de la pantalla, o de puntos por pulgada (PPP), del monitor que se está usando. En 96 PPP, las imágenes grandes tienen un tamaño de 32 x 32 píxeles y las imágenes pequeñas son de 16 x 16 píxeles. Los tamaños de imagen aumentan de manera lineal en relación con los PPP, como se muestra en la tabla siguiente.



| ppp     | Imagen pequeña  | Imagen grande  |
|---------|--------------|--------------|
| 96 PPP  | 16x16 píxeles | 32x32 píxeles |
| 120 ppp | 20x20 píxeles | 40 x 40 píxeles |
| 144 ppp | 24x24 píxeles | 48x48 píxeles |
| 192 PPP | 32x32 píxeles | 64 x 64 píxeles |



 

El marco de cinta escala los recursos de imagen según sea necesario. Sin embargo, dado que el cambio de tamaño puede producir artefactos no deseados y degradación de la imagen, se recomienda encarecidamente que la aplicación proporcione un pequeño conjunto de recursos de imagen que abarquen varios valores de PPP usados con frecuencia. Si no se encuentra una coincidencia exacta, la imagen más cercana se escalará o reducirá verticalmente.

Para facilitar esto, los recursos de imagen se pueden declarar en el marcado de la cinta de opciones mediante un conjunto de elementos [**Image**](windowsribbon-element-image.md) para cada elemento [**Command**](windowsribbon-element-command.md) . En tiempo de ejecución, el marco de trabajo selecciona la imagen que se va a mostrar basándose en el atributo *MinDPI* de cada elemento de **imagen** .

> [!IMPORTANT]
>
> Cuando se proporciona una colección de recursos de imagen que están diseñados para admitir valores de PPP de pantalla específicos para el marco de cinta a través de un conjunto de elementos de [**imagen**](windowsribbon-element-image.md) , el marco de trabajo usa la **imagen** con un valor de atributo *MinDPI* que coincide con la configuración de PPP de pantalla actual.
>
> Si no se declara ningún elemento de [**imagen**](windowsribbon-element-image.md) con un valor de *MinDPI* que coincida con la configuración de PPP de pantalla actual, el marco de trabajo selecciona la **imagen** que tiene el valor de *MinDPI* más cercano menor que la configuración de PPP de pantalla actual y escala el recurso de imagen hacia arriba. De lo contrario, si no se declara ningún elemento de **imagen** con un valor de atributo *MinDPI* inferior al valor de PPP de pantalla actual, el marco de trabajo selecciona el valor de *MinDPI* más cercano mayor que la configuración de PPP de pantalla actual y escala el recurso de imagen hacia abajo.

 

En el ejemplo siguiente se muestra cómo declarar un conjunto de imágenes para acomodar varios tamaños de cinta y configuraciones del sistema.


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



Si las imágenes declaradas en el marcado se invalidan en tiempo de ejecución por cualquier motivo, se consultan las nuevas imágenes de la aplicación host. Cuando estas imágenes se generan y se cargan mediante programación, la aplicación debe intentar devolver imágenes cuyo tamaño se ajusta a los tamaños de icono del sistema predeterminados determinados por la [ \_ métrica del sistema SM CXICON](/windows/win32/api/winuser/nf-winuser-getsystemmetrics).

> [!Note]  
> Las imágenes grandes tienen un tamaño de SM \_ CXICON por SM \_ CXICON y las imágenes pequeñas tienen un tamaño de SM \_ CXICON/2 por SM \_ CXICON/2.

 

## <a name="color-depth-transparency-and-contrast"></a>Profundidad de color, transparencia y contraste

Se espera que las imágenes normales tengan el formato de píxel ARGB de 32 bits por píxel (BPP) y que se escalen al tamaño del icono del sistema predeterminado. Este formato admite la transparencia y el suavizado de contorno (usando 8 bits por canal).

> [!WARNING]
> Muchas herramientas de edición de imágenes no conservan el canal alfa de 8 bits de orden superior al cargar o guardar imágenes de 32 BPP.

 

Para que una imagen se muestre correctamente en el modo de contraste alto, debe tener un formato de píxel de 4 BPP con un formato de píxeles. Cuando se representa la imagen, el marco de la cinta de opciones reasigna los colores específicos en función del contexto de alto contraste de la imagen.

En la tabla siguiente se muestra el comportamiento de representación de color de alto contraste del marco de trabajo.



Color de píxel

Valor RGB

Comportamiento

Fondo blanco

Fondo oscuro

FUCSIA

800080

Transparente

Transparente

BLANCO

000000

COLOR \_ WINDOWTEXT

Blanco

Blanco

FFFFFF

ventana de COLOR \_

BLANCO

GRIS OSCURO

808080

COLOR \_ 3DSHADOW

COLOR \_ 3DSHADOW

AMBIGUO

C0C0C0

COLOR \_ 3DFACE

COLOR \_ 3DFACE

GRIS CLARO

DFDFDF

COLOR \_ 3DLIGHT

COLOR \_ 3DLIGHT

AZUL MARINO

000080

N/D

Blanco



 

Para obtener más información sobre los formatos de imagen admitidos por el marco de la cinta de opciones, consulte lo siguiente:

-   [Estructura BITMAPINFOHEADER](/previous-versions//dd183376(v=vs.85)) : describe el formato de píxel ARGB 32 bpp.
-   [Función CreateDIBSection](/windows/win32/api/wingdi/nf-wingdi-createdibsection) : describe cómo crear una imagen de formato de píxel ARGB de 32 bpp.
-   [Función LoadImage](/windows/win32/api/winuser/nf-winuser-loadimagea) : describe cómo cargar una imagen de formato de píxel ARGB 32 bpp.

## <a name="accessibility"></a>Accesibilidad

Basándose en los recursos de imagen para proporcionar información, transmitir la funcionalidad de control y exponer el estado de la aplicación, aumenta la necesidad de los requisitos de accesibilidad durante el desarrollo y el diseño de la aplicación.

En el caso de la compatibilidad básica de contraste alto, la cinta permite que se muestre un conjunto independiente de archivos de imagen cuando un tema de contraste alto está activo. Estas imágenes pueden ser de 32 BPP o 4 BPP, con colores asignados a una paleta especial en la que se invierten los colores oscuros y claros en función de los colores de primer plano y de fondo del tema activo de contraste alto.

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

[**Comando. SmallImages**](windowsribbon-element-command-smallimages.md)
</dt> <dt>

[UI \_ PKEY \_ SmallImage](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> <dt>

[**Comando. LargeImages**](windowsribbon-element-command-largeimages.md)
</dt> <dt>

[UI \_ PKEY \_ LargeImage](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> <dt>

[**Comando. SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)
</dt> <dt>

[UI \_ PKEY \_ SmallHighContrastImage](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> <dt>

[**Comando. LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)
</dt> <dt>

[UI \_ PKEY \_ LargeHighContrastImage](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 