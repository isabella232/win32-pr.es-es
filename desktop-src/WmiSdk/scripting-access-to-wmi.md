---
description: Los scripts pueden tener acceso a todas las clases WMI para objetos de hardware y software.
ms.assetid: dbb29bc8-a675-4538-99f4-00613c83eeaa
ms.tgt_platform: multiple
title: Acceso de script a WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd487c127c670f9ddee9596e44c4b2b9691ed880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276141"
---
# <a name="scripting-access-to-wmi"></a>Acceso de script a WMI

Los scripts pueden tener acceso a todas las clases WMI para objetos de hardware y software. Los scripts de Windows Script Host (WSH) pueden realizar operaciones en objetos del sistema de archivos, manipular impresoras de red o cambiar variables de entorno. Puede encontrar una variedad de tareas de administrador e instrucciones breves sobre cómo realizarlas en WMI en [tareas WMI para scripts y aplicaciones](wmi-tasks-for-scripts-and-applications.md). Para obtener más información y ejemplos, vea el [repositorio de scripts](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx)de TechNet ScriptCenter.

Si no está familiarizado con el scripting o con el scripting específico de WMI, consulte la sección TechNet ScriptCenter [Introducción](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx).

Con la [API de scripting para WMI](scripting-api-for-wmi.md), puede desarrollar scripts rápidos, sencillos o aplicaciones complejas. Scripting ofrece la misma capacidad de obtener información o de configurar la mayoría de los objetos de una empresa como lo haría con una aplicación de C++ o C#. Para obtener más información, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

No se puede escribir un [*proveedor WMI*](gloss-p.md) en el script. Para obtener más información, consulte [proporcionar datos a WMI](providing-data-to-wmi.md).

Los scripts de WMI se pueden escribir en cualquier lenguaje de scripting que pueda interactuar con objetos ActiveX.

Windows PowerShell proporciona un entorno sencillo para la administración y el scripting de WMI. Para obtener más información sobre PowerShell, vea [Introducción con Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).

Active Directory scripts de interfaces de servicio (ADSI) proporciona acceso a objetos de Active Directory Domain Services (AD DS). Tanto los scripts de WSH como ADSI tienen acceso a objetos y permiten procedimientos no disponibles a través de archivos por lotes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de WMI](about-wmi.md)
</dt> <dt>

[API de scripting para WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 
