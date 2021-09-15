---
description: El ejemplo de código IFilterSample muestra cómo crear una clase base IFilter para implementar la interfaz IFilter.
ms.assetid: 4c0df747-627d-4937-a117-d43137d5d081
title: IFilterSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f66bf32c4abe25038aa6b2a3b6d879ba65cf7a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360384"
---
# <a name="ifiltersample"></a>IFilterSample

El ejemplo de código IFilterSample muestra cómo crear una clase base de IFilter para implementar la [**interfaz IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)

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
| GitHub        | [IFilterSample](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)          |

> [!NOTE]  
> Para todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.

## <a name="building-the-sample"></a>Generar el ejemplo

1. Abra Windows explorador y vaya al directorio **del proyecto FilterBase.**
2. Haga doble clic en el icono del archivo FilterBase.sln para abrir el proyecto en Visual Studio.

    > [!NOTE]  
    > El archivo sln se creó en una versión anterior de Visual Studio, por lo que será necesario actualizarlo si está ejecutando Visual Studio 2012 o posterior. Esto no afectará al comportamiento de la muestra.

3. En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1. Vaya al directorio que contiene el nuevo ejecutable, mediante la ventana símbolo del sistema o Windows Explorador.
2. En el símbolo del sistema, escriba o, en Windows Explorer, haga doble clic en el `FilterBase.exe` icono de FilterBase.exe.

## <a name="related-topics"></a>Temas relacionados

### <a name="reference"></a>Referencia

[**Ifilter**](/windows/win32/api/filter/nn-filter-ifilter)

### <a name="conceptual"></a>Conceptual

[Desarrollar controladores de filtro](-search-ifilter-conceptual.md)

### <a name="other-samples"></a>Otros ejemplos

[Ejemplos de código de búsqueda](-search-samples-ovw.md)
