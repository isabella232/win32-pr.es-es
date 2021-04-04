---
description: No es posible eliminar todas las circunstancias en las que la aplicación de una revisión puede requerir acceso al origen de instalación original.
ms.assetid: f7028c55-e4a5-4596-af7a-728c9f4f367e
title: Impedir que una revisión requiera acceso al origen de instalación original
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baee8b261ff0a3f6bb94fb141ee765726ffa2ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909005"
---
# <a name="preventing-a-patch-from-requiring-access-to-the-original-installation-source"></a>Impedir que una revisión requiera acceso al origen de instalación original

No es posible eliminar todas las circunstancias en las que la aplicación de una revisión puede requerir acceso al origen de instalación original.

Siga los puntos que se indican a continuación para minimizar la posibilidad de que la revisión requiera acceso al origen original:

-   Usar revisiones solo de archivo completo. Esto elimina la necesidad de crear revisiones binarias para todas las versiones publicadas anteriormente del archivo. Tenga en cuenta que las revisiones de archivo completas suelen tener un tamaño mayor que las revisiones binarias. Puede establecer fácilmente una revisión para que sea una revisión de archivo completa mediante la creación de la propiedad IncludeWholeFilesOnly con un valor de 1 (uno) en el archivo de las propiedades de creación de revisiones (PCP).
-   Asegúrese de que ninguna de las acciones personalizadas tenga acceso a la ubicación de origen original.
-   Asegúrese de que la acción ResolveSource esté condicional para que solo se ejecute cuando sea necesario, o bien no esté presente en absoluto.
-   Rellene la [tabla MsiFileHash](msifilehash-table.md) para todos los archivos que no tienen versiones. La herramienta Windows Installer SDK, Msifiler.exe, puede hacerlo fácilmente.
-   Asegúrese de que todos los archivos tengan la información de idioma y la versión correctas. La herramienta Windows Installer SDK, Msifiler.exe, puede hacerlo fácilmente.

## <a name="source-requirements-when-patching"></a>Requisitos de origen al aplicar revisiones

Es posible que sea necesario tener acceso a los orígenes de instalación originales para aplicar la revisión en los casos siguientes:

-   La revisión se aplica a una característica que se ejecuta actualmente desde el origen. En este caso, la característica pasa del estado de origen de ejecución al estado local.
-   La revisión se aplica a un componente que tiene un archivo que falta o que está dañado.
-   La revisión se aplica a un archivo de un componente que también contiene archivos sin versión sin entradas MsiFileHash. Se necesita una [tabla MsiFileHash](msifilehash-table.md) rellenada para evitar que se vuelvan a copiar innecesariamente los archivos que no tienen versiones desde la ubicación de origen.
-   La revisión se aplicó con un REINSTALLMODE de AMUS o emus. Esta opción es peligrosa porque realiza operaciones de copia de archivos independientemente de la versión del archivo. Esto puede dar lugar a inreving de archivos y casi siempre requiere el origen. El valor de REINSTALLMODE recomendado es OMUs.
-   Falta el paquete en caché para el producto. El paquete almacenado en caché es necesario para la aplicación de una revisión. El paquete almacenado en caché se almacena en la carpeta% WINDIR% \\ Installer.
-   El paquete se crea para hacer una llamada a la [acción ResolveSource](resolvesource-action.md). Por lo general, esta acción debe evitarse o aplicarse condicionalmente, porque su ejecución siempre produce un acceso al origen.
-   El paquete tiene una acción personalizada que intenta tener acceso al origen de alguna manera. El ejemplo más común es una acción personalizada de tipo 23 instalación simultánea.
    > [!Note]  
    > No se recomiendan instalaciones simultáneas para la instalación de aplicaciones destinadas a publicarse en el público. Para obtener información acerca de las instalaciones simultáneas, consulte [instalaciones](concurrent-installations.md)simultáneas.

     

-   El paquete de revisión consta de revisiones binarias que no se aplican a la versión actual del archivo en el equipo.

Considere el ejemplo siguiente, donde Windows Installer requiere acceso al origen original al aplicar una revisión:

1.  Instale la versión RTM del ejemplo del producto.
2.  Aplique la revisión Qfe1. MSP al equipo. Esta versión de revisión 1,0 de Example.dll a la versión 1,1.
3.  Se proporciona una nueva revisión, Qfe2. MSP, que actualiza Example.dll a la versión 1,2 y que Qfe1. MSP está obsoleto. Sin embargo, la revisión solo se creó para tener como destino la versión 1,0 de Example.dll porque se generó con la versión RTM del producto. Example.dll versión 1,2 incluye la corrección incluida en Example.dll versión 1,1, pero se generó el archivo. MSP entre las imágenes RTM y QFE2. Por lo tanto, cuando se aplica Qfe2. MSP al equipo, Windows Installer necesita tener acceso al origen original. La revisión binaria de Example.dll no se puede aplicar a la versión 1,1; solo se puede aplicar a la versión 1,0. Como resultado, el instalador vuelve a copiar la versión 1,0 de Example.dll desde la ubicación de origen original para que la revisión se pueda aplicar correctamente.

## <a name="source-requirements-when-removing-a-patch"></a>Requisitos de origen al quitar una revisión

Es posible que sea necesario tener acceso a los orígenes de instalación originales para quitar una revisión si el Windows Installer no ha almacenado la información de línea de base de la revisión. A partir de Windows Installer 3,0, el instalador guarda selectivamente la información de línea de base de los archivos cuando se actualizan. Para obtener más información acerca de la caché de línea de base, consulte [reducir el tamaño](reducing-patch-size.md) de la revisión.

 

 



