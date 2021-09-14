---
description: Los scripts pueden acceder a todas las clases WMI para objetos de hardware y software.
ms.assetid: dbb29bc8-a675-4538-99f4-00613c83eeaa
ms.tgt_platform: multiple
title: Acceso de scripting a WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd487c127c670f9ddee9596e44c4b2b9691ed880
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358932"
---
# <a name="scripting-access-to-wmi"></a>Acceso de scripting a WMI

Los scripts pueden acceder a todas las clases WMI para objetos de hardware y software. Windows Los scripts de Host de script (WSH) pueden realizar operaciones en objetos del sistema de archivos, manipular impresoras de red o cambiar variables de entorno. Puede encontrar diversas tareas de administrador e instrucciones breves sobre cómo realizarlas en WMI en [Tareas de WMI para scripts y aplicaciones.](wmi-tasks-for-scripts-and-applications.md) Para obtener más información y ejemplos, vea El repositorio de scripts de Scriptcenter [de](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx)TechNet .

Si no está nuevo en scripting o en scripting específico de WMI, consulte la sección ScriptCenter de TechNet [Tareas iniciales](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx).

Con [Scripting API para WMI,](scripting-api-for-wmi.md)puede desarrollar scripts rápidos y sencillos o aplicaciones complejas. El scripting ofrece la misma capacidad de obtener información o de configurar la mayoría de los objetos de una empresa que tendría a través de una aplicación de C++ o C#. Para obtener más información, vea [Scripting en WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

No se puede escribir un [*proveedor WMI en*](gloss-p.md) el script. Para obtener más información, vea [Proporcionar datos a WMI.](providing-data-to-wmi.md)

Los scripts WMI se pueden escribir en cualquier lenguaje de scripting que pueda interactuar con ActiveX objetos.

Windows PowerShell proporciona un entorno sencillo para la administración y el scripting de WMI. Para obtener más información sobre PowerShell, [vea Tareas iniciales con Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).

Active Directory scripts de interfaces de servicio (ADSI) proporciona acceso a Active Directory Domain Services objetos (AD DS). Los scripts WSH y ADSI tienen acceso a objetos y permiten procedimientos que no están disponibles a través de archivos por lotes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de WMI](about-wmi.md)
</dt> <dt>

[API de scripting para WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 
