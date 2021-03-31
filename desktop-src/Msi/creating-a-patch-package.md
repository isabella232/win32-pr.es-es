---
description: Los desarrolladores crean un paquete de revisión generando un archivo de creación de revisiones y usando Msimsp.exe para llamar a la función UiCreatePatchPackageEx en Patchwiz.dll.
ms.assetid: 8a163653-6ba1-46ea-9832-f998749d29ae
title: Crear un paquete de revisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2561cb6729dc7b4e0e48acd13b6338f08a8ba943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277185"
---
# <a name="creating-a-patch-package"></a>Crear un paquete de revisión

Los desarrolladores crean un paquete de revisión generando un archivo de creación de revisiones y usando [Msimsp.exe](msimsp-exe.md) para llamar a la función [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) en [Patchwiz.dll](patchwiz-dll.md). En el SDK de Windows Installer se proporcionan Msimsp.exe y Patchwiz.dll. Para obtener más información, vea [un pequeño ejemplo de revisión de actualización](a-small-update-patching-example.md).

Dado que la aplicación de una revisión a un paquete de Windows Installer da como resultado la instalación de los orígenes originales con un nuevo archivo. msi, el nuevo archivo. msi debe ser compatible con el diseño del origen original.

Cuando cree un paquete de revisión, debe utilizar una imagen de instalación sin comprimir para crear una revisión, por ejemplo, una imagen administrativa o una imagen de instalación sin comprimir de un CD-ROM. También debe cumplir las restricciones siguientes:

-   No mueva archivos de una carpeta a otra.
-   No mueva archivos de un archivo. cab a otro.
-   No cambie el orden de los archivos en un archivo. cab.
-   No cambie el número de secuencia de los archivos existentes. El número de secuencia es el valor especificado en la columna Sequence de la [tabla File](file-table.md).
-   Los archivos nuevos que agregue la revisión deben colocarse al final de la secuencia de archivos existente. El número de secuencia de cualquier archivo nuevo en la imagen actualizada debe ser mayor que el número de secuencia más grande de los archivos existentes en la imagen de destino.
-   No cambie las claves principales de la [tabla de archivos](file-table.md) entre las versiones originales y nuevas del archivo. msi.
    > [!Note]  
    > El archivo debe tener la misma clave en la [tabla de archivos](file-table.md) de la imagen de destino y la imagen actualizada. Los valores de cadena de la columna de archivo de ambas tablas deben ser idénticos, incluido el caso.

     

-   No cree un paquete con claves de [tabla de archivos](file-table.md) que solo difieran en caso de que, por ejemplo, evite el siguiente ejemplo de tabla.

    

    | Archivo       | Componente\_ | FileName   |
    |------------|-------------|------------|
    | readme.txt | Comp1       | readme.txt |
    | ReadMe.txt | Comp2       | readme.txt |

    

     

    El Windows Installer puede permitir el ejemplo de tabla anterior cuando Comp1 y Comp2 se instalan en directorios diferentes, pero no puede usar [Msimsp.exe](msimsp-exe.md) o [Patchwiz.dll](patchwiz-dll.md) para generar una revisión para el paquete. Msimsp.exe y Patchwiz.dll llaman a Makecab.exe, que distingue entre mayúsculas y minúsculas y produce un error.

    Al usar módulos de fusión mediante combinación en el programa de instalación, asegúrese de que los números de secuencia de archivos y el diseño cumplen las instrucciones anteriores.

 

 



