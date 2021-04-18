---
description: El WiLstPrd.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. El script de ejemplo se conecta a un objeto de instalador y enumera los productos registrados y la información del producto.
ms.assetid: 13615dc2-ebc7-4536-9dd8-9bb1dbf3cfaf
title: Enumerar productos, propiedades, características y componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20d2f563efad42108f763b909e7a1118e255dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686796"
---
# <a name="list-products-properties-features-and-components"></a>Enumerar productos, propiedades, características y componentes

El WiLstPrd.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). El script de ejemplo se conecta a un objeto de [**instalador**](installer-object.md) y enumera los productos registrados y la información del producto.

Este ejemplo muestra el uso de:

-   [**Propiedad ProductInfo**](installer-productinfo.md)
-   [**Propiedad ProductState (objeto Installer)**](installer-productstate-property.md)
-   [**Propiedad Products**](installer-products.md)
-   [**Propiedad Features**](installer-features.md)
-   [**Propiedad FeatureParent**](installer-featureparent.md)
-   [**Propiedad FeatureState**](installer-featurestate.md)
-   [**Propiedad Components**](installer-components.md)
-   [**Propiedad ComponentClients**](installer-componentclients.md)
-   [**Propiedad ComponentPath**](installer-componentpath.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md)
-   [**Método**](installer-registryvalue.md) del objeto del [ **instalador**](installer-object.md)

Para usar este ejemplo, necesitará la versión CScript.exe o WScript.exe de Windows Script Host. Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la siguiente sintaxis. La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ ruta de acceso al archivo \] . El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**cscript WiLstPrd.vbs \[ Opciones de nombre de producto \] \[\]**

Especifique el nombre de producto sin distinción de mayúsculas y minúsculas o el GUID de ID. de producto del producto instalado o anunciado. Si no se especifica ningún producto o opción, el instalador muestra todos los productos instalados o anunciados en el sistema.

Tenga en cuenta que estas opciones no son modificadores, por lo que no debe prefijarse con una barra diagonal (/) en la línea de comandos. Las siguientes opciones se pueden combinar mediante la concatenación de las letras. Por ejemplo, "PC" para mostrar las propiedades de los productos y los componentes instalados.



| Opción               | Descripción                                                                                                                           |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| no se especificaron opciones | Enumera las propiedades de los productos.                                                                                                        |
| p                    | Enumera las propiedades de los productos.                                                                                                        |
| f                    | Enumerar las características de los productos, los padres de características y los Estados de instalación                                                                 |
| c                    | Enumera los componentes instalados de los productos.                                                                                              |
| d                    | Enumere el valor bajo **HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ SharedDlls** para los archivos de claves del componente de los productos. |



 

Para obtener más información, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md) para obtener ejemplos adicionales de scripting. Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

 

 



