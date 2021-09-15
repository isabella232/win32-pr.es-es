---
description: El ejemplo de código DSearch muestra cómo crear una clase para una aplicación de consola estática para consultar Windows Search mediante el ensamblado Microsoft.Search.Interop para ISearchQueryHelper.
ms.assetid: 9c09b1fe-c63e-4c6e-9c8b-f5e29cf0fe9e
title: DSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4285596a8109361accd6b3adecf80ea98074e55e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360385"
---
# <a name="dsearch"></a>DSearch

El ejemplo de código DSearch muestra cómo crear una clase para una aplicación de consola estática para consultar Windows Search mediante el ensamblado Microsoft.Search.Interop para [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper).

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

| Location      | Dirección URL de ruta de acceso                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub        | [Ejemplo de DSearch](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/DSearch)         |

> [!NOTE]  
> Para todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para la versión más actualizada.

## <a name="building-the-sample"></a>Generar el ejemplo

1. Abra Windows explorador y vaya al directorio **del proyecto DSearch.**
2. Haga doble clic en el icono del archivo DSearch.sln para abrir el proyecto en Visual Studio.
  
    > [!NOTE]  
    > El archivo sln se creó en una versión anterior de Visual Studio, por lo que será necesario actualizarlo si está ejecutando Visual Studio 2012 o posterior. Esto no afectará al comportamiento de la muestra.

3. En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1. Vaya al directorio que contiene el nuevo ejecutable, mediante la ventana símbolo del sistema o Windows Explorador.
2. En el símbolo del sistema, escriba o, en Windows Explorer, haga doble clic en el `DSearch.exe` icono de DSearch.exe.

## <a name="related-topics"></a>Temas relacionados

### <a name="reference"></a>Referencia

[**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)

[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

### <a name="other-samples"></a>Otros ejemplos

[Ejemplos de código de búsqueda](-search-samples-ovw.md)
