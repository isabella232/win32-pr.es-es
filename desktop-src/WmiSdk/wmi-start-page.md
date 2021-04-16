---
description: Instrumental de administración de Windows (WMI) es la infraestructura de datos y operaciones de administración en sistemas operativos basados en Windows.
ms.assetid: 4804152f-2042-4c6a-83c6-75c5e1ab7a04
ms.tgt_platform: multiple
title: Instrumental de administración de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec2313ca7ee744ebe6f14be42a33e2e5878960b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696916"
---
# <a name="windows-management-instrumentation"></a>Instrumental de administración de Windows

## <a name="purpose"></a>Propósito

Instrumental de administración de Windows (WMI) es la infraestructura de datos y operaciones de administración en sistemas operativos basados en Windows. Puede escribir scripts o aplicaciones de WMI para automatizar las tareas administrativas en equipos remotos, pero WMI también proporciona datos de administración a otras partes del sistema operativo y los productos, por ejemplo System Center Operations Manager, anteriormente Microsoft Operations Manager (MOM) o Administración remota de Windows ([WinRM](/windows/desktop/WinRM/portal)).

> [!Note]  
> La siguiente documentación está dirigida a desarrolladores y administradores de ti. Si es un usuario final que ha experimentado un mensaje de error relacionado con WMI, debe ir a [soporte técnico de Microsoft](https://support.microsoft.com/) y buscar el código de error que aparece en el mensaje de error. Para obtener más información acerca de la solución de problemas con los scripts WMI y el servicio WMI, vea [WMI no funciona.](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

> [!Note]  
> WMI es totalmente compatible con Microsoft; sin embargo, la versión más reciente del control y scripting administrativo está disponible a través de la infraestructura de administración de Windows (MI). MI es totalmente compatible con las versiones anteriores de WMI y proporciona un host de características y ventajas que facilitan el diseño y el desarrollo de proveedores y clientes. Para obtener más información, consulte [infraestructura de administración de Windows (mi)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).

 

## <a name="where-applicable"></a>Donde sea aplicable

WMI se puede usar en todas las aplicaciones basadas en Windows y es muy útil en aplicaciones empresariales y scripts administrativos.

Los administradores del sistema pueden encontrar información sobre el uso de WMI en TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx)y en varios libros sobre WMI. Para obtener más información, vea más [información](further-information.md).

## <a name="developer-audience"></a>Audiencia de desarrolladores

WMI está diseñado para los programadores que utilizan C/C++, la aplicación de Microsoft Visual Basic o un lenguaje de scripting que tiene un motor de Windows y controla los objetos de Microsoft ActiveX. Aunque es útil cierta familiaridad con la programación COM, los desarrolladores de C++ que escriben aplicaciones pueden encontrar buenos ejemplos para empezar a [crear una aplicación WMI con C++](creating-a-wmi-application-using-c-.md).

Para desarrollar proveedores de código administrados o aplicaciones en C# o Visual Basic .NET mediante el .NET Framework, vea [WMI en .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).

Muchos administradores y profesionales de ti acceden a WMI a través de PowerShell. El cmdlet Get-WMI para PowerShell permite recuperar información de un repositorio de WMI local o remoto. Como tal, una serie de temas y clases, especialmente en la sección [creación de clientes WMI](creating-wmi-clients.md) , contiene ejemplos de PowerShell. Para obtener información adicional sobre el uso de PowerShell, vea [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) y [scripting con Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Para obtener más información sobre qué sistema operativo se requiere para utilizar un elemento de API específico o una clase WMI, consulte la sección de requisitos de cada tema en la documentación de WMI.

Si parece que falta un componente esperado, consulte [disponibilidad del sistema operativo de los componentes de WMI](operating-system-availability-of-wmi-components.md).

No es necesario descargar ni instalar un desarrollo de software (SDK) específico para crear scripts o aplicaciones para WMI. Sin embargo, hay algunas herramientas administrativas de WMI que los desarrolladores pueden encontrar útiles. Para obtener más información, consulte la sección descargas en [información adicional](further-information.md).

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Acerca de WMI](about-wmi.md)
</dt> <dd>

Información general sobre WMI.

</dd> <dt>

[Usar WMI](using-wmi.md)
</dt> <dd>

Información sobre cómo desarrollar aplicaciones para usar WMI, que incluye información sobre las herramientas.

</dd> <dt>

[Referencia de WMI](wmi-reference.md)
</dt> <dd>

Documentación acerca de las clases de WMI, clases de C++ de WMI, API COM de WMI, API de scripting y otro material de referencia de WMI.

</dd> </dl>

 

 
