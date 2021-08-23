---
title: .NET Framework configuración predeterminada
description: .NET Framework 4.5 es el valor predeterminado y .NET Framework 3.5 es opcional
ms.assetid: 19B53C82-812A-49AC-87C6-C08E7C199208
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e875f7508bc0940689afde5eb9b3f00407dd2c7dd70e35de52fe580717c8ad53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549795"
---
# <a name="net-framework-45-is-default-and-net-framework-35-is-optional"></a>.NET Framework 4.5 es el valor predeterminado y .NET Framework 3.5 es opcional

## <a name="platforms"></a>Plataformas

**Clientes Windows 8**     
**Servidores Windows Server 2012**     

## <a name="description"></a>Descripción

.NET Framework 4.5 está habilitado de forma predeterminada en Windows 8. Windows 8 no incluye .NET 3.5 de forma predeterminada, pero los archivos de .NET 3.5 están disponibles en el medio de instalación de Windows 8 como característica opcional.

Si el usuario está actualizando de Windows 7 a Windows 8, .NET Framework 3.5 está totalmente habilitado para asegurarse de que las aplicaciones del equipo sigan funcionando correctamente.

## <a name="manifestation"></a>Manifestación

Si el usuario realiza una instalación limpia de Windows 8 y, a continuación, instala aplicaciones que requieren .NET Framework 3.5 (o 2.0), desencadenará una solicitud para los archivos .NET 3.5 necesarios. Normalmente, los archivos que faltan se descargarán de Windows Update (después de pedir permiso al usuario), pero si no es posible el acceso a Windows Update, se producirá un error al habilitar .NET Framework 3.5 a menos que se haya especificado un origen alternativo para los archivos que faltan.

## <a name="mitigation"></a>Mitigación

Para habilitar .NET Framework 3.5 solo en máquinas de prueba con instalación limpia de Windows 8:

1.  Copie los sxs de orígenes de la imagen ISO de compilación del sistema operativo montado \\ \\ en \\ dotnet35 o una carpeta similar. Por ejemplo:
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  Ejecute esta línea de comandos con privilegios de administrador:
    ```
    Dism.exe /online /enable-feature /featurename:NetFX3 /All /Source:c:\dotnet35 /LimitAccess

    ```



> [!Note]  
> La carpeta \\ sources SxS no debe usarse como mecanismo de redistribución, ya que no se trata de un mecanismo admitido.



## <a name="solution"></a>Solución

**Para consumidores:**

Windows 8 incluye un mecanismo que habilita automáticamente .NET Framework 3.5 al intentar instalar el paquete redistribuible o cuando un instalador de aplicación que necesita .NET 3.5 invoca el redistribuible.

**Para desarrolladores de aplicaciones (y administradores de TI):**

Los administradores de TI pueden configurar aplicaciones de .NET 3.5 para que se ejecuten en .NET 3.5 o .NET 4.5 (en función de lo que ya esté instalado). Para ejecutar una aplicación administrada en 3.5 o 4.5, basta con agregar una sección en el archivo de configuración de la aplicación. Esto garantizará que, si .NET 3.5 está instalado, la aplicación se ejecutará en .NET 3.5. De lo contrario, la aplicación se ejecutará en .NET 4.5. A continuación se proporciona un ejemplo de la sección adicional del archivo de configuración:


```
<configuration>
   <startup>
      <supportedRuntime version="v2.0.50727"/>
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5"/>
   </startup>
</configuration>
```



**Para OEM empresariales:**

Para habilitar .NET Framework 3.5 para las compilaciones DE LAPAPA Y para las aplicaciones que no tienen acceso a Windows Update:

1.  Copie los sxs de orígenes de la imagen ISO de compilación del sistema operativo montado \\ \\ en la carpeta \\ dotnet35 o similar. Por ejemplo:
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  Establezca la clave de registro:
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]
     LocalSourcePath = c:\dotnet35
    ```



**Para empresas:**

En el caso de las máquinas que están configuradas para usar WSUS para el mantenimiento, puede establecer una entrada del Registro para permitir que la máquina use Windows Update para habilitar .NET 3.5 en lugar de WSUS (el mantenimiento se realizará desde WSUS si lo hace).

-   Establezca la clave de registro:
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]  RepairContentServerSource =DWORD(2)
    ```



Esta entrada del Registro también se puede establecer a través de directiva de grupo (Directiva de equipo local -> configuración del equipo -> Plantillas administrativas -> sistema. Seleccione la opción Especificar la configuración para la instalación opcional de componentes y la reparación de componentes.

Si selecciona Contact Windows Update directly (Ponerse en contacto directamente con Windows Update) para descargar contenido de reparación en lugar de Windows Server Update Services (WSUS), cualquier intento de agregar características de Windows (por ejemplo, .NET Framework 3.5) o reparar características desencadenará descargas de archivos de Windows Update. Los equipos de destino requieren acceso a Internet y WU para esta opción. Las operaciones de mantenimiento normales siguen usando WSUS si se ha configurado como origen.

**Nota relacionada con la configuración de la ubicación de origen local a través de entradas del Registro**

Los administradores de TI pueden establecer las ubicaciónes de origen locales para los archivos de .NET 3.5 a través de una entrada del Registro, de modo que los usuarios puedan usar el cuadro de diálogo Agregar o quitar características de Windows para habilitar características con carga útil que faltan sin tener que especificar una ubicación de origen. El valor de la entrada del Registro se puede controlar a través de la directiva de grupo.

Esta entrada del Registro es compatible:



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
<td>Rutas de acceso de origen locales que se usarán de forma predeterminada. Se pueden especificar varias rutas de acceso; deben estar separados por ; . Las ubicaciones se buscarán en el orden en que se especifican. <br/> Las ubicaciones de origen locales que se especifican en la línea de comandos dism tienen prioridad sobre las ubicaciones especificadas en esta entrada del Registro. Las ubicaciones de carpeta se pueden especificar en esta entrada del Registro. <br/> Se pueden usar WIM, pero la ruta de acceso debe ser al archivo WIM; no es necesario montarlo, por ejemplo: <br/> <dl> wim: \\ machine\share\file.wim:1<br />
</dl> Observe el 1 al final. Debe especificar el índice numérico de la imagen que desea usar en el archivo WIM. <br/> Para un WIM montado, la ruta de acceso de origen debe hacer referencia al directorio windows de la imagen montada, en lugar del punto de montaje (por ejemplo: /source: \windows en lugar <mount_point> de /source: <mount_point> ). <br/></td>
</tr>
</tbody>
</table>





## <a name="resources"></a>Recursos

<dl>

[Implementación de la directiva basada en el Registro](/previous-versions/windows/desktop/Policy/implementing-registry-based-policy)  
</dl>