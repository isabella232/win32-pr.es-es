---
description: La utilidad comprobador de archivos de sistema, Sfc.exe, permite a los administradores analizar todos los recursos protegidos para comprobar sus versiones.
ms.assetid: 72f69ad2-15d9-4191-a8aa-4c23a2392006
title: Comprobador de archivos de sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4e0d67f6de6aba62fe262969d7f30db0c45335
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669813"
---
# <a name="system-file-checker"></a>Comprobador de archivos de sistema

La utilidad comprobador de archivos de sistema, Sfc.exe, permite a los administradores analizar todos los recursos protegidos para comprobar sus versiones.

Los archivos críticos para reiniciar Windows que no coinciden con la versión de Windows esperada pueden reemplazarse por las versiones correctas. Si se repara un archivo, también se reparan los datos del registro correspondientes. Los archivos protegidos no críticos para reiniciar Windows no se reparan.

## <a name="syntax"></a>Sintaxis

A continuación se muestra la sintaxis de línea de comandos para SFC.

**Opciones de SFC \[ = ruta de acceso completa del archivo\]**

## <a name="options"></a>Opciones

<dl> <dt>

<span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE =*x*
</dt> <dd>

Este valor no se admite.

**Windows Server 2003 y Windows XP:** Establece el tamaño de la caché de archivos. El tamaño predeterminado de la memoria caché es de 50 MB.

</dd> <dt>

<span id="_CANCEL"></span><span id="_cancel"></span>/CANCEL
</dt> <dd>

Este valor no se admite.

</dd> <dt>

<span id="_ENABLE"></span><span id="_enable"></span>/ENABLE
</dt> <dd>

Este valor no se admite.

</dd> <dt>

<span id="_FILESONLY"></span><span id="_filesonly"></span>/FILESONLY
</dt> <dd>

Comprobar o reparar solo archivos. No Compruebe ni repare las claves del registro.

**Windows XP:** No compatible.

</dd> <dt>

<span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR
</dt> <dd>

Use esta opción para las reparaciones sin conexión. Especifique la ubicación del directorio de arranque sin conexión.

**Windows XP:** No compatible.

</dd> <dt>

<span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR
</dt> <dd>

Use esta opción para las reparaciones sin conexión. Especifique la ubicación del directorio de Windows sin conexión.

**Windows XP:** No compatible.

</dd> <dt>

<span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE
</dt> <dd>

Este valor no se admite.

**Windows Server 2003 y Windows XP:** Vacía la memoria caché de archivos y examina todos los archivos del sistema protegidos.

</dd> <dt>

<span id="_QUIET"></span><span id="_quiet"></span>/QUIET
</dt> <dd>

Este valor no se admite.

</dd> <dt>

<span id="_REVERT"></span><span id="_revert"></span>/REVERT
</dt> <dd>

Vuelva a la configuración predeterminada.

**Windows Server 2008 y Windows Vista:** No compatible.

</dd> <dt>

<span id="_SCANBOOT"></span><span id="_scanboot"></span>/SCANBOOT
</dt> <dd>

Este valor no se admite.

**Windows Server 2003 y Windows XP:** Examina todos los archivos del sistema protegidos en cada arranque.

</dd> <dt>

<span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE
</dt> <dd>

Examina y repara el archivo que se encuentra en la ruta de acceso completa especificada.

**Windows XP:** No compatible.

</dd> <dt>

<span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW
</dt> <dd>

Examina todos los archivos del sistema protegidos inmediatamente.

</dd> <dt>

<span id="_SCANONCE"></span><span id="_scanonce"></span>/SCANONCE
</dt> <dd>

Este valor no se admite.

**Windows Server 2003 y Windows XP:** Examina todos los archivos del sistema protegidos en el siguiente arranque.

</dd> <dt>

<span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE
</dt> <dd>

Comprueba el archivo en la ruta de acceso completa especificada. Esta opción no repara el archivo.

**Windows XP:** No compatible.

</dd> <dt>

<span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY
</dt> <dd>

Examina todos los archivos del sistema protegidos, pero no repara los archivos.

**Windows XP:** No compatible.

</dd> </dl>

SFC establece el siguiente valor del registro:

 = HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCScan

Para obtener más información, consulte [valores del registro de WFP](wfp-registry-values.md).

## <a name="remarks"></a>Observaciones

En Windows Vista únicamente, puede establecer la variable de entorno de **\_ \_ registro de seguimiento de Windows** en la ubicación de un directorio válido para recibir un archivo de registro.

## <a name="examples"></a>Ejemplos

Las siguientes líneas de comandos de ejemplo son ejemplos de sintaxis sfc.exe.

**SFC/SCANNOW**

**SFC/VERIFYFILE = c: \\ Windows \\ system32 \\kernel32.dll**

**SFC/SCANFILE = d: \\ Windows \\ system32 \\kernel32.dll/OFFBOOTDIR = d: \\ /OFFWINDIR = d: \\ Windows**

**/VERIFYONLY de SFC/FILESONLY**

 

 



