---
description: Lista de recursos protegidos
ms.assetid: 70413c13-3db0-4af0-b584-259cce70f084
title: Lista de recursos protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c221068d9185c289d601f53c6b76df9677d8bc213b44f3dc13dbf5b66a0df446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760125"
---
# <a name="protected-resource-list"></a>Lista de recursos protegidos

El permiso para el acceso completo para modificar recursos protegidos con WRP está restringido a TrustedInstaller. Los recursos protegidos con WRP solo se pueden cambiar mediante los mecanismos de reemplazo de recursos [admitidos](supported-file-replacement-mechanisms.md) con Windows Instalador de módulos.

WRP protege los archivos con las siguientes extensiones instaladas por Windows Server 2008 o Windows Vista: .dll, .exe, .ocx y .sys.

WRP protege los archivos críticos instalados por Windows Server 2008 o Windows Vista con las siguientes extensiones: .acm, .ade, .adp, .app, .asa, .asp, .aspx, .ax, .bas, .bat, .bin, .cer, .chm, .clb, .cmd, .cnt, .cnv, .com, .cpl, .cpx, .cpx, .crt, .csh, .dll, .drv, .dtd, .exe, .fxp, .grp, .h1s, .hlp, .hta, .ime, .inf, .ins, .isp, .its, .js, .jse, .ksh, .lnk, .mad, .maf, .mag, .mam, .man, .maq, .mar, .mar, .mas, .mat, .mau, .mav, .maw, .mda, .mdb, .mde, .mdt, .mdw, .mdz, .msc, .msi, .msp, .mst, .daemon, .nls, .ocx, .ops, .pal, .pcd, .pif, .prf, .prg, .pst, .reg, .scf, .scr, .sct, .shb, .shs, .sys, .tlb, .tsp, .url, .vb, .vbe, .vbs, .vsmacros, .vss, .vst, .vsw, .ws, .wsc, .wsf, .wsh,  .xsd y .xsl.

WRP protege las carpetas críticas. Una carpeta que contiene solo archivos protegidos por WRP puede bloquearse para que solo el instalador de confianza Windows pueda crear archivos o subcarpetas en la carpeta. Una carpeta puede estar parcialmente bloqueada para permitir que los administradores creen archivos y subcarpetas en la carpeta.

WRP protege las claves esenciales del Registro instaladas por Windows Server 2008 y Windows Vista. Si una clave está protegida por WRP, se pueden proteger todas sus subclaves y valores.

WRP copia los archivos necesarios para reiniciar  Windows en el directorio de caché ubicado en %Windir% \\ winsxs \\ Backup. Los archivos críticos que no son necesarios para reiniciar Windows no se copian en el directorio de caché. El tamaño del directorio de caché y la lista de archivos copiados en la memoria caché no se pueden modificar.

**Windows Server 2003 y Windows XP: **

Windows Protección de archivos (WFP) precedido por WRP.

WFP protege los archivos instalados por Windows con las siguientes extensiones: .dll, .exe, .ocx y .sys. Además, las fuentes TrueType Micross.ttf, Holooma.ttf y Holoomabd.ttf también están protegidas.

Al final de la instalación Windows, WFP ejecuta un examen de todos los archivos protegidos para asegurarse de que no se han modificado por las aplicaciones instaladas a través de la instalación desatendida. WFP también copia las versiones comprobadas de estos archivos del sistema en el directorio de caché. Cuando una aplicación intenta reemplazar un archivo protegido, WFP puede restaurar el archivo original desde el directorio de caché.

El valor predeterminado es %systemroot% \\ system32 \\ dllcache. Para especificar una ubicación diferente para la caché, cree el siguiente valor del Registro: **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Winlogon \\ SFCDllCacheDir**

Debe ser una ruta de acceso local. El uso de una ruta de acceso de red crea un único origen de red compartido para los archivos de caché, siempre que todos los clientes que usan el recurso compartido ejecuten los mismos Service Pack y revisiones.

El tamaño predeterminado de la memoria caché es ilimitado. Para cambiar el tamaño de la memoria caché, use la siguiente configuración del Registro: **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Winlogon \\ SFCQuota**

Si el valor es SFC QUOTA ALL FILES, todos los archivos del sistema se almacenarán en \_ caché en el directorio de \_ \_ caché.

Debido a las consideraciones de espacio en disco, puede que no sea conveniente mantener las versiones almacenadas en caché de todos los archivos del sistema en el directorio de caché. Según el tamaño de la memoria caché, WFP almacenará las versiones de archivo comprobadas en el directorio de caché en la unidad de disco duro del sistema. WFP agregará archivos a la memoria caché hasta que el tamaño del directorio de caché alcance el límite especificado.

Cuando una aplicación intenta reemplazar un archivo protegido que no está en la memoria caché, WFP intenta restaurar el archivo original desde el origen de instalación, solicitando al usuario si es necesario.

 

 



