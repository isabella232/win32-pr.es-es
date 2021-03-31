---
description: La función UiCreatePatchPackage toma un archivo de creación de paquetes (archivo. PCP) y genera un paquete de revisión de Windows Installer (paquete. msp).
ms.assetid: 77fedb80-b664-417d-879b-846e74cc4c23
title: UiCreatePatchPackage (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bcda07d74ffc32c76809037d9ac90cf11ea25c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907616"
---
# <a name="uicreatepatchpackage-patchwizdll"></a>UiCreatePatchPackage (Patchwiz.dll)

La función UiCreatePatchPackage toma un archivo de creación de paquetes (archivo. PCP) y genera un paquete de revisión de Windows Installer (paquete. msp). La llamada a [Msimsp.exe](msimsp-exe.md) es el método recomendado para utilizar [Patchwiz.dll](patchwiz-dll.md). La función [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) está disponible en la versión 4,0 de Patchwiz.dll y extiende la funcionalidad de la función UiCreatePatchPackage.

``` syntax
UINT UiCreatePatchPackage(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  Bool fRemoveTempFolderContents  
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*
</dt> <dd>

Ruta de acceso completa al archivo de propiedades de creación de revisiones (archivo. PCP) para esta revisión.

</dd> <dt>

<span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*
</dt> <dd>

Ruta de acceso completa al paquete de revisión de Windows Installer (archivo. msp) que se va a crear. Este parámetro puede ser **null** o una cadena vacía, pero no se puede omitir. Si es **null** o una cadena vacía, la función usa el valor de PatchOutputPath en la [tabla Properties (Patchwiz.dll)](properties-table-patchwiz-dll-.md).

</dd> <dt>

<span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*
</dt> <dd>

Ruta de acceso completa a un archivo de registro de texto que se va a anexar. Este parámetro puede ser **null** o una cadena vacía, pero no se puede omitir.

</dd> <dt>

<span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*
</dt> <dd>

Identificador de una ventana que muestra el texto de estado. Este parámetro puede ser **null** o una cadena vacía, pero no se puede omitir.

</dd> <dt>

<span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*
</dt> <dd>

Ubicación de los archivos temporales. Este parámetro puede ser **null** o una cadena vacía, pero no se puede omitir. La ubicación predeterminada es% TMP% \\ ~ PCW \_ tmp. tmp \\ .

</dd> <dt>

<span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*
</dt> <dd>

Si **es true**, quite la carpeta temporal y todo su contenido, si está presente. Si es **false** y la carpeta está presente, se produce un error en la función.

</dd> </dl>

## <a name="return-values"></a>Valores devueltos

Vea la tabla de [valores devueltos para UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).

## <a name="remarks"></a>Observaciones

Para obtener un ejemplo de creación de un archivo. PCP y el uso de UiCreatePatchPackage para generar un paquete de revisión de Windows Installer, vea la sección [un pequeño ejemplo de revisión de actualización](a-small-update-patching-example.md).

La creación de una revisión requiere una imagen de instalación sin comprimir, como una imagen administrativa o una imagen de instalación sin comprimir de un CD-ROM. UiCreatePatchPackage no genera revisiones binarias para los archivos de los archivadores.

 

 



