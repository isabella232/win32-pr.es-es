---
description: El archivo VBScript WiLstPrd.vbs se proporciona en los componentes del SDK de Windows para Windows Instalador de aplicaciones. El script de ejemplo se conecta a un objeto Installer y enumera los productos registrados y la información del producto.
ms.assetid: 13615dc2-ebc7-4536-9dd8-9bb1dbf3cfaf
title: Enumerar productos, propiedades, características y componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20d2f563efad42108f763b909e7a1118e255dcb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071958"
---
# <a name="list-products-properties-features-and-components"></a>Enumerar productos, propiedades, características y componentes

El archivo vbscript WiLstPrd.vbs se proporciona en los componentes del SDK Windows [para Windows instalador de .](platform-sdk-components-for-windows-installer-developers.md) El script de ejemplo se conecta a un [**objeto Installer**](installer-object.md) y enumera los productos registrados y la información del producto.

En este ejemplo se muestra el uso de:

-   [**Propiedad ProductInfo**](installer-productinfo.md)
-   [**Propiedad ProductState (objeto Installer)**](installer-productstate-property.md)
-   [**Propiedad Products**](installer-products.md)
-   [**Propiedad Features**](installer-features.md)
-   [**Propiedad FeatureParent**](installer-featureparent.md)
-   [**Propiedad FeatureState**](installer-featurestate.md)
-   [**Propiedad Components**](installer-components.md)
-   [**ComponentClients, propiedad**](installer-componentclients.md)
-   [**Propiedad ComponentPath**](installer-componentpath.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md)
-   [**Método RegistryValue**](installer-registryvalue.md) del [ **objeto Installer**](installer-object.md)

Necesitará la versión CScript.exe o WScript.exe de Windows script para usar este ejemplo. Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la sintaxis siguiente. Se muestra ayuda si el primer argumento es /? o si se especifican demasiados argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ ruta de acceso al archivo \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca ayuda y 2 si se produce un error en el script.

**Opciones de nombre WiLstPrd.vbs \[ producto de \] \[ cscript\]**

Especifique el nombre del producto que no tiene en cuenta mayúsculas de minúsculas o el GUID del identificador de producto del producto instalado o anunciado. Si no se especifica ningún producto o opción, el instalador enumera todos los productos instalados o anunciados en el sistema.

Tenga en cuenta que estas opciones no son modificadores, por lo que no debe prefijarlos con una barra diagonal (/) en la línea de comandos. Las siguientes opciones se pueden combinar concatenando las letras. Por ejemplo, "pc" para enumerar las propiedades de los productos y los componentes instalados.



| Opción               | Descripción                                                                                                                           |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| no se especifica ninguna opción | Enumera las propiedades de los productos.                                                                                                        |
| p                    | Enumera las propiedades de los productos.                                                                                                        |
| f                    | Enumeración de las características, los elementos principales de las características y los estados de instalación de los productos                                                                 |
| c                    | Enumera los componentes instalados de los productos.                                                                                              |
| d                    | Enumere el valor **de HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion \\ SharedDlls** para los archivos clave del componente del producto. |



 

Para obtener más información, vea [Windows de scripting del instalador para](windows-installer-scripting-examples.md) obtener ejemplos de scripting adicionales. Para obtener utilidades de ejemplo que no requieren Windows host de script, [vea Windows Herramientas de desarrollo del instalador .](windows-installer-development-tools.md)

 

 



