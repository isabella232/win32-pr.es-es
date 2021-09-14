---
description: 'El ejemplo de código ReindexMatchingUrls muestra cómo proporcionar tres maneras de especificar los archivos que se van a volver a indexar: direcciones URL que coinciden con un tipo de archivo, un tipo mime o una cláusula WHERE especificada.'
ms.assetid: f7b3a8a6-b464-46d4-a99c-fc56eea9b1ec
title: ReindexMatchingUrls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a7bb6ae3148f6969fc5349e1ebdf666a527282
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363238"
---
# <a name="reindexmatchingurls"></a>ReindexMatchingUrls

El ejemplo de código ReindexMatchingUrls muestra cómo proporcionar tres maneras de especificar los archivos que se van a volver a indexar: direcciones URL que coinciden con un tipo de archivo, un tipo mime o una cláusula WHERE especificada.

En este tema se incluyen las siguientes secciones.

- [Requisitos](#requirements)
- [Descargar el ejemplo](#downloading-the-sample)
- [Compilar el ejemplo](#building-the-sample)
- [Ejecución del ejemplo](#running-the-sample)
- [Temas relacionados](#related-topics)

## <a name="requirements"></a>Requisitos

| Producto     | Versión del producto          |
|-------------|--------------------------|
| Windows     | Windows 7, 8.1 o 10    |
| Windows SDK | 7.0 o superior           |

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en la siguiente ubicación.

| Location      | Dirección URL de ruta de acceso                                                                      |
|---------------|-------------------------------------------------------------------------------|
| GitHub  | [Ejemplo de ReindexMatchingUrls](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/ReindexMatchingUrls) |

> [!NOTE]  
> Para todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para la versión más actualizada.

## <a name="building-the-sample"></a>Generar el ejemplo

1. Abra Windows explorador y vaya al directorio **de proyecto ReindexMatchingUrls.** Por ejemplo, la ruta de instalación predeterminada completa es `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\ReindexMatchingUrls` .
2. Haga doble clic en el icono del archivo Reindex.sln para abrir el proyecto en Visual Studio.
  
    > [!NOTE]  
    > El archivo sln se creó en una versión anterior de Visual Studio, por lo que será necesario actualizarlo si está ejecutando Visual Studio 2012 o posterior. Esto no afectará al comportamiento de la muestra.

3. En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1. Vaya al directorio que contiene el nuevo ejecutable, mediante la ventana símbolo del sistema o Windows explorador.
2. En el símbolo del sistema, escriba o, en Windows Explorer, haga doble clic en el `Reindex.exe` icono de Reindex.exe.

## <a name="related-topics"></a>Temas relacionados

### <a name="reference"></a>Referencia

[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink)

[**ISearchViewChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchviewchangedsink)

[**PRIORIZAR \_ MARCAS**](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)

### <a name="other-samples"></a>Otros ejemplos

[Ejemplos de código de búsqueda](-search-samples-ovw.md)
