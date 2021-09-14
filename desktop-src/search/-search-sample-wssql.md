---
description: El ejemplo de código WSSQL muestra cómo comunicarse entre Microsoft OLE DB y Windows Search a través de Lenguaje de consulta estructurado (SQL).
ms.assetid: 28663608-66b3-4404-9426-5a4b5f52a408
title: WSSQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac8f76b995d21a562f843344d1722cecec433af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363218"
---
# <a name="wssql"></a>WSSQL

El ejemplo de código WSSQL muestra cómo comunicarse entre Microsoft OLE DB y Windows Search a través de Lenguaje de consulta estructurado (SQL).

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
| GitHub        | [Ejemplo de WSSQL](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSSQL)           |

> [!NOTE]  
> Para todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para la versión más actualizada.

## <a name="building-the-sample"></a>Generar el ejemplo

1. Abra Windows Explorador de aplicaciones y vaya al **directorio del proyecto de WSSQL.**
2. Haga doble clic en el icono del archivo WSSQL.sln para abrir el proyecto en Visual Studio.
    > [!NOTE]  
    > El archivo sln se creó en una versión anterior de Visual Studio, por lo que será necesario actualizarlo si está ejecutando Visual Studio 2012 o posterior. Esto no afectará al comportamiento de la muestra.

3. En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1. Vaya al directorio que contiene el nuevo ejecutable, mediante la ventana símbolo del sistema o Windows explorador.
2. En el símbolo del sistema, escriba o, en Windows Explorer, haga doble clic en el `WSSQL.exe` icono de WSSQL.exe.

## <a name="related-topics"></a>Temas relacionados

### <a name="conceptual"></a>Conceptual

[Uso de Windows de búsqueda SQL búsqueda](-search-sql-windowssearch-entry.md)

[Información general del lenguaje de consulta](-search-sql-generalqueryinfo.md)

[OLE DB de programación](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a>Otros ejemplos

[Ejemplos de código de búsqueda](-search-samples-ovw.md)
