---
description: Protección de recursos de Windows (WRP) impide el reemplazo de archivos esenciales del sistema, carpetas y claves del registro que se instalan como parte de Windows Vista o Windows Server 2008.
ms.assetid: 1cb67b4a-dc75-4bd7-b314-d695c10d5558
title: Detección de reemplazo de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62dc1855b98ca5834ef9e13e2f48bf7cca492e94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817038"
---
# <a name="detecting-resource-replacement"></a>Detección de reemplazo de recursos

Protección de recursos de Windows (WRP) impide el reemplazo de archivos esenciales del sistema, carpetas y claves del registro que se instalan como parte de Windows Vista o Windows Server 2008.

WRP protege archivos, carpetas y claves del registro en Windows Vista o Windows Server 2008 detectando e impidiendo intentos de reemplazar recursos protegidos. Esta protección se basa en una lista de control de acceso discrecional (DACL) de Windows y en las listas de control de acceso (ACL) definidas para los recursos protegidos. El permiso para el acceso completo para modificar los recursos protegidos por WRP está restringido a TrustedInstaller. Los recursos protegidos por WRP solo pueden cambiarse mediante los [mecanismos de sustitución de recursos admitidos](supported-file-replacement-mechanisms.md) con el servicio de instalador de módulos de Windows. Las aplicaciones que intentan modificar un recurso protegido por WRP nunca cambian el recurso y pueden recibir un mensaje de error que indica que se denegó el acceso al recurso.

Las aplicaciones y los instaladores pueden usar las funciones [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) y [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) para determinar si un archivo o una clave del registro están protegidos.

* * Windows Server 2003 y Windows XP: * *

Protección de archivos de Windows (WFP) protege los archivos del sistema mediante la detección de intentos de reemplazar archivos del sistema protegidos. Esta protección se desencadena después de que WFP reciba una notificación de cambio de directorio para un archivo en un directorio protegido. Cuando WFP recibe esta notificación, determina qué archivo ha cambiado. Si el archivo está protegido, WFP busca la firma de archivo en un archivo de catálogo para determinar si el nuevo archivo es la versión correcta. Si la versión del archivo no es correcta, el sistema reemplaza el archivo con la versión correcta de la memoria caché o del medio de distribución, dependiendo de si el archivo se encuentra en la memoria caché. WFP busca el archivo correcto en el siguiente orden:

1.  Busque en el directorio de caché.
2.  Busque la ruta de instalación de red, si el sistema se instaló con la instalación de red.
3.  Busque en un CD-ROM de Windows si el sistema se instaló desde el CD-ROM.

Si WFP no puede encontrar automáticamente el archivo en las dos primeras ubicaciones, muestra el siguiente mensaje:

![mensaje de WFP mostrado cuando no se encuentra el archivo en el directorio de caché o la ruta de instalación de red](images/wfp-1.png)

Si el sistema se instaló con un CD-ROM, WFP muestra el siguiente mensaje:

![mensaje de WFP que se muestra para solicitar al usuario que inserte el CD-ROM de Windows](images/wfp-2.png)

Si un administrador no ha iniciado sesión, WFP no puede mostrar ninguno de estos cuadros de diálogo. WFP mostrará el cuadro de diálogo después de que un administrador inicie sesión.

WFP también registra el intento de reemplazo del archivo en el registro de eventos del sistema. Si el administrador canceló la restauración del archivo correcto, WFP registra la cancelación.

## <a name="retrieving-the-list-of-protected-files"></a>Recuperando la lista de archivos protegidos

En el ejemplo siguiente se muestra cómo las aplicaciones y los instaladores pueden usar la función [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) para obtener la lista completa de archivos protegidos.


```C++
#include <windows.h>
#include <sfc.h>
#include <stdio.h>

#pragma comment(lib, "sfc")

void wmain (int argc, WCHAR ** argv)
{  UNREFERENCED_PARAMETER(argc);    
   PROTECTED_FILE_DATA pfd = {0};
   BOOL fResult;

   wprintf (L"List of protected files:\n\n", argv[1]);

   while (FALSE != (fResult = SfcGetNextProtectedFile (NULL, &pfd)))
   {
      wprintf (L"   %lu   %s\n", pfd.FileNumber, pfd.FileName);
   }

   if (GetLastError() == ERROR_NO_MORE_FILES)
   {
      wprintf (L"\nAll %lu protected files listed\n", pfd.FileNumber);
   }
   else
   {
      wprintf (L"\nerror %lu: SfcGetNextProtectedFile() failed unexpectedly\n", GetLastError());
   }

}
```



 

 



