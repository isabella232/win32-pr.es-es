---
description: Lista de recursos protegidos
ms.assetid: 70413c13-3db0-4af0-b584-259cce70f084
title: Lista de recursos protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 316a9bf9233283a7c0aba11f0d5fe8a09f38f1e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279126"
---
# <a name="protected-resource-list"></a>Lista de recursos protegidos

El permiso para el acceso completo para modificar los recursos protegidos por WRP está restringido a TrustedInstaller. Los recursos protegidos por WRP solo pueden cambiarse mediante los [mecanismos de sustitución de recursos compatibles](supported-file-replacement-mechanisms.md) con el servicio de instalador de módulos de Windows.

WRP protege los archivos con las siguientes extensiones instaladas por Windows Server 2008 o Windows Vista:. dll,. exe,. ocx y. sys.

WRP protege los archivos críticos instalados por Windows Server 2008 o Windows Vista con las siguientes extensiones:. ACM,. ADE,. ADP,. app,. asa,. asp,. aspx,. AX,. Bas,. bat,. bin,. cer,. chm,. CLB,. cmd,. CNT,. CNV,. com,. cpl,. CPX,. CRT,. CSH,. dll,. drv,. DTD,. exe,. fxp,. GRP,. H1S,. HLP,. HTA,. IME,. inf,. ins,. ISP,. su,. js,. JSE,. ksh,. lnk,. Mad,. MAF,. ,. MAM,. Man,. MAQ,. mar,. mas,. MAT,. Mau,. MAV,. Maw,. MDA,. mdb,. MDE,. MDT,. mdw,. MDZ,. msc,. msi,. MSP,. MST,. MUI,. NLS,. ocx,. OPS,. PAL,. PCD,. PIF,. PRG,. pst,. reg,. SCF,. SCR,. SCT,. SHB,. SHS,. sys,. tlb,. TSP,. URL,. VB,. VBE,. vbs,. VSMacros,. VSS,. VST,. VSW,. ws,. WSC,.,. WSH,. xsd y. Xsl.

WRP protege las carpetas críticas. Una carpeta que solo contiene archivos protegidos por WRP puede estar bloqueada para que solo el instalador de confianza de Windows pueda crear archivos o subcarpetas en la carpeta. Una carpeta puede estar parcialmente bloqueada para permitir que los administradores creen archivos y subcarpetas en la carpeta.

WRP protege las claves del registro esenciales instaladas por Windows Server 2008 y Windows Vista. Si una clave está protegida por WRP, se pueden proteger todas sus subclaves y valores.

WRP copia los archivos necesarios para reiniciar Windows en el *Directorio de caché* que se encuentra en% WINDIR% \\ WinSxS \\ backup. Los archivos críticos que no son necesarios para reiniciar Windows no se copian en el directorio de caché. El tamaño del directorio de caché y la lista de archivos copiados en la memoria caché no se pueden modificar.

* * Windows Server 2003 y Windows XP: * *

Protección de archivos de Windows (WFP) precedía a WRP.

WFP protege los archivos que instala Windows con las siguientes extensiones:. dll,. exe,. ocx y. sys. Además, las fuentes TrueType Micross. ttf, Tahoma. ttf y Tahomabd. ttf también están protegidas.

Al final de la instalación de Windows, WFP ejecuta un examen de todos los archivos protegidos para asegurarse de que no hayan sido modificados por las aplicaciones instaladas a través de la instalación desatendida. WFP también copia las versiones comprobadas de estos archivos del sistema en el directorio de caché. Cuando una aplicación intenta reemplazar un archivo protegido, WFP puede restaurar el archivo original desde el directorio de caché.

El valor predeterminado es% SystemRoot% \\ system32 \\ dllcache. Para especificar una ubicación diferente para la memoria caché, cree el siguiente valor del registro: **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCDllCacheDir**

Debe ser una ruta de acceso local. El uso de una ruta de acceso de red crea un único origen de red compartido para los archivos de caché, siempre que todos los clientes que usen el recurso compartido ejecuten los mismos Service Packs y revisiones.

El tamaño predeterminado de la memoria caché es ilimitado. Para cambiar el tamaño de la memoria caché, use la siguiente configuración del registro: **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCQuota**

Si el valor es SFC \_ quota \_ All \_ files, todos los archivos del sistema se almacenarán en caché en el directorio de caché.

Debido a las consideraciones de espacio en disco, puede que no sea conveniente mantener las versiones almacenadas en caché de todos los archivos del sistema en el directorio de caché. En función del tamaño de la memoria caché, WFP almacenará las versiones de archivo comprobadas en el directorio de caché del disco duro del sistema. WFP agregará archivos a la memoria caché hasta que el tamaño del directorio de la caché alcance el límite especificado.

Cuando una aplicación intenta reemplazar un archivo protegido que no está en la memoria caché, WFP intenta restaurar el archivo original desde el origen de instalación, solicitando al usuario si es necesario.

 

 



