---
description: Windows Vista hace un mayor uso de imágenes en miniatura específicas del archivo que las versiones anteriores de Windows.
title: Controladores de miniaturas
ms.topic: article
ms.date: 07/02/2018
ms.assetid: ed9e17bb-aa28-4f8c-8b5a-9b57cab1c438
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d81accf59401a46dd6b5611e15a67eeec68d5d82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247934"
---
# <a name="thumbnail-handlers"></a>Controladores de miniaturas

Windows Vista hace un mayor uso de imágenes en miniatura específicas del archivo que las versiones anteriores de Windows. Windows Vista los usa en todas las vistas, en los cuadros de diálogo y en cualquier tipo de archivo que las proporciona. Otras aplicaciones también pueden consumir la miniatura. La visualización de miniaturas también ha cambiado. Ahora, hay disponible un espectro continuo de tamaños seleccionables por el usuario en lugar de los tamaños discretos, como iconos y miniaturas proporcionados en Windows XP.

> [!Note]  
> Es posible que escuche estas miniaturas denominadas iconos en directo.

 

Las miniaturas de resolución de 32 bits y un tamaño de hasta 256 x 256 píxeles se usan a menudo en Windows interfaz de usuario de Vista. Los propietarios de formato de archivo deben estar preparados para mostrar sus miniaturas con ese tamaño. También deben proporcionar imágenes no estáticas para sus miniaturas que reflejen el contenido del archivo determinado. Por ejemplo, la miniatura de un archivo de texto debe mostrar una versión en miniatura del documento, incluido su texto.

La [**interfaz IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) se ha introducido para que proporcionar una miniatura sea más fácil y sencillo que en el pasado, cuando se habría usado [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) en su lugar. Tenga en cuenta que el código existente que **usa IExtractImage** sigue siendo válido en Windows Vista. Sin embargo, **IExtractImage** no se admite en el **panel** Detalles.

Este tema trata lo siguiente:

-   [Procesos en miniatura](#thumbnail-processes)
-   [Caché de miniaturas y tamaño](#thumbnail-cache-and-sizing)
-   [Superposiciones de miniatura](#thumbnail-overlays)
-   [Adornos en miniatura](#thumbnail-adornments)
-   [Registro del controlador de miniaturas](#registering-your-thumbnail-handler)
-   [Temas relacionados](#related-topics)

## <a name="thumbnail-processes"></a>Procesos en miniatura

Los controladores, incluidos los controladores de miniaturas, se ejecutan de forma predeterminada en un proceso independiente. Puede forzar que el controlador se ejecute en proceso pasando un valor **NULL** como contexto de enlace en una llamada a [**IShellItem::BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) como se muestra aquí:


```
IShellItem::BindToHandler(NULL, BHID_ThumbnailHandler,..)
```



También puede optar por no ejecutarse del proceso de forma predeterminada estableciendo la entrada DisableProcessIsolation en el Registro como se muestra en este ejemplo. El identificador de clase (CLSID) {E357FCCD-A995-4576-B01F-234630154E96} es el CLSID para las implementaciones de [**IThumbnailProvider.**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider)

```
HKEY_CLASSES_ROOT
   CLSID
      {E357FCCD-A995-4576-B01F-234630154E96}
         DisableProcessIsolation = 1
```

## <a name="thumbnail-cache-and-sizing"></a>Caché de miniaturas y tamaño

Cuando se necesita una miniatura, Windows comprueba primero la caché de miniaturas de la imagen. Se llama al extractor de miniaturas si la imagen no se encuentra en la memoria caché. También se llama cuando la hora de la última modificación de la imagen es posterior a la de la copia en la memoria caché.

Las imágenes en miniatura de esta caché se almacenan en un conjunto de tamaños discretos. Todos los tamaños se dan en píxeles.

-   32x32
-   96x96
-   256x256
-   1024x1024

> [!Note]  
> Estos valores están sujetos a cambios. El código no debe suponer que siempre se usará un tamaño determinado.

 

Si una imagen no es cuadrada, no debe hacerlo usted mismo. Windows es responsable de respetar la relación de aspecto original y de rellenar la imagen a un tamaño cuadrado.

Cuando se solicita una imagen de un tamaño determinado, a menos que se encuentra una coincidencia exacta, Windows Vista siempre recupera la siguiente imagen más grande y la escala verticalmente hasta el tamaño solicitado. Una imagen nunca se escala verticalmente, como era el caso en versiones anteriores de Windows.

En la tabla siguiente se proporcionan algunos ejemplos de la relación entre el tamaño solicitado y el tamaño disponible.



| Tamaño máximo de imagen que proporcione | Tamaño solicitado por el extractor | Se proporciona                                 |
|--------------------------------|---------------------------------|---------------------------------------------|
| 156 x 120                        | 256x256                         | 156 x 120 (No panel, mantener relación de aspecto) |
| 2048 x 1024                      | 256x256                         | 256 x 128 (No panel, mantener relación de aspecto) |



 

Puede declarar un punto de límite como parte de la entrada del identificador de programa de la aplicación asociada en el Registro. Por debajo de este tamaño, no se usan miniaturas.

```
HKEY_CLASSES_ROOT
   .{ProgId}
      ThumbnailCutoff
```

La entrada ThumbnailCutoff es uno de estos valores \_ reg DWORD.

| Value | Corte | HighDPI Sensitive |
|-------|--------|-------------------|
| 0     | 32x32  | Sí               |
| 1     | 16x16  | Sí               |
| 2     | 48x48  | Sí               |
| 3     | 16x16  | Sí               |


La sensibilidad de puntos altos por pulgada (ppp) significa que las dimensiones de píxel de la miniatura se ajustan automáticamente para el valor de ppp mayor. Por ejemplo, una imagen de 32 x 32 a 96 ppp sería una imagen de 40 x 40 a 120 ppp.

Si no se especifica la entrada ThumbnailCutoff, el límite predeterminado es 20 x 20 (no distingue ppp).

## <a name="thumbnail-overlays"></a>Superposiciones de miniatura

Las superposiciones de miniaturas, una imagen pequeña que se muestra en la esquina inferior derecha de la miniatura, proporcionan una oportunidad para que los desarrolladores apliquen la identificación de marca a sus miniaturas. Las superposiciones se declaran en el Registro como parte de la entrada de id. de programa de la aplicación asociada, como se muestra aquí:

```
HKEY_CLASSES_ROOT
   .{ProgId}
      TypeOverlay
```

La entrada TypeOverlay contiene un valor \_ REG SZ interpretado como sigue:

-   Si el valor es una referencia de recursos (un archivo **.ico** incrustado en el archivo DLL), como , esa imagen se usa como superposición para los archivos con esa extensión `ISVComponent.dll,-155` de nombre de archivo. Tenga en cuenta que en este ejemplo, **155** es el identificador de recurso y, si el archivo DLL no está presente en una ruta de acceso estándar (como **C:/Windows/System32),** se requiere la ruta de acceso completa en lugar de solo el nombre del archivo DLL.
-   Si el valor es una cadena vacía, no se aplica ninguna superposición a la imagen.
-   Si el valor no está presente, se usa el icono predeterminado de la aplicación asociada.

Las superposiciones de las miniaturas solo se deben proporcionar a través de este mecanismo y aplicar Windows. No aplique las superposiciones usted mismo.

## <a name="thumbnail-adornments"></a>Adornos en miniatura

Los adornos, como las sombras paralelas, se aplican a las miniaturas en función del tema seleccionado actualmente por el usuario. Los adornos los proporciona Windows; no los cree usted mismo. Windows cambiar el aspecto de adornos concretos en cualquier momento, por lo que si proporciona su propiedad, se arriesga a quedarse sin sincronizar con el sistema. Las miniaturas podrían llegar a tener una vista con fecha o fuera de lugar.

Los adornos potenciales se declaran en el Registro como parte de la entrada del identificador de programa de la aplicación asociada, como se muestra aquí:

```
HKEY_CLASSES_ROOT
   .{ProgId}
      Treatment
```

La entrada Tratamiento contiene uno de estos valores reg \_ DWORD:



| Value | Significado         |
|-------|-----------------|
| 0     | Sin adorno    |
| 1     | Sombra paralela     |
| 2     | Borde de la foto    |
| 3     | Video Sprockets |


De forma predeterminada, se aplica una sombra paralela a las imágenes.

## <a name="registering-your-thumbnail-handler"></a>Registro del controlador de miniaturas

El registro de un controlador de miniaturas se basa en asociaciones de archivo estándar.

El GUID de la extensión de Shell del controlador de miniaturas es `E357FCCD-A995-4576-B01F-234630154E96` .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider)
</dt> <dt>

[Compilar controladores de miniaturas](building-thumbnail-providers.md)
</dt> <dt>

[Instrucciones del controlador de miniaturas](thumbnail-provider-guidelines.md)
</dt> </dl>

 

 



