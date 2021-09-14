---
title: Instrumental de administración de Windows
description: Windows Instrumental de administración (WMI) es la infraestructura para los datos de administración y las operaciones en Windows operativos basados en aplicaciones.
ms.assetid: 4804152f-2042-4c6a-83c6-75c5e1ab7a04
ms.tgt_platform: multiple
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: 201bab9766b57564a20e6bee391fe87377e8262e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249332"
---
# <a name="windows-management-instrumentation"></a>Instrumental de administración de Windows

## <a name="purpose"></a>Propósito

Windows Instrumental de administración (WMI) es la infraestructura para los datos de administración y las operaciones en Windows operativos basados en aplicaciones. Puede escribir scripts o aplicaciones WMI para automatizar tareas administrativas en equipos remotos, pero WMI también proporciona datos de administración a otras partes del sistema operativo y productos, por &mdash; ejemplo, System Center Operations Manager (anteriormente Microsoft Operations Manager (MOM)) o Windows Remote Management[(WinRM).](/windows/win32/WinRM/portal)

> [!NOTE]  
> Esta documentación es para desarrolladores y administradores de TI. Si es un usuario final que ha experimentado un mensaje de error sobre WMI, debe ir [a Soporte técnico de Microsoft](https://support.microsoft.com/)y buscar el código de error que ve en el mensaje de error. Para obtener más información sobre cómo solucionar problemas con scripts WMI y el servicio WMI, vea [WMI no funciona.](/previous-versions/tn-archive/ff406382(v=msdn.10))

> [!NOTE]  
> WMI es totalmente compatible con Microsoft. Sin embargo, la versión más reciente de scripting administrativo y control está disponible a través de Windows Management Infrastructure (MI). MI es totalmente compatible con versiones anteriores de WMI y proporciona una serie de características y ventajas que facilitan el diseño y el desarrollo de proveedores y clientes que nunca. Para obtener más información, [vea Windows Management Infrastructure (MI)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).

## <a name="where-is-wmi-applicable"></a>¿Dónde es aplicable WMI?

WMI se puede usar en todas las Windows basadas en aplicaciones y es más útil en aplicaciones empresariales y scripts administrativos.

Los administradores del sistema pueden encontrar información sobre el uso de WMI en varios libros sobre WMI. Para obtener más información, [vea Más información.](further-information.md)

## <a name="developer-audience"></a>Audiencia de desarrolladores

WMI está diseñado para programadores que usan C/C++, la aplicación Microsoft Visual Basic o un lenguaje de scripting que tiene un motor en Windows y controla objetos ActiveX Microsoft. Aunque es útil estar familiarizado con la programación COM, los desarrolladores de C++ que escriben aplicaciones pueden encontrar buenos ejemplos para empezar a trabajar en Creación de una [aplicación WMI con C++.](creating-a-wmi-application-using-c-.md)

Para desarrollar aplicaciones o proveedores de código administrado en C# o Visual Basic .NET mediante el .NET Framework, vea [WMI en .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).

Muchos administradores y profesionales de TI acceden a WMI a través de PowerShell. El `Get-WMI` cmdlet de PowerShell permite recuperar información de un repositorio WMI local o remoto. Por lo tanto, una serie de temas y clases, especialmente en la sección Creación [de clientes WMI,](creating-wmi-clients.md) contienen ejemplos de PowerShell. Para obtener información adicional sobre el uso de PowerShell, [vea Windows PowerShell](/powershell/).

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Para obtener más información sobre qué sistema operativo es necesario para usar un elemento de API o una clase WMI específicos, vea la sección Requisitos de cada tema en la documentación de WMI.

Si parece que falta un componente esperado, vea Disponibilidad del sistema [operativo de componentes WMI.](operating-system-availability-of-wmi-components.md)

No es necesario descargar ni instalar un desarrollo de software (SDK) específico para crear scripts o aplicaciones para WMI. Sin embargo, hay algunas herramientas administrativas de WMI que los desarrolladores encuentran útiles. Para obtener más información, vea la sección Descargas de [Más información.](further-information.md)

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
| - | - |
| [Acerca de WMI](about-wmi.md) | Información general sobre WMI. |
| [Uso de WMI](using-wmi.md) | Información sobre cómo desarrollar aplicaciones para usar WMI, que incluye información sobre herramientas. |
| [Referencia de WMI](wmi-reference.md) | Documentación sobre las clases WMI, las clases C++ de WMI, la API COM de WMI, la API de scripting y otro material de referencia de WMI. |
| [Glosario wmi](wmi-glossary.md) | Windows Instrumental de administración (WMI) usa su propia colección de términos. Muchos de estos términos son familiares para los desarrolladores, pero tienen definiciones nuevas o modificadas en el entorno wmi. |
