---
description: Los desarrolladores crean un paquete de revisión generando un archivo de creación de revisiones y Msimsp.exe para llamar a la función UiCreatePatchPackageEx en Patchwiz.dll.
ms.assetid: 8a163653-6ba1-46ea-9832-f998749d29ae
title: Crear un paquete de revisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2561cb6729dc7b4e0e48acd13b6338f08a8ba943
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158731"
---
# <a name="creating-a-patch-package"></a>Crear un paquete de revisión

Los desarrolladores crean un paquete de revisión generando un archivo de creación de revisiones yMsimsp.exepara llamar a la función [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) [enPatchwiz.dll](patchwiz-dll.md). [](msimsp-exe.md) Msimsp.exe y Patchwiz.dll se proporcionan en el SDK Windows Installer. Para obtener más información, vea [A Small Update Patching Example](a-small-update-patching-example.md).

Dado que la aplicación de una revisión a un paquete del instalador de Windows da como resultado la instalación de los orígenes originales mediante un nuevo archivo .msi, el nuevo archivo .msi debe seguir siendo compatible con el diseño del origen original.

Al crear un paquete de revisión, debe usar una imagen de instalación sin comprimir para crear una revisión, por ejemplo, una imagen administrativa o una imagen de instalación sin comprimir desde un CD-ROM. También debe cumplir las restricciones siguientes:

-   No mueva archivos de una carpeta a otra.
-   No mueva archivos de un gabinete a otro.
-   No cambie el orden de los archivos en un gabinete.
-   No cambie el número de secuencia de los archivos existentes. El número de secuencia es el valor especificado en la columna Secuencia de la [tabla de archivos](file-table.md).
-   Los nuevos archivos agregados por la revisión deben colocarse al final de la secuencia de archivos existente. El número de secuencia de cualquier archivo nuevo de la imagen actualizada debe ser mayor que el número de secuencia más grande de archivos existentes en la imagen de destino.
-   No cambie las claves principales de la tabla [de archivos](file-table.md) entre el archivo original y el nuevo .msi de archivos.
    > [!Note]  
    > El archivo debe tener la misma clave en la tabla [de archivos](file-table.md) de la imagen de destino y la imagen actualizada. Los valores de cadena de la columna Archivo de ambas tablas deben ser idénticos, incluido el caso.

     

-   No cree un paquete con claves [de tabla de](file-table.md) archivos que solo difieren en caso de que, por ejemplo, evite el siguiente ejemplo de tabla.

    

    | Archivo       | Componente\_ | FileName   |
    |------------|-------------|------------|
    | readme.txt | Comp1       | readme.txt |
    | ReadMe.txt | Comp2       | readme.txt |

    

     

    El instalador Windows puede permitir el ejemplo de tabla anterior cuando Comp1 y Comp2 están instalados en directorios diferentes, pero no puede usar [Msimsp.exe](msimsp-exe.md) [oPatchwiz.dll](patchwiz-dll.md) para generar una revisión para el paquete. Msimsp.exe y Patchwiz.dll a Makecab.exe, que no tiene en cuenta las mayúsculas y minúsculas y genera un error.

    Al usar módulos de combinación en la instalación, asegúrese de que los números de secuencia de archivos y el diseño cumplan las directrices anteriores.

 

 



