---
description: La utilidad de comprobación de archivos del sistema, Sfc.exe, permite a los administradores examinar todos los recursos protegidos para comprobar sus versiones.
ms.assetid: 72f69ad2-15d9-4191-a8aa-4c23a2392006
title: Comprobador de archivos de sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4e0d67f6de6aba62fe262969d7f30db0c45335
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249470"
---
# <a name="system-file-checker"></a>Comprobador de archivos de sistema

La utilidad de comprobación de archivos del sistema, Sfc.exe, permite a los administradores examinar todos los recursos protegidos para comprobar sus versiones.

Los archivos críticos para reiniciar Windows que no coincidan con la versión Windows esperada se pueden reemplazar por las versiones correctas. Si se repara un archivo, también se repararán los datos del Registro correspondientes. Los archivos protegidos no son críticos para Windows no se reparan.

## <a name="syntax"></a>Sintaxis

A continuación se muestra la sintaxis de la línea de comandos para Sfc.

**Opciones de SFC \[ =ruta de acceso de archivo completa\]**

## <a name="options"></a>Opciones

<dl> <dt>

<span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE=*x*
</dt> <dd>

Este valor no se admite.

**Windows Server 2003 y Windows XP:** Establece el tamaño de la caché de archivos. El tamaño predeterminado de la memoria caché es 0x32 (50 MB).

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

Compruebe o repare solo los archivos. No compruebe ni repare las claves del Registro.

**Windows XP:** No se admite.

</dd> <dt>

<span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR
</dt> <dd>

Use esta opción para reparaciones sin conexión. Especifique la ubicación del directorio de arranque sin conexión.

**Windows XP:** No se admite.

</dd> <dt>

<span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR
</dt> <dd>

Use esta opción para reparaciones sin conexión. Especifique la ubicación del directorio de Windows sin conexión.

**Windows XP:** No se admite.

</dd> <dt>

<span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE
</dt> <dd>

Este valor no se admite.

**Windows Server 2003 y Windows XP:** Vacía la caché de archivos y examina todos los archivos del sistema protegidos.

</dd> <dt>

<span id="_QUIET"></span><span id="_quiet"></span>/QUIET
</dt> <dd>

Este valor no se admite.

</dd> <dt>

<span id="_REVERT"></span><span id="_revert"></span>/REVERT
</dt> <dd>

Vuelva a la configuración predeterminada.

**Windows Server 2008 y Windows Vista:** No se admite.

</dd> <dt>

<span id="_SCANBOOT"></span><span id="_scanboot"></span>/SCANBOOT
</dt> <dd>

Este valor no se admite.

**Windows Server 2003 y Windows XP:** Examina todos los archivos del sistema protegidos en cada arranque.

</dd> <dt>

<span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE
</dt> <dd>

Examina y repara el archivo ubicado en la ruta de acceso completa especificada.

**Windows XP:** No se admite.

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

**Windows XP:** No se admite.

</dd> <dt>

<span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY
</dt> <dd>

Examina todos los archivos del sistema protegidos, pero no los repara.

**Windows XP:** No se admite.

</dd> </dl>

Sfc establece el siguiente valor del Registro:

 = HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Winlogon \\ SFCScan

Para obtener más información, vea [Valores del Registro WFP](wfp-registry-values.md).

## <a name="remarks"></a>Observaciones

Solo Windows Vista, puede establecer la variable de entorno **\_ \_ LOGFILE** de SEGUIMIENTO DE WINDOWS en la ubicación de un directorio válido para recibir un archivo de registro.

## <a name="examples"></a>Ejemplos

Las siguientes líneas de comandos de ejemplo son ejemplos de sfc.exe sintaxis.

**sfc /SCANNOW**

**sfc /VERIFYFILE=c: \\ windows \\ system32 \\kernel32.dll**

**sfc /SCANFILE=d: \\ windows \\ system32 \\kernel32.dll /OFFBOOTDIR=d: \\ /OFFWINDIR=d: \\ windows**

**sfc /VERIFYONLY /FILESONLY**

 

 



