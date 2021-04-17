---
title: Configuración predeterminada de .NET Framework
description: .NET Framework 4,5 es el valor predeterminado y .NET Framework 3,5 es opcional
ms.assetid: 19B53C82-812A-49AC-87C6-C08E7C199208
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1f91acc8739b2c660bfb1ba1392ea192511d1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "105705069"
---
# <a name="net-framework-45-is-default-and-net-framework-35-is-optional"></a>.NET Framework 4,5 es el valor predeterminado y .NET Framework 3,5 es opcional

## <a name="platforms"></a>Plataformas

**Clientes**   de   Windows 8  
**Servidores**   de   Windows Server 2012  

## <a name="description"></a>Descripción

.NET Framework 4,5 está habilitado de forma predeterminada en Windows 8. Windows 8 no incluye .NET 3,5 de forma predeterminada, pero los archivos para .NET 3,5 están disponibles en los medios de instalación de Windows 8 como una característica opcional.

Si el usuario está actualizando de Windows 7 a Windows 8, .NET Framework 3,5 está totalmente habilitado para asegurarse de que las aplicaciones del equipo sigan funcionando correctamente.

## <a name="manifestation"></a>Manifestación

Si el usuario realiza una instalación limpia de Windows 8 y, a continuación, instala las aplicaciones que requieren .NET Framework 3,5 (o 2,0), desencadenará una solicitud para los archivos de .NET 3,5 necesarios. Normalmente, los archivos que faltan se descargarán de Windows Update (después de solicitar permiso al usuario), pero si no es posible el acceso a Windows Update, la habilitación de .NET Framework 3,5 producirá un error a menos que se haya especificado un origen alternativo para los archivos que faltan.

## <a name="mitigation"></a>Mitigación

Para habilitar .NET Framework 3,5 solo en máquinas de prueba con instalaciones limpias de Windows 8:

1.  Copie \\ \\ los orígenes SxS \\ de la imagen ISO de compilación del sistema operativo montada en dotnet35 o en una carpeta similar. Por ejemplo:
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  Ejecute esta línea de comandos con privilegios de administrador:
    ```
    Dism.exe /online /enable-feature /featurename:NetFX3 /All /Source:c:\dotnet35 /LimitAccess

    ```



> [!Note]  
> La carpeta de orígenes \\ SxS no debe usarse como mecanismo de redistribución, ya que no es un mecanismo compatible.



## <a name="solution"></a>Solución

**Para los consumidores:**

Windows 8 incluye un mecanismo que habilita automáticamente .NET Framework 3,5 al intentar instalar el paquete redistribuible o cuando un instalador de la aplicación que necesita .NET 3,5 invoca el redistribuible.

**Para desarrolladores de aplicaciones (y administradores de TI):**

Los administradores de TI pueden configurar aplicaciones de .NET 3,5 para que se ejecuten en .NET 3,5 o .NET 4,5 (según lo que ya esté instalado). Para ejecutar una aplicación administrada en 3,5 o 4,5, solo tiene que agregar una sección en el archivo de configuración de la aplicación. Esto garantizará que si .NET 3,5 está instalado, la aplicación se ejecutará en .NET 3,5; de lo contrario, la aplicación se ejecutará en .NET 4,5. A continuación se proporciona un ejemplo de la sección adicional en el archivo de configuración:


```
<configuration>
   <startup>
      <supportedRuntime version="v2.0.50727"/>
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5"/>
   </startup>
</configuration>
```



**Para los OEM de empresa:**

Para habilitar .NET Framework 3,5 para las compilaciones de EEAP y para las aplicaciones que no tienen acceso a Windows Update:

1.  Copie los \\ orígenes \\ SxS \\ de la imagen ISO de compilación del SO montado en la dotnet35 o en una carpeta similar. Por ejemplo:
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  Establezca RegKey:
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]
     LocalSourcePath = c:\dotnet35
    ```



**Para empresas:**

En el caso de las máquinas que están configuradas para usar WSUS para el servicio, puede establecer una entrada del registro para permitir que el equipo use Windows Update para habilitar .NET 3,5 en lugar de WSUS (el mantenimiento se realizará desde WSUS si lo hace).

-   Establezca RegKey:
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]  RepairContentServerSource =DWORD(2)
    ```



Esta entrada del registro también se puede establecer mediante directiva de grupo (Directiva de equipo local-configuración del equipo de >-> Plantillas administrativas-> sistema. Seleccione la opción especificar la configuración de instalación de componentes opcionales y reparación de componentes.

Si selecciona contacto Windows Update directamente para descargar el contenido de reparación en lugar de Windows Server Update Services (WSUS), cualquier intento de agregar características de Windows (por ejemplo, .NET Framework 3,5) o características de reparación desencadenará descargas de archivos de Windows Update. Los equipos de destino necesitan acceso a Internet y WU para esta opción. Las operaciones de mantenimiento normales siguen usando WSUS si se ha configurado como origen.

**Nota relativa a la configuración de la ubicación de origen local a través de entradas del registro**

Los administradores de TI pueden establecer ubicaciones de origen locales para los archivos de .NET 3,5 a través de una entrada del registro, de modo que los usuarios puedan usar el cuadro de diálogo Agregar o quitar características de Windows para habilitar características con carga útil que faltan sin tener que especificar una ubicación de origen. El valor de la entrada del registro se puede controlar a través de la Directiva de grupo.

Se admite esta entrada del registro:



<table>
<thead>
<tr class="header">
<th>Entrada</th>
<th>Tipo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ruta de acceso de origen local</td>
<td> REG_EXPAND_SZ </td>
<td>Rutas de acceso de origen local que se usarán de forma predeterminada. Se pueden especificar varias rutas de acceso; deben separarse mediante;. Las ubicaciones se buscarán en el orden en que se especifiquen. <br/> Las ubicaciones de origen locales especificadas en la línea de comandos de DISM tienen prioridad sobre las ubicaciones especificadas en esta entrada del registro. Las ubicaciones de carpeta se pueden especificar en esta entrada del registro. <br/> Se puede usar Wim, pero la ruta de acceso debe ser al archivo WIM; no es necesario montarlo, por ejemplo: <br/> <dl> Wim: \\ machine\share\file.Wim: 1<br />
</dl> Observe el 1 al final. Debe especificar el índice numérico de la imagen que desea utilizar en el archivo WIM. <br/> En el caso de una WIM montada, la ruta de acceso de origen debe hacer referencia al directorio de Windows de la imagen montada, en lugar de al punto de montaje (por ejemplo:/Source: <mount_point> \Windows en lugar de/Source: <mount_point> ). <br/></td>
</tr>
</tbody>
</table>





## <a name="resources"></a>Recursos

<dl>

[Implementación de directivas basadas en el registro](/previous-versions/windows/desktop/Policy/implementing-registry-based-policy)  
</dl>