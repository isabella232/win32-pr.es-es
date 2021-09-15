---
description: Windows Protección de recursos (WRP) impide el reemplazo de archivos esenciales del sistema, carpetas y claves del Registro que se instalan como parte de Windows Vista o Windows Server 2008.
ms.assetid: 1cb67b4a-dc75-4bd7-b314-d695c10d5558
title: Detección de reemplazo de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62dc1855b98ca5834ef9e13e2f48bf7cca492e94
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360554"
---
# <a name="detecting-resource-replacement"></a>Detección de reemplazo de recursos

Windows Protección de recursos (WRP) impide el reemplazo de archivos esenciales del sistema, carpetas y claves del Registro que se instalan como parte de Windows Vista o Windows Server 2008.

WRP protege archivos, carpetas y claves del Registro en Windows Vista o Windows Server 2008 al detectar e impedir intentos de reemplazar recursos protegidos. Esta protección se basa en una Windows de control de acceso discrecional (DACL) y listas de control de acceso (ACL) definidas para los recursos protegidos. El permiso para el acceso completo para modificar recursos protegidos por WRP está restringido a TrustedInstaller. Los recursos protegidos con WRP solo se pueden cambiar mediante los mecanismos de reemplazo de recursos admitidos con el Windows Instalador de [módulos](supported-file-replacement-mechanisms.md) de almacenamiento. Las aplicaciones que intentan modificar un recurso protegido por WRP nunca cambian el recurso y pueden recibir un mensaje de error que indica que se denegó el acceso al recurso.

Las aplicaciones e instaladores pueden usar las funciones [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) y [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) para determinar si un archivo o clave del Registro está protegido.

**Windows Server 2003 y Windows XP: **

Windows La protección de archivos (WFP) protege los archivos del sistema mediante la detección de intentos de reemplazar archivos del sistema protegidos. Esta protección se desencadena después de que WFP reciba una notificación de cambio de directorio para un archivo en un directorio protegido. Cuando WFP recibe esta notificación, determina qué archivo ha cambiado. Si el archivo está protegido, WFP busca la firma de archivo en un archivo de catálogo para determinar si el nuevo archivo es la versión correcta. Si la versión del archivo no es correcta, el sistema reemplaza el archivo por la versión correcta de la caché o del medio de distribución, en función de si el archivo se encuentra en la memoria caché. WFP busca el archivo correcto en el orden siguiente:

1.  Busque en el directorio de caché.
2.  Busque la ruta de acceso de instalación de red si el sistema se instaló mediante la instalación de red.
3.  Busque en un Windows CD-ROM, si el sistema se instaló desde CD-ROM.

Si WFP no encuentra automáticamente el archivo en las dos primeras ubicaciones, muestra el mensaje siguiente:

![Mensaje wfp que se muestra cuando no se encuentra el archivo en el directorio de caché o la ruta de instalación de red](images/wfp-1.png)

Si el sistema se instaló mediante un CD-ROM, WFP muestra el mensaje siguiente:

![Mensaje de wfp que se muestra para solicitar al usuario que inserte windows cd-rom](images/wfp-2.png)

Si un administrador no ha iniciado sesión, WFP no puede mostrar ninguno de estos cuadros de diálogo. WFP mostrará el cuadro de diálogo después de que un administrador inicie sesión.

WFP también registra el intento de reemplazo de archivos en el registro de eventos del sistema. Si el administrador canceló la restauración del archivo correcto, WFP registra la cancelación.

## <a name="retrieving-the-list-of-protected-files"></a>Recuperar la lista de archivos protegidos

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



 

 



