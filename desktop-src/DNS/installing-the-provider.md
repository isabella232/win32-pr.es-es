---
title: Instalación del proveedor
description: El procedimiento para instalar el proveedor WMI de DNS difiere en función de la versión de Windows en la que está instalado.
ms.assetid: 5f2bd11a-bc1d-4a43-92d4-26392d2504e7
keywords:
- Sistema de nombres de dominio, proveedor WMI, instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 722ca33b8359c613986bf551a0280ad4eb3ac9d2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880099"
---
# <a name="installing-the-provider"></a>Instalación del proveedor

El procedimiento para instalar el proveedor WMI de DNS difiere en función de la versión de Windows en la que está instalado. En el procedimiento siguiente se describe cómo instalar y configurar el proveedor WMI de DNS Windows 2000. Para obtener el proveedor WMI de DNS Windows 2000, descargue el archivo siguiente:

**ADVERTENCIA:** Los archivos del proveedor WMI de DNS no son intercambiables. Windows servidores DNS 2000 requieren archivos diferentes y un procedimiento diferente al de Windows Server 2003 DNS Server. Se proporciona el procedimiento para cada uno de ellos.

**Para instalar el proveedor WMI dns en Windows 2000 Server**

1.  Obtenga el proveedor WMI de DNS para Windows 2000 desde el Kit de recursos de servidor de Windows 2000 o descargue el archivo, Dnsprov.zip, desde: ftp://ftp.microsoft.com/reskit/win2000/
2.  Copie los archivos dns wmi provider (Dnsprov.dll) y Dnsschema.mof en el &lt; directorio winntdir &gt; \\ system32 \\ wbem.
3.  Compile el archivo MOF. Al hacerlo, se personaliza el esquema para que coincida con el servidor.

    **mofcomp dnsschema.mof**

4.  Registre el archivo DLL en el servidor DNS.

    **regsvr32 dnsprov.dll**

5.  A continuación, se pueden usar scripts o programas que usan el proveedor WMI de DNS para administrar servidores DNS. Los scripts o programas se pueden ejecutar desde el servidor DNS o desde un equipo cliente.
    > [!Note]  
    > El SDK de WMI no es necesario para ejecutar el proveedor DE WMI de DNS, pero contiene muchas herramientas útiles.

     

El proveedor WMI de DNS debe estar instalado en cualquier servidor DNS que se va a administrar; Sin embargo, los scripts DNS se pueden ejecutar en el servidor DNS o en un host remoto.

**Para instalar el proveedor WMI dns en Windows Server 2003**

-   Para Windows server 2003, el proveedor WMI de DNS se instala y registra automáticamente y su archivo MOF se compila cuando se instala el servicio servidor DNS.

 

 




