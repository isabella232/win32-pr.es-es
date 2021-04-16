---
description: En el ejemplo de código OpenSearch se muestra cómo crear un servicio de búsqueda federado mediante el protocolo OpenSearch y un archivo de descriptor de OpenSearch (. osdx) (un conector de búsqueda).
ms.assetid: 792884e4-826b-4474-82e1-1680d4d8b602
title: OpenSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8656efec434744d14714529d1e7b0d01a5349ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423727"
---
# <a name="opensearch"></a>OpenSearch

En el ejemplo de código OpenSearch se muestra cómo crear un servicio de búsqueda federado mediante el protocolo [OpenSearch](https://github.com/dewitt/opensearch) y un archivo de descriptor de OpenSearch (. osdx) (un conector de búsqueda).

En este tema se incluyen las siguientes secciones.

-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="requirements"></a>Requisitos



| Producto     | Versión mínima del producto |
|-------------|-------------------------|
| Windows     | Windows 7               |
| Windows SDK | 7.0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location      | URL de ruta de acceso                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub  | [Ejemplo de OpenSearch](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/OpenSearch)      |



 

 

> [!Note]  
> En todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.

 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **AdventureSearch** . 
2.  Escriba `msbuild AdventureSearch.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra el explorador de Windows y navegue hasta el directorio del proyecto **AdventureSearch** .
2.  Haga doble clic en el icono del archivo AdventureSearch. sln para abrir el proyecto en Visual Studio.
    > [!Note]  
    > La extensión de nombre de archivo. sln no se muestra en configuración de carpeta predeterminada. En esa situación, puede identificarse por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".

     

3.  En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Desplácese hasta el directorio que contiene el nuevo ejecutable, mediante la ventana del símbolo del sistema o el explorador de Windows.
2.  En el símbolo del sistema, escriba `AdventureSearch.exe` o, en el explorador de Windows, haga doble clic en el icono de AdventureSearch.exe.
3.  En el símbolo del sistema, escriba `GetOSDX.exe` o, en el explorador de Windows, haga doble clic en el icono de GetOSDX.exe.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Información general sobre el esquema de Descripción del conector de búsqueda](search-sconn-desc-schema-entry.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Búsqueda federada en Windows](-search-federated-search-overview.md)
</dt> <dt>

[Ejemplos de código de búsqueda](-search-samples-ovw.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Esquema de descripción de biblioteca](../shell/library-schema-entry.md)
</dt> </dl>

 

 
