---
description: El ejemplo de código WSOleDB muestra Active Template Library (ATL) OLE DB acceso a aplicaciones de Windows Search y muestra dos métodos adicionales para recuperar resultados de Windows Search.
ms.assetid: c81bf3af-e023-4384-8c89-0fa9c8f08773
title: WSOleDB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17000de683fc9f5171bc556c607c7c068cabb4b3e88693407e1381565fb6b242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969624"
---
# <a name="wsoledb"></a>WSOleDB

El ejemplo de código WSOleDB muestra Active Template Library (ATL) OLE DB acceso a aplicaciones de Windows Search y muestra dos métodos adicionales para recuperar resultados de Windows Search.

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

| Ubicación      | Dirección URL de ruta de acceso                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub        | [Ejemplo de WSOleDB](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSOleDB)         |

> [!NOTE]  
> Para todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.

## <a name="building-the-sample"></a>Generar el ejemplo

1. Abra Windows Explorador de aplicaciones y vaya al **directorio del proyecto WSOleDB.**
2. Haga doble clic en el icono del archivo WSOleDB.sln para abrir el proyecto en Visual Studio.
  
    > [!NOTE]  
    > El archivo sln se creó en una versión anterior de Visual Studio, por lo que será necesario actualizarlo si está ejecutando Visual Studio 2012 o posterior. Esto no afectará al comportamiento de la muestra.

3. En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1. Vaya al directorio que contiene el nuevo ejecutable, mediante la ventana símbolo del sistema o Windows Explorador.
2. En el símbolo del sistema, escriba o, en Windows Explorer, haga doble clic `WSOleDB.exe` en el icono para WSOleDB.exe.

## <a name="related-topics"></a>Temas relacionados

### <a name="reference"></a>Referencia

[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

### <a name="conceptual"></a>Conceptual

[OLE DB de programación](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a>Otros ejemplos

[Ejemplos de código de búsqueda](-search-samples-ovw.md)
