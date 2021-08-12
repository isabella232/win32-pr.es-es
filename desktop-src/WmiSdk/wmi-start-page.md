---
description: Windows Instrumental de administración (WMI) es la infraestructura para la administración de datos y operaciones en Windows sistemas operativos basados en administración.
ms.assetid: 4804152f-2042-4c6a-83c6-75c5e1ab7a04
ms.tgt_platform: multiple
title: Instrumental de administración de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0b08c0301881b57c8132be9eead2e5b52cb64d4d3c4278985a573d5bff94f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553139"
---
# <a name="windows-management-instrumentation"></a>Instrumental de administración de Windows

## <a name="purpose"></a>Propósito

Windows Instrumental de administración (WMI) es la infraestructura para la administración de datos y operaciones en Windows sistemas operativos basados en administración. Puede escribir scripts WMI o aplicaciones para automatizar tareas administrativas en equipos remotos, pero WMI también proporciona datos de administración a otras partes del sistema operativo y productos, por ejemplo, System Center Operations Manager, anteriormente Microsoft Operations Manager (MOM) o Windows Remote Management[(WinRM).](/windows/desktop/WinRM/portal)

> [!Note]  
> La siguiente documentación está dirigida a desarrolladores y administradores de TI. Si es un usuario final que ha experimentado un mensaje de error relativo a WMI, debe ir [a Soporte técnico de Microsoft](https://support.microsoft.com/) y buscar el código de error que ve en el mensaje de error. Para obtener más información sobre cómo solucionar problemas con scripts WMI y el servicio WMI, vea [WMI isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

> [!Note]  
> WMI es totalmente compatible con Microsoft; sin embargo, la versión más reciente de scripting administrativo y control está disponible a través de Windows Management Infrastructure (MI). MI es totalmente compatible con versiones anteriores de WMI y proporciona una serie de características y ventajas que facilitan el diseño y el desarrollo de proveedores y clientes que nunca. Para obtener más información, [vea Windows Management Infrastructure (MI)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).

 

## <a name="where-applicable"></a>Donde sea aplicable

WMI se puede usar en todas las Windows basadas en aplicaciones y es más útil en aplicaciones empresariales y scripts administrativos.

Los administradores del sistema pueden encontrar información sobre el uso de WMI en TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx)y en varios libros sobre WMI. Para obtener más información, [vea Información adicional.](further-information.md)

## <a name="developer-audience"></a>Audiencia de desarrolladores

WMI está diseñado para programadores que usan C/C++, la aplicación Microsoft Visual Basic o un lenguaje de scripting que tiene un motor en Windows y controla objetos de microsoft ActiveX. Aunque es útil estar familiarizado con la programación COM, los desarrolladores de C++ que escriben aplicaciones pueden encontrar buenos ejemplos para empezar a trabajar en Creación de una [aplicación WMI mediante C++.](creating-a-wmi-application-using-c-.md)

Para desarrollar aplicaciones o proveedores de código administrado en C# o Visual Basic .NET mediante el .NET Framework, vea [WMI en .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).

Muchos administradores y profesionales de TI acceden a WMI a través de PowerShell. El cmdlet Get-WMI para PowerShell permite recuperar información de un repositorio WMI local o remoto. Por lo tanto, una serie de temas y clases, especialmente en la [sección Creación de clientes WMI,](creating-wmi-clients.md) contienen ejemplos de PowerShell. Para obtener más información sobre el uso de PowerShell, [consulte Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) scripting [con Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Para obtener más información sobre qué sistema operativo debe usar un elemento de API o una clase WMI específicos, vea la sección Requisitos de cada tema en la documentación de WMI.

Si parece que falta un componente esperado, vea Disponibilidad del sistema operativo [de componentes WMI.](operating-system-availability-of-wmi-components.md)

No es necesario descargar ni instalar un desarrollo de software (SDK) específico para crear scripts o aplicaciones para WMI. Sin embargo, hay algunas herramientas administrativas de WMI que los desarrolladores encuentran útiles. Para obtener más información, vea la sección Descargas de [Más información.](further-information.md)

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Acerca de WMI](about-wmi.md)
</dt> <dd>

Información general sobre WMI.

</dd> <dt>

[Uso de WMI](using-wmi.md)
</dt> <dd>

Información sobre cómo desarrollar aplicaciones para usar WMI, que incluye información sobre herramientas.

</dd> <dt>

[Referencia de WMI](wmi-reference.md)
</dt> <dd>

Documentación sobre las clases WMI, clases C++ de WMI, API COM de WMI, API de scripting y otro material de referencia de WMI.

</dd> </dl>

 

 
