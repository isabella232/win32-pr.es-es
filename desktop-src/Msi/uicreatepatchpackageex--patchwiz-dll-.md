---
description: La función UiCreatePatchPackageEx toma un archivo de creación de paquetes (archivo .msp) y genera un paquete de revisión Windows Installer (paquete .msp). Llamar Msimsp.exe es el método recomendado para usar Patchwiz.dll.
ms.assetid: 76d9a21d-73bc-41fc-8ed0-7d7d7deff815
title: UiCreatePatchPackageEx (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac61371d1e7bf1809880c8f10a403d1730adc8e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071822"
---
# <a name="uicreatepatchpackageex-patchwizdll"></a>UiCreatePatchPackageEx (Patchwiz.dll)

La función UiCreatePatchPackageEx toma un archivo de creación de paquetes (archivo .msp) y genera un paquete de revisión Windows Installer (paquete .msp). Llamar [Msimsp.exe](msimsp-exe.md) es el método recomendado para usar [Patchwiz.dll](patchwiz-dll.md).

La función UiCreatePatchPackageEx está disponible a partir de Patchwiz.dll versión 4.0 y amplía la funcionalidad de la función [UiCreatePatchPackage.](uicreatepatchpackage-patchwiz-dll-.md)

``` syntax
UINT UiCreatePatchPackageEx(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  BOOL fRemoveTempFolderContents,
  DWORD dwFlags,
  DWORD dwReserved    
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*
</dt> <dd>

Ruta de acceso completa al archivo de propiedades de creación de revisiones (archivo .csv) para esta revisión.

</dd> <dt>

<span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*
</dt> <dd>

Ruta de acceso completa al Windows de revisión del instalador (archivo .msp) que se va a crear. Este parámetro puede ser **NULL** o una cadena vacía, pero no se puede omitir. Si es **NULL o** una cadena vacía, la función usa el valor de PatchOutputPath en la tabla properties [(Patchwiz.dll).](properties-table-patchwiz-dll-.md)

</dd> <dt>

<span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*
</dt> <dd>

Ruta de acceso completa a un archivo de registro de texto que se anexará. Este parámetro puede ser **NULL** o una cadena vacía, pero no se puede omitir.

</dd> <dt>

<span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*
</dt> <dd>

Identificador de una ventana que muestra el texto de estado. Este parámetro puede ser **NULL** o una cadena vacía, pero no se puede omitir.

</dd> <dt>

<span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*
</dt> <dd>

Ubicación de los archivos temporales. Este parámetro puede ser **NULL** o una cadena vacía, pero no se puede omitir. El usuario debe tener privilegios suficientes para leer y escribir en esta carpeta. La ubicación predeterminada es %TMP% \\ ~pcw \_ tmp.tmp \\ .

</dd> <dt>

<span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*
</dt> <dd>

Si **es TRUE,** quite la carpeta temporal y todo su contenido si está presente. Si **false** y la carpeta están presentes, se produce un error en la función.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

Este parámetro se puede establecer en uno o una combinación de los siguientes valores para especificar opciones de registro o interfaz de usuario.



| Marca            | Value       | Significado                                  |
|-----------------|-------------|------------------------------------------|
| LOGNONE         | 0x00000000  | No escriba ningún mensaje en el registro.            |
| LOGINFO         | 0x00000001  | Escriba mensajes informativos en el registro. |
| LOGWARN         | 0x00000002  | Escriba advertencias en el registro.               |
| LOGERR          | 0x00000004  | Escriba mensajes de error en el registro.         |
| LOGPERFMESSAGES | 0x00000008  | Escriba mensajes de rendimiento en el registro.   |
| UINONE          | 0x00000000f | No muestre la interfaz de usuario.       |
| UIALL           | 0x00000010  | Muestra la interfaz de usuario.              |



 

</dd> <dt>

<span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*dwReserved*
</dt> <dd>

Reservado. Este parámetro debe establecerse en cero.

</dd> </dl>

## <a name="return-values"></a>Valores devueltos

Vea la tabla en [Valores devueltos para UiCreatePatchPackage.](return-values-for-uicreatepatchpackage.md)

## <a name="remarks"></a>Observaciones

Para obtener un ejemplo de creación de un archivo .msi y el uso de [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) para generar un paquete de revisión de Windows Installer, vea la sección [A Small Update Patching Example](a-small-update-patching-example.md).

La creación de una revisión requiere una imagen de instalación sin comprimir, como una imagen administrativa o una imagen de instalación sin comprimir de un CD-ROM. [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) no genera revisiones binarias para los archivos de los archivadores.

 

 



