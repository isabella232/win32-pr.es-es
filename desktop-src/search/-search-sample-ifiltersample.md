---
description: En el ejemplo de código IFilterSample se muestra cómo crear una clase base de IFilter para implementar la interfaz IFilter.
ms.assetid: 4c0df747-627d-4937-a117-d43137d5d081
title: IFilterSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f66bf32c4abe25038aa6b2a3b6d879ba65cf7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696288"
---
# <a name="ifiltersample"></a>IFilterSample

En el ejemplo de código IFilterSample se muestra cómo crear una clase base de IFilter para implementar la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .

En este tema se incluyen las siguientes secciones.

- [Requisitos](#requirements)
- [Descargar el ejemplo](#downloading-the-sample)
- [Compilar el ejemplo](#building-the-sample)
- [Ejecutar el ejemplo](#running-the-sample)
- [Temas relacionados](#related-topics)

## <a name="requirements"></a>Requisitos

| Producto     | Versión del producto          |
|-------------|--------------------------|
| Windows     | Windows 7, 8.1 o 10    |
| Windows SDK | 7,0 o superior           |

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en la siguiente ubicación.

| Location      | URL de ruta de acceso                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub        | [IFilterSample](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)          |

> [!NOTE]  
> En todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.

## <a name="building-the-sample"></a>Generar el ejemplo

1. Abra el explorador de Windows y navegue hasta el directorio del proyecto **FilterBase** .
2. Haga doble clic en el icono del archivo FilterBase. sln para abrir el proyecto en Visual Studio.

    > [!NOTE]  
    > El archivo sln se creó con una versión anterior de Visual Studio, por lo que será necesario actualizarlo si está ejecutando Visual Studio 2012 o posterior. Esto no afectará al comportamiento del ejemplo.

3. En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1. Desplácese hasta el directorio que contiene el nuevo ejecutable, mediante la ventana del símbolo del sistema o el explorador de Windows.
2. En el símbolo del sistema, escriba `FilterBase.exe` o, en el explorador de Windows, haga doble clic en el icono de FilterBase.exe.

## <a name="related-topics"></a>Temas relacionados

### <a name="reference"></a>Referencia

[**Imaging**](/windows/win32/api/filter/nn-filter-ifilter)

### <a name="conceptual"></a>Conceptual

[Desarrollar controladores de filtro](-search-ifilter-conceptual.md)

### <a name="other-samples"></a>Otros ejemplos

[Ejemplos de código de búsqueda](-search-samples-ovw.md)
