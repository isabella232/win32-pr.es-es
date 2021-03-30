---
description: En el ejemplo de código WSOleDB se muestra Active Template Library (ATL) OLE DB el acceso a las aplicaciones de Windows Search y se muestran dos métodos adicionales para recuperar los resultados de la búsqueda de Windows.
ms.assetid: c81bf3af-e023-4384-8c89-0fa9c8f08773
title: WSOleDB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6cecfc308fdfa9af796e64ab8bc6273f9c4d94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907747"
---
# <a name="wsoledb"></a>WSOleDB

En el ejemplo de código WSOleDB se muestra Active Template Library (ATL) OLE DB el acceso a las aplicaciones de Windows Search y se muestran dos métodos adicionales para recuperar los resultados de la búsqueda de Windows.

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
| GitHub        | [Ejemplo de WSOleDB](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSOleDB)         |

> [!NOTE]  
> En todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.

## <a name="building-the-sample"></a>Generar el ejemplo

1. Abra el explorador de Windows y navegue hasta el directorio del proyecto **WSOleDB** .
2. Haga doble clic en el icono del archivo WSOleDB. sln para abrir el proyecto en Visual Studio.
  
    > [!NOTE]  
    > El archivo sln se creó con una versión anterior de Visual Studio, por lo que será necesario actualizarlo si está ejecutando Visual Studio 2012 o posterior. Esto no afectará al comportamiento del ejemplo.

3. En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1. Desplácese hasta el directorio que contiene el nuevo ejecutable, mediante la ventana del símbolo del sistema o el explorador de Windows.
2. En el símbolo del sistema, escriba `WSOleDB.exe` o, en el explorador de Windows, haga doble clic en el icono de WSOleDB.exe.

## <a name="related-topics"></a>Temas relacionados

### <a name="reference"></a>Referencia

[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

### <a name="conceptual"></a>Conceptual

[Información general sobre la programación de OLE DB](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a>Otros ejemplos

[Ejemplos de código de búsqueda](-search-samples-ovw.md)
