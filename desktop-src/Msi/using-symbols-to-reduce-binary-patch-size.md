---
description: El uso de símbolos públicos para los archivos binarios de imagen de destino y actualización puede reducir el tamaño de las revisiones binarias aproximadamente a la mitad.
ms.assetid: 83351a1b-ba70-4f0b-bacf-71ad7993a5aa
title: Usar símbolos para reducir el tamaño de revisión binaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d5ccf33dbf3ffefbee909d99bd0204ea2f49aba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253982"
---
# <a name="using-symbols-to-reduce-binary-patch-size"></a>Usar símbolos para reducir el tamaño de revisión binaria

El uso de símbolos públicos para los archivos binarios de imagen de destino y actualización puede reducir el tamaño de las revisiones binarias aproximadamente a la mitad. La reducción real depende de los símbolos usados. Tenga en cuenta que el uso de símbolos puede dar lugar a tiempos de creación de revisiones más lentos, ya que se tarda más tiempo en procesar los archivos de símbolos.

Para reducir el tamaño de una revisión binaria mediante símbolos, debe proporcionar símbolos para los archivos binarios de imagen de destino y de actualización. Especifique los símbolos de la columna SymbolPaths de la [tabla TargetImages](targetimages-table-patchwiz-dll-.md) y la columna SymbolPaths de [la tabla UpgradedImages.](upgradedimages-table-patchwiz-dll-.md) Debe usar Visual C++ para generar símbolos en el formato de archivo de base de datos de programa (PDB). Las versiones más recientes Visual C++ proporcionan toda la información necesaria en el archivo PDB. Las versiones anteriores de Visual C++ también generan el formato de archivo de depuración (DBG). En este caso, el valor SymbolsPaths debe especificar la ubicación de los archivos PDB y DBG.

Por ejemplo, TargetImage para una revisión podría ser el paquete de instalación que se incluye con Windows 2000 y que instala la versión 1.1.1029.0 de MSI.DLL. UpgradedImage podría ser el paquete de instalación actualizado que se incluye con Windows 2000 con Service Pack 1 (SP1) y que instala la versión 1.11.1314.0 de MSI.DLL. A continuación, se tendrían que crear dos archivos de propiedades de creación de revisiones (PATCH), uno con la columna SymbolPaths de las tablas [TargetImages](targetimages-table-patchwiz-dll-.md) y [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) que dejó NULL (en blanco) y la otra con la columna SymbolPaths de las tablas TargetImages y UpgradedImages rellenada con la ubicación de los símbolos de los archivos binarios. En este caso, el tamaño de la revisión generada sin usar símbolos puede ser aproximadamente tres veces el tamaño de la revisión generada mediante símbolos.

La Mpatch.exe se puede usar para probar la generación de revisiones binarias para un único archivo y para comprobar si los símbolos son válidos o no. La utilidad Mpatch.exe se incluye en los componentes del SDK de Windows [para Windows programadores del instalador](platform-sdk-components-for-windows-installer-developers.md). La salida de Mpatch.exe indicará si los símbolos no coinciden.

Por ejemplo, escriba la siguiente línea de comandos para comprobar si los símbolos son válidos o no.

**mpatch.exe -NEWSYMPATH:d: \\ update -OLDSYMPATH:d: \\ target d: targetexample.dll \\ \\ d: updateexample.dll \\ \\ example.pat**

Si los símbolos no están en la ubicación correcta, la salida de Mpatch.exe puede incluir la advertencia siguiente.

``` syntax
WARNING: no debug symbols for d:\update\example.dll
```

 

 



