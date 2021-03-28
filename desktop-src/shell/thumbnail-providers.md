---
description: Windows Vista hace un mayor uso de las imágenes en miniatura específicas del archivo que las versiones anteriores de Windows.
title: Controladores en miniatura
ms.topic: article
ms.date: 07/02/2018
ms.assetid: ed9e17bb-aa28-4f8c-8b5a-9b57cab1c438
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d81accf59401a46dd6b5611e15a67eeec68d5d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278491"
---
# <a name="thumbnail-handlers"></a>Controladores en miniatura

Windows Vista hace un mayor uso de las imágenes en miniatura específicas del archivo que las versiones anteriores de Windows. Windows Vista los utiliza en todas las vistas, en los cuadros de diálogo y en cualquier tipo de archivo que las proporcione. Otras aplicaciones también pueden usar su miniatura. También se ha cambiado la presentación en miniatura. Ahora, hay disponible un espectro continuo de tamaños seleccionables por el usuario en lugar de los tamaños discretos, como los iconos y las miniaturas que se proporcionan en Windows XP.

> [!Note]  
> Podría oír estas miniaturas denominadas iconos dinámicos.

 

En la interfaz de usuario de Windows Vista, a menudo se usan vistas en miniatura de la resolución de 32 bits y tan grandes como 256x256 píxeles. Los propietarios de formato de archivo deben estar preparados para mostrar sus miniaturas en ese tamaño. También deben proporcionar imágenes no estáticas para las miniaturas que reflejan el contenido de un archivo concreto. Por ejemplo, la miniatura de un archivo de texto debería mostrar una versión en miniatura del documento, incluido el texto.

La interfaz [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) se ha introducido para proporcionar una miniatura más sencilla y más sencilla que en el pasado, cuando se habría usado [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) en su lugar. Tenga en cuenta que el código existente que usa **IExtractImage** sigue siendo válido en Windows Vista. Sin embargo, **IExtractImage** no se admite en el panel de **detalles** .

Este tema trata lo siguiente:

-   [Procesos en miniatura](#thumbnail-processes)
-   [Caché y tamaño de miniaturas](#thumbnail-cache-and-sizing)
-   [Superposiciones en miniatura](#thumbnail-overlays)
-   [Elementos gráficos de miniaturas](#thumbnail-adornments)
-   [Registrar el controlador de miniaturas](#registering-your-thumbnail-handler)
-   [Temas relacionados](#related-topics)

## <a name="thumbnail-processes"></a>Procesos en miniatura

Los controladores, incluidos los controladores de miniaturas, se ejecutan de forma predeterminada en un proceso independiente. Puede forzar que el controlador se ejecute en proceso pasando un valor **null** como contexto de enlace en una llamada a [**IShellItem:: BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) como se muestra aquí:


```
IShellItem::BindToHandler(NULL, BHID_ThumbnailHandler,..)
```



También puede optar por no quedarse fuera de proceso de forma predeterminada estableciendo la entrada DisableProcessIsolation en el registro tal como se muestra en este ejemplo. El identificador de clase (CLSID) {E357FCCD-A995-4576-B01F-234630154E96} es el CLSID para las implementaciones de [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) .

```
HKEY_CLASSES_ROOT
   CLSID
      {E357FCCD-A995-4576-B01F-234630154E96}
         DisableProcessIsolation = 1
```

## <a name="thumbnail-cache-and-sizing"></a>Caché y tamaño de miniaturas

Cuando se necesita una miniatura, Windows comprueba primero la caché en miniatura de la imagen. Se llama al extractor de miniaturas si la imagen no se encuentra en la memoria caché. También se llama cuando la hora de la última modificación de la imagen es posterior a la de la copia de la memoria caché.

Las imágenes en miniatura de esta caché se almacenan en un conjunto de tamaños discretos. Todos los tamaños se proporcionan en píxeles.

-   32x32
-   96x96
-   256x256
-   1024x1024

> [!Note]  
> Estos valores están sujetos a cambios. El código no debe suponer que siempre se usará un tamaño determinado.

 

Si una imagen no es cuadrada, no debe rellenarla. Windows es responsable de respetar la relación de aspecto original y de rellenar la imagen con un tamaño cuadrado.

Cuando se solicita una imagen de un tamaño determinado, a menos que se encuentre una coincidencia exacta, Windows Vista siempre recupera la siguiente imagen más grande y la escala hasta el tamaño solicitado. Una imagen nunca se escala verticalmente en tamaño como era el caso de las versiones anteriores de Windows.

En la tabla siguiente se proporcionan algunos ejemplos de la relación entre el tamaño solicitado y el tamaño disponible.



| Tamaño máximo de la imagen que se proporciona | Tamaño solicitado por el extractor | Proporciona                                 |
|--------------------------------|---------------------------------|---------------------------------------------|
| 156x120                        | 256x256                         | 156x120 (no rellenar, mantener relación de aspecto) |
| 2048x1024                      | 256x256                         | 256x128 (no rellenar, mantener relación de aspecto) |



 

Puede declarar un punto de corte como parte de la entrada de ID. de programa de la aplicación asociada en el registro. Por debajo de este tamaño, no se usan vistas en miniatura.

```
HKEY_CLASSES_ROOT
   .{ProgId}
      ThumbnailCutoff
```

La entrada ThumbnailCutoff es uno de estos valores de REG \_ DWORD.

| Value | Límite | HighDPI sensible |
|-------|--------|-------------------|
| 0     | 32x32  | Sí               |
| 1     | 16x16  | Sí               |
| 2     | 48x48  | Sí               |
| 3     | 16x16  | Sí               |


La distinción de puntos por pulgada (PPP) de alto significa que las dimensiones de píxeles de la miniatura se ajustan automáticamente para un mayor tamaño de PPP. Por ejemplo, una imagen de 32 x 96 PPP sería una imagen 40 x 40 a 120 ppp.

Si no se especifica la entrada ThumbnailCutoff, el límite predeterminado es 20x20 (no sensible a PPP).

## <a name="thumbnail-overlays"></a>Superposiciones en miniatura

Las superposiciones en miniatura, una pequeña imagen que se muestra en la esquina inferior derecha de la miniatura, proporcionan una oportunidad para que los desarrolladores apliquen la identificación de la marca a sus miniaturas. Las superposiciones se declaran en el registro como parte de la entrada del identificador de programa de la aplicación asociada, como se muestra aquí:

```
HKEY_CLASSES_ROOT
   .{ProgId}
      TypeOverlay
```

La entrada TypeOverlay contiene un valor de REG \_ SZ interpretado de la siguiente manera:

-   Si el valor es una referencia de recursos (un archivo **. ico** incrustado en el archivo dll) como `ISVComponent.dll,-155` , esa imagen se utiliza como la superposición de los archivos con esa extensión de nombre de archivo. Tenga en cuenta que en este ejemplo, **155** es el identificador de recurso y, si el archivo dll no está presente en una ruta de acceso estándar (como **C:/Windows/system32**), se requiere la ruta de acceso completa en lugar de solo el nombre del archivo dll.
-   Si el valor es una cadena vacía, no se aplica ninguna superposición a la imagen.
-   Si el valor no está presente, se usa el icono predeterminado de la aplicación asociada.

Las superposiciones de las miniaturas solo deben proporcionarse a través de este mecanismo y se pueden aplicar mediante Windows. No aplique las superposiciones por su cuenta.

## <a name="thumbnail-adornments"></a>Elementos gráficos de miniaturas

Los elementos gráficos como las sombras paralelas se aplican a las miniaturas en función del tema seleccionado actualmente por el usuario. Windows proporciona elementos gráficos; no las cree. Windows podría cambiar la apariencia de los elementos gráficos concretos en cualquier momento, por lo que si usted le proporcionó el riesgo, podría quedar fuera de la sincronización con el sistema. Es posible que las miniaturas se desplacen por la fecha o la ubicación.

Los posibles elementos gráficos se declaran en el registro como parte de la entrada del identificador de programa de la aplicación asociada, como se muestra aquí:

```
HKEY_CLASSES_ROOT
   .{ProgId}
      Treatment
```

La entrada de tratamiento contiene uno de estos \_ valores de REG DWORD:



| Value | Significado         |
|-------|-----------------|
| 0     | Sin elemento gráfico    |
| 1     | Sombra paralela     |
| 2     | Borde fotográfico    |
| 3     | Engranajes de vídeo |


De forma predeterminada, se aplica una sombra paralela a las imágenes.

## <a name="registering-your-thumbnail-handler"></a>Registrar el controlador de miniaturas

El registro de un controlador de miniaturas se basa en las asociaciones de archivo estándar.

El GUID de la extensión de Shell del controlador de miniaturas es `E357FCCD-A995-4576-B01F-234630154E96` .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider)
</dt> <dt>

[Crear controladores de miniaturas](building-thumbnail-providers.md)
</dt> <dt>

[Instrucciones de controlador de miniaturas](thumbnail-provider-guidelines.md)
</dt> </dl>

 

 



