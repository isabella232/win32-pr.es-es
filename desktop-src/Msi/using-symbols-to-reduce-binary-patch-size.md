---
description: El uso de símbolos públicos para los archivos binarios de imagen de destino y actualización puede reducir el tamaño de las revisiones binarias en aproximadamente una mitad.
ms.assetid: 83351a1b-ba70-4f0b-bacf-71ad7993a5aa
title: Usar símbolos para reducir el tamaño de la revisión binaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d5ccf33dbf3ffefbee909d99bd0204ea2f49aba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677431"
---
# <a name="using-symbols-to-reduce-binary-patch-size"></a>Usar símbolos para reducir el tamaño de la revisión binaria

El uso de símbolos públicos para los archivos binarios de imagen de destino y actualización puede reducir el tamaño de las revisiones binarias en aproximadamente una mitad. La reducción real depende de los símbolos usados. Tenga en cuenta que el uso de símbolos puede dar lugar a tiempos de creación de revisiones más lentos, ya que tarda más tiempo en procesar los archivos de símbolos.

Para reducir el tamaño de una revisión binaria mediante símbolos, debe proporcionar símbolos para los archivos binarios de la imagen de destino y de actualización. Especifique los símbolos en la columna SymbolPaths de la tabla [TargetImages](targetimages-table-patchwiz-dll-.md) y la columna SymbolPaths de la tabla [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) . Debe utilizar Visual C++ para generar símbolos en el formato de archivo de base de datos de programa (PDB). Las versiones más recientes de Visual C++ proporcionan toda la información necesaria en el archivo PDB. Las versiones anteriores de Visual C++ también generan el formato de archivo de depuración (DBG). En este caso, el valor SymbolsPaths debe especificar la ubicación de los archivos PDB y DBG.

Por ejemplo, el TargetImage de una revisión podría ser el paquete de instalación incluido con Windows 2000 y que instala la versión 1.1.1029.0 de MSI.DLL. UpgradedImage podría ser el paquete de instalación actualizado que se incluye con Windows 2000 con Service Pack 1 (SP1) y que instala la versión 1.11.1314.0 de MSI.DLL. A continuación, se tendrían que crear dos archivos de propiedades de creación de revisiones (PCP), uno con la columna SymbolPaths de las tablas [TargetImages](targetimages-table-patchwiz-dll-.md) y [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) a la izquierda (en blanco) y el otro con la columna SymbolPaths de las tablas TargetImages y UpgradedImages que se rellenan con la ubicación de los símbolos para los archivos binarios. En este caso, el tamaño de la revisión generada sin usar símbolos puede ser aproximadamente tres veces el tamaño de la revisión generado mediante símbolos.

La utilidad Mpatch.exe se puede usar para probar la generación de revisiones binarias para un único archivo y para comprobar si los símbolos son válidos o no. La utilidad de Mpatch.exe se incluye en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). La salida de Mpatch.exe indicará si los símbolos no coinciden.

Por ejemplo, escriba la siguiente línea de comandos para comprobar si los símbolos son válidos.

**mpatch.exe-NEWSYMPATH: d: \\ Update-OLDSYMPATH: d: \\ target d: \\ target \\example.dll d: \\ Update \\example.dll example. Pat**

Si los símbolos no están en la ubicación correcta, la salida de Mpatch.exe puede incluir la advertencia siguiente.

``` syntax
WARNING: no debug symbols for d:\update\example.dll
```

 

 



