---
description: AppInit_DLLs en Windows 7 y Windows Server 2008 R2
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: AppInit_DLLs en Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8741039952b0ea15d32b19bc48d4197ea13751bc492ff82fc8e67b1662d0b682
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031075"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a>Archivos DLL de AppInit \_ en Windows 7 y Windows Server 2008 R2

## <a name="platform"></a>Plataforma

**Clientes:** Windows 7  
**Servidores:** Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** baja  
**Frecuencia:** baja  





## <a name="description"></a>Descripción

Los archivos DLL de AppInit son un mecanismo que permite cargar una lista arbitraria de archivos DLL en cada proceso de modo de usuario \_ del sistema. Microsoft está modificando la instalación de archivos DLL de AppInit en Windows 7 y Windows Server 2008 R2 para agregar un nuevo requisito de firma de código. Esto ayudará a mejorar la confiabilidad y el rendimiento del sistema, así como a mejorar la visibilidad del origen del software.

## <a name="configuration"></a>Configuración

Los valores almacenados en HKEY LOCAL MACHINE SOFTWARE Microsoft Windows NT CurrentVersion Windows clave en el Registro determinan el comportamiento de la infraestructura \_ \_ de archivos DLL \\ \\ \\ \\ \\ \_ AppInit. En la tabla siguiente se describen estos valores del Registro:



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
<td rowspan="2">LoadAppInit_DLLs (REG_DWORD)${REMOVE}$<br />
</td>
<td rowspan="2">Habilita o deshabilita globalmente AppInit_DLLs.${REMOVE}$<br />
</td>
<td>0x0: los AppInit_DLLs están deshabilitados.</td>
</tr>
<tr class="even">
<td>0x1: AppInit_DLLs están habilitados.</td>


</tr>
<tr class="odd">
<td>AppInit_DLLs (REG_SZ)</td>
<td>Lista delimitada por espacios o comas de archivos DLL que se cargarán. La ruta de acceso completa al archivo DLL debe especificarse mediante nombres cortos.</td>
<td>C:\ PROGRA~1\WID288~1\MICROS~1.DLL</td>
</tr>
<tr class="even">
<td rowspan="2">RequireSignedAppInit_DLLs (REG_DWORD)${REMOVE}$<br />
</td>
<td rowspan="2">Cargar solo archivos DLL firmados con código.${REMOVE}$<br />
</td>
<td>0x0: cargue los archivos DLL.</td>
</tr>
<tr class="odd">
<td>0x1: cargue solo archivos DLL firmados por código.</td>


</tr>
</tbody>
</table>



 

**Windows 7**

Todos los archivos DLL cargados por la infraestructura de archivos DLL AppInit \_ deben estar firmados por código. En a favor de la compatibilidad de aplicaciones, el Windows operativo 7 cargará todos los archivos DLL de AppInit. Sin embargo, Microsoft recomienda que todos los desarrolladores de aplicaciones firmen sus archivos DLL para ayudar a mejorar la confiabilidad de Windows y prepararse para el cumplimiento de la firma de código en versiones futuras de Windows. La clave del Registro RequireSignedAppInit controla este comportamiento y su valor en Windows 7 se establece \_ en 0 de forma predeterminada.

**Windows Server 2008 R2**

Todos los archivos DLL cargados por la infraestructura de archivos DLL AppInit \_ deben estar firmados por código. La clave del Registro RequireSignedAppInit controla este comportamiento y su valor en Windows Server 2008 R2 está establecido en \_ 1 de forma predeterminada.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

<dl>

[Archivos DLL de AppInit en Windows 7 y Windows Server 2008 R2](/windows-hardware/drivers/install/)  
</dl>

 

 
