---
title: Manifiesto de aplicación (ejecutable)
description: Manifiesto de aplicación (ejecutable)
ms.assetid: F46F33A6-0B2F-4086-9C6D-4AD43C26BCD3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4abd733bf1575a7f6106b0e6b2aaa068cffc56668dc595edc73ad0413c0c34e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549785"
---
# <a name="app-executable-manifest"></a>Manifiesto de aplicación (ejecutable)

## <a name="platforms"></a>Plataformas

**Clientes:** Windows 8  
**Servidores:** Windows Server 2012  


## <a name="description"></a>Descripción

La sección de compatibilidad del manifiesto de aplicación (ejecutable) que se introdujo en Windows ayuda al sistema operativo a determinar las versiones de Windows de destino de una aplicación. Además, el manifiesto de aplicación Windows proporcionar el comportamiento esperado por la aplicación en función de la versión de Windows destino de la aplicación.

La sección de compatibilidad del manifiesto permite a Windows proporcionar un nuevo comportamiento al software recién creado mientras se mantiene la compatibilidad con el software existente. Esta sección ayuda a Windows ofrecer una mayor compatibilidad en futuras versiones de Windows también. Por ejemplo, una aplicación que declara compatibilidad solo con Windows 8 en la sección de compatibilidad seguirá recibiendo un comportamiento Windows 8 en versiones futuras de Windows.

## <a name="manifestation"></a>Manifestación

Las aplicaciones sin una sección de compatibilidad en su manifiesto tendrán un comportamiento Windows Vista de forma predeterminada en Windows 7 y Windows 8 y versiones Windows posteriores. Tenga en cuenta que Windows XP y Windows Vista omiten esta sección de manifiesto y no les afecta.

Estos Windows proporcionan un comportamiento divergente en función de la sección de compatibilidad:

**Grupo de subprocesos predeterminado de llamada a procedimiento remoto (RPC)**

-   Windows 8 y Windows 7: para mejorar la escalabilidad y reducir el número de subprocesos, RPC cambió al grupo de subprocesos NT (grupo predeterminado). Para Windows Vista, RPC usó un grupo de subprocesos privado:

    -   Para los archivos binarios compilados para Windows 7 y versiones posteriores de Windows, se usa el grupo predeterminado.
    -   Si se llama a I RpcMgmtEnableDedicatedThreadPool antes de llamar a cualquier API RPC, se usa el grupo de subprocesos privado \_ (comportamiento de Vista).
    -   Si se llama a I RpcMgmtEnableDedicatedThreadPool después de una llamada RPC, se usa el grupo \_ predeterminado, I \_ RpcMgmtEnableDedicatedThreadPool devuelve el error 1764 y no se admite la operación solicitada.

-   Windows Vista (valor predeterminado): para los archivos binarios compilados para Windows Vista y versiones anteriores de Windows, se usa el grupo privado.

**Bloqueo de DirectDraw**

-   Windows 8 y Windows 7: las aplicaciones manifestadas para Windows 7 y versiones posteriores del sistema operativo no pueden llamar a Lock API en DDRAW para bloquear el búfer de vídeo de escritorio principal; Si lo hace, se producirá un error y se devolverá un puntero NULL para la principal. Este comportamiento se aplica incluso si Administrador de ventanas de escritorio Composition no está activado. Las aplicaciones con compatibilidad declaradas para Windows 7 y versiones posteriores no deben bloquear el búfer de vídeo principal que se va a representar.
-   Windows Vista (valor predeterminado): las aplicaciones pueden adquirir un bloqueo en el búfer de vídeo principal, ya que las aplicaciones heredadas dependen de este comportamiento. La ejecución de la aplicación se desactiva Administrador de ventanas de escritorio.

**Transferencia de bloque de bits de DirectDraw (bitblt) a principal sin ventana de recorte**

-   Windows 8 y Windows 7: se impide que las aplicaciones manifestadas para Windows 7 y versiones posteriores de Windows realicen un bitblt en el búfer de vídeo principal de escritorio sin una ventana de recorte; Al hacerlo, se produce un error y el área bitblt no se representará. Windows aplica este comportamiento incluso si no se activa Administrador de ventanas de escritorio Composition. Las aplicaciones con compatibilidad declaradas para Windows 7 y versiones posteriores deben realizar una operación de bits en una ventana de recorte.
-   Windows Vista (valor predeterminado): las aplicaciones deben poder realizar un bitblt en la principal sin una ventana de recorte, ya que las aplicaciones heredadas dependen de este comportamiento. Al ejecutar esta aplicación se desactiva el Administrador de ventanas de escritorio.

**GetOverlappedResult API**

-   Windows 8 y Windows 7: resuelve una condición de carrera en la que una aplicación multiproceso mediante **GetOverlappedResult** puede devolver sin restablecer el evento en la estructura superpuesta, lo que hace que la siguiente llamada a esta función vuelva prematuramente.
-   Windows Vista (valor predeterminado): proporciona el comportamiento con la condición de carrera de la que las aplicaciones pueden tener una dependencia. Las aplicaciones que deben evitar esta carrera antes del comportamiento de Windows 7 deben esperar en el evento superpuesto y, cuando se señala, llamar a GetOverlappedResult con bWait == FALSE.

**Estado de los temas de shell en modo de contraste alto**

-   Windows 8: devuelve el estado de la tesón real para cuando está en modo de contraste alto.
-   Windows 7: devuelve la información como no disponible cuando está en modo de contraste alto porque DWM todavía está en funcionamiento.
-   Windows Vista (valor predeterminado): devuelve el formato como no disponible cuando está en modo de contraste alto porque DWM todavía está en funcionamiento.

**Shell iPersistFile::Save (Método)**

-   Windows 8: CShellLink::Save ahora determina si se llama al controlador IPersistFile con un argumento de ruta de acceso relativa y se produce un error en la llamada si es así.

    La [documentación pública](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) que describe este comportamiento indica que el argumento path debe ser una ruta de acceso absoluta:

-   Windows 7 y anteriores (valor predeterminado): CShellLink::Save no determina si el controlador iPersistFile envía una comprobación de ruta de acceso relativa y permite que las aplicaciones sigan trabajando con rutas de acceso absolutas o relativas.

**Asistente para la compatibilidad de programas (PCA)**

-   Windows 8: las aplicaciones con la sección de compatibilidad no obtienen la mitigación de PCA.
-   Windows 7: Se realiza un seguimiento de las aplicaciones con la sección de compatibilidad en busca de posibles problemas de compatibilidad Windows 8 cambios (que se describen en este documento).
-   Windows Vista (valor predeterminado): las aplicaciones que no se instalan correctamente o se bloquean durante el tiempo de ejecución en algunas circunstancias específicas obtienen la mitigación de PCA. Para más información, consulte la sección Recursos.

## <a name="leveraging-feature-capabilities"></a>Aprovechamiento de las funcionalidades de características

Actualice el manifiesto de aplicación con la información de compatibilidad más reciente para la compatibilidad con el sistema operativo. En esta sección se describen las adiciones al manifiesto:

**Espacio de nombres:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)

**Nombre de sección:** Compatibilidad (nueva sección)

**SupportedOS:** GUID del sistema operativo compatible: los GUID que se asignan a los sistemas operativos compatibles son:

-   {e2011457-1546-43c5-a5fe-008deee3d3f0}

    para **Windows Vista:** este es el valor predeterminado para el contexto de conmutación por recuperación.

-   {35138b9a-5d96-4fbd-8e2d-a2440225f93a}

    para **Windows 7:** las aplicaciones que establecen este valor en el manifiesto de aplicación obtienen el comportamiento Windows 7.

-   {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}

    for **Windows 8**: las aplicaciones que establecen este valor en el manifiesto de aplicación obtienen el Windows 8 aplicación

Microsoft generará y mostrará GUID para futuras versiones Windows, según sea necesario.

Un ejemplo XML de un manifiesto actualizado:

> [!Note]  
> Los nombres de atributo y etiqueta del manifiesto de aplicación distinguen mayúsculas de minúsculas.

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
    <application> 
        <!--The ID below indicates app support for Windows Vista -->
        <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates app support for Windows 7 -->
        <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--The ID below indicates app support for Windows 8 -->
        <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
    </application> 
</compatibility>
</assembly>
```



Los GUID de todos los sistemas operativos del ejemplo anterior proporcionan compatibilidad de nivel inferior. Las aplicaciones que admiten varias plataformas no necesitan manifiestos independientes para cada plataforma.

## <a name="tests"></a>Pruebas

Una aplicación puede especificar varios IDs de sistema operativo admitidos. Debe agregar un identificador de sistema operativo compatible si ha probado o está en proceso de prueba la aplicación en ese sistema operativo. Windows Vista y versiones anteriores del sistema operativo no presten atención a estas entradas. A partir de Windows 7, Windows elegirá el GUID de versión más alto del manifiesto hasta la versión de Windows en ejecución y dará soporte técnico a la aplicación en ese nivel. Para comprobar que la aplicación funciona con la nueva sección de compatibilidad de manifiestos de aplicación:

1.  Pruebe la aplicación con la nueva sección de compatibilidad e Id. de SupportedOS = { 4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} para asegurarse de que la aplicación funciona correctamente con el comportamiento de Windows 8 más reciente.
2.  Pruebe la aplicación con la nueva sección de compatibilidad e Id. de SupportedOS = {35138b9a-5d96-4fbd-8e2d-a2440225f93a} para asegurarse de que la aplicación funciona correctamente con el comportamiento Windows 7.
3.  Pruebe la aplicación con la nueva sección de compatibilidad e Id. de SupportedOS = {e2011457-1546-43c5-a5fe-008deee3d3f0} para asegurarse de que la aplicación funciona correctamente con el comportamiento de Windows Vista.

## <a name="resources"></a>Recursos

-   [QueryActCtxW (Función)](../sbscs/application-manifests.md)
-   [Manifiesto de UAC](/previous-versions/bb756929(v=msdn.10))
-   [Manifiestos de aplicación para Windows aplicaciones](../sbscs/application-manifests.md)
-   [Administrador de ventanas de escritorio (DWM)](../dwm/dwm-overview.md)
-   [Actualización de la discrepancia de contexto](https://support.microsoft.com/kb/978637)
-   [Asistente para la compatibilidad de programas](/previous-versions/bb756937(v=msdn.10))

 

 