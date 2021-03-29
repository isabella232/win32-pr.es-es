---
title: Instalación del proveedor
description: El procedimiento para instalar el proveedor WMI de DNS es distinto en función de la versión de Windows en la que está instalado.
ms.assetid: 5f2bd11a-bc1d-4a43-92d4-26392d2504e7
keywords:
- Sistema de nombres de dominio, proveedor WMI, instalar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b1c9dbdaf6d3ad55247d0b978c0a422361a2f04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774184"
---
# <a name="installing-the-provider"></a>Instalación del proveedor

El procedimiento para instalar el proveedor WMI de DNS es distinto en función de la versión de Windows en la que está instalado. En el procedimiento siguiente se describe cómo instalar y configurar el proveedor WMI de DNS en Windows 2000. Para obtener el proveedor WMI de DNS para Windows 2000, descargue el siguiente archivo:

**ADVERTENCIA:** Los archivos del proveedor WMI de DNS no son intercambiables. Los servidores DNS de Windows 2000 requieren diferentes archivos y un procedimiento diferente que los servidores DNS de Windows Server 2003. Se proporciona el procedimiento para cada uno.

**Para instalar el proveedor WMI de DNS en el servidor de Windows 2000**

1.  Obtenga el proveedor WMI de DNS para Windows 2000 del kit de recursos del servidor de Windows 2000 o descargue el archivo, Dnsprov.zip, de: ftp://ftp.microsoft.com/reskit/win2000/
2.  Copie los archivos del proveedor WMI de DNS (Dnsprov.dll) y Dnsschema. mof en el <winntdir> \\ \\ directorio system32 WBEM.
3.  Compile el archivo MOF. Al hacerlo, se personaliza el esquema para que coincida con el servidor.

    **MOFCOMP Dnsschema. mof**

4.  Registre el archivo DLL en el servidor DNS.

    **regsvr32 dnsprov.dll**

5.  Los scripts o programas que utilizan el proveedor WMI de DNS para administrar los servidores DNS se pueden usar. Los scripts o programas se pueden ejecutar desde el servidor DNS o desde un equipo cliente.
    > [!Note]  
    > El SDK de WMI no es necesario para ejecutar el proveedor WMI de DNS, pero contiene muchas herramientas útiles.

     

El proveedor WMI de DNS debe estar instalado en cualquier servidor DNS que se va a administrar; sin embargo, los scripts de DNS se pueden ejecutar en el servidor DNS o en un host remoto.

**Para instalar el proveedor WMI de DNS en Windows Server 2003**

-   En el caso de los sistemas operativos Windows Server 2003, el proveedor WMI de DNS se instala y registra automáticamente, y su archivo MOF se compila cuando se instala el servicio servidor DNS.

 

 




