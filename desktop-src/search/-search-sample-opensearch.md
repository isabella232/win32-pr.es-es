---
description: El OpenSearch muestra cómo crear un servicio de búsqueda federado mediante el protocolo OpenSearch y un archivo de descriptor de OpenSearch (.osdx) (un conector de búsqueda).
ms.assetid: 792884e4-826b-4474-82e1-1680d4d8b602
title: OpenSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6279b66be3b259058cc1b13bae6d9185e035211c65e87c21e070db638e74573
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118051848"
---
# <a name="opensearch"></a>OpenSearch

El OpenSearch muestra cómo crear un servicio de búsqueda federado mediante el protocolo OpenSearch y un archivo de descriptor de [OpenSearch](https://github.com/dewitt/opensearch) (.osdx) (un conector de búsqueda).

En este tema se incluyen las siguientes secciones.

-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="requirements"></a>Requisitos



| Producto     | Versión mínima del producto |
|-------------|-------------------------|
| Windows     | Windows 7               |
| Windows SDK | 7,0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location      | Dirección URL de ruta de acceso                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub  | [OpenSearch ejemplo](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/OpenSearch)      |



 

 

> [!Note]  
> Para todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.

 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y vaya al **directorio del proyecto AdventureSearch.** 
2.  Escriba `msbuild AdventureSearch.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (opción preferida):

1.  Abra Windows Explorer y vaya al **directorio del proyecto AdventureSearch.**
2.  Haga doble clic en el icono del archivo AdventureSearch.sln para abrir el proyecto en Visual Studio.
    > [!Note]  
    > La extensión de nombre de archivo .sln no se muestra en la configuración de carpeta predeterminada. En esa situación, se puede identificar por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".

     

3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Vaya al directorio que contiene el nuevo ejecutable, mediante la ventana símbolo del sistema o Windows Explorador.
2.  En el símbolo del sistema, escriba o, en Windows Explorer, haga doble clic `AdventureSearch.exe` en el icono para AdventureSearch.exe.
3.  En el símbolo del sistema, escriba o, en Windows Explorer, haga doble clic `GetOSDX.exe` en el icono para GetOSDX.exe.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Información general sobre el esquema de descripción del conector de búsqueda](search-sconn-desc-schema-entry.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Búsqueda federada en Windows](-search-federated-search-overview.md)
</dt> <dt>

[Ejemplos de código de búsqueda](-search-samples-ovw.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Esquema de descripción de biblioteca](../shell/library-schema-entry.md)
</dt> </dl>

 

 
