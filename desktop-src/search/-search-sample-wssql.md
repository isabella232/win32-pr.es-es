---
description: En el ejemplo de código WSSQL se muestra cómo comunicarse entre Microsoft OLE DB y Windows Search a través de Lenguaje de consulta estructurado (SQL).
ms.assetid: 28663608-66b3-4404-9426-5a4b5f52a408
title: WSSQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac8f76b995d21a562f843344d1722cecec433af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907746"
---
# <a name="wssql"></a>WSSQL

En el ejemplo de código WSSQL se muestra cómo comunicarse entre Microsoft OLE DB y Windows Search a través de Lenguaje de consulta estructurado (SQL).

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
| GitHub        | [Ejemplo de WSSQL](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSSQL)           |

> [!NOTE]  
> En todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.

## <a name="building-the-sample"></a>Generar el ejemplo

1. Abra el explorador de Windows y navegue hasta el directorio del proyecto **WSSQL** .
2. Haga doble clic en el icono del archivo WSSQL. sln para abrir el proyecto en Visual Studio.
    > [!NOTE]  
    > El archivo sln se creó con una versión anterior de Visual Studio, por lo que será necesario actualizarlo si está ejecutando Visual Studio 2012 o posterior. Esto no afectará al comportamiento del ejemplo.

3. En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1. Desplácese hasta el directorio que contiene el nuevo ejecutable, mediante la ventana del símbolo del sistema o el explorador de Windows.
2. En el símbolo del sistema, escriba `WSSQL.exe` o, en el explorador de Windows, haga doble clic en el icono de WSSQL.exe.

## <a name="related-topics"></a>Temas relacionados

### <a name="conceptual"></a>Conceptual

[Usar la sintaxis SQL de búsqueda de Windows](-search-sql-windowssearch-entry.md)

[Información general del lenguaje de consulta](-search-sql-generalqueryinfo.md)

[Información general sobre la programación de OLE DB](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a>Otros ejemplos

[Ejemplos de código de búsqueda](-search-samples-ovw.md)
