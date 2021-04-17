---
description: .
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: AppInit_DLLs en Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31db695805b751e5dcd39293d0170c7fb78a11ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697784"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a>\_Archivos dll de Appinit en Windows 7 y Windows Server 2008 R2

## <a name="platform"></a>Plataforma

**Clientes** : Windows 7  
**Servidores** : Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

 **Gravedad** baja  
**Frecuencia** : baja  





## <a name="description"></a>Descripción

AppInit \_ dll es un mecanismo que permite cargar una lista arbitraria de archivos dll en cada proceso de modo de usuario del sistema. Microsoft está modificando la instalación de los archivos dll de AppInit en Windows 7 y Windows Server 2008 R2 para agregar un nuevo requisito de firma de código. Esto ayudará a mejorar la confiabilidad y el rendimiento del sistema, así como a mejorar la visibilidad del origen del software.

## <a name="configuration"></a>Configuración

Los valores almacenados en la \_ clave HKEY local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows en el registro determinan el comportamiento de la infraestructura de dll de Appinit \_ . En la tabla siguiente se describen estos valores del registro:



<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Descripción</th>
<th>Valores de ejemplo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">LoadAppInit_DLLs (REG_DWORD) $ {REMOVE} $<br />
</td>
<td rowspan="2">Habilita o deshabilita globalmente AppInit_DLLs. $ {REMOVE} $<br />
</td>
<td>0X0: AppInit_DLLs están deshabilitados.</td>
</tr>
<tr class="even">
<td>0x1: AppInit_DLLs están habilitadas.</td>


</tr>
<tr class="odd">
<td>AppInit_DLLs (REG_SZ)</td>
<td>Espacio o lista delimitada por comas de los archivos DLL que se van a cargar. La ruta de acceso completa al archivo DLL debe especificarse mediante nombres cortos.</td>
<td>C:\ PROGRAMA ~ 1 \ WID288 ~ 1 \ MICROS ~1.DLL</td>
</tr>
<tr class="even">
<td rowspan="2">RequireSignedAppInit_DLLs (REG_DWORD) $ {REMOVE} $<br />
</td>
<td rowspan="2">Cargar solo archivos DLL con firma de código. $ {REMOVE} $<br />
</td>
<td>0X0: cargar cualquier dll.</td>
</tr>
<tr class="odd">
<td>0x1: cargar solo archivos DLL con firma de código.</td>


</tr>
</tbody>
</table>



 

**Windows 7**

Todos los archivos dll cargados por la \_ infraestructura de archivos dll de Appinit deben tener firma de código. En aras de la compatibilidad de aplicaciones, el sistema operativo Windows 7 cargará todos los archivos dll de AppInit. Sin embargo, Microsoft recomienda que todos los desarrolladores de aplicaciones firmen el código de los archivos DLL para ayudar a mejorar la confiabilidad de Windows y prepararse para el cumplimiento de la firma de código en versiones futuras de Windows. La \_ clave del registro RequireSignedAppInit DLL controla este comportamiento y su valor en Windows 7 se establece en 0 de forma predeterminada.

**Windows Server 2008 R2**

Todos los archivos dll cargados por la \_ infraestructura de archivos dll de Appinit deben tener firma de código. La \_ clave del registro RequireSignedAppInit DLL controla este comportamiento y su valor en Windows Server 2008 R2 se establece en 1 de forma predeterminada.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

<dl>

[Archivos dll de AppInit en Windows 7 y Windows Server 2008 R2](/windows-hardware/drivers/install/)  
</dl>

 

 
