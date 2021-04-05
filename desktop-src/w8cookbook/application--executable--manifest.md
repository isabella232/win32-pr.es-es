---
title: Manifiesto de aplicación (ejecutable)
description: Manifiesto de aplicación (ejecutable)
ms.assetid: F46F33A6-0B2F-4086-9C6D-4AD43C26BCD3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de6f5a1d26af4b8ac6314655013ed56275bf7d73
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104078497"
---
# <a name="app-executable-manifest"></a>Manifiesto de aplicación (ejecutable)

## <a name="platforms"></a>Plataformas

**Clientes** : Windows 8  
**Servidores** : Windows Server 2012  


## <a name="description"></a>Descripción

La sección de compatibilidad del manifiesto de la aplicación (ejecutable) introducida en Windows ayuda al sistema operativo a determinar las versiones de Windows a las que se diseñó una aplicación como destino. Además, el manifiesto de la aplicación permite que Windows proporcione el comportamiento que espera la aplicación en función de la versión de Windows a la que se dirige la aplicación.

La sección de compatibilidad del manifiesto permite que Windows proporcione un nuevo comportamiento al software recién creado a la vez que mantiene la compatibilidad con el software existente. En esta sección también se ayuda a Windows a ofrecer mayor compatibilidad en versiones futuras de Windows. Por ejemplo, una aplicación que solo admita Windows 8 en la sección de compatibilidad seguirá recibiendo el comportamiento de Windows 8 en versiones futuras de Windows.

## <a name="manifestation"></a>Manifestación

Las aplicaciones sin una sección de compatibilidad en el manifiesto tendrán el comportamiento de Windows Vista de forma predeterminada en Windows 7 y Windows 8 y versiones futuras de Windows. Tenga en cuenta que Windows XP y Windows Vista omiten esta sección del manifiesto y no tienen ningún impacto en ellos.

Estos componentes de Windows proporcionan un comportamiento divergente basado en la sección de compatibilidad:

**Grupo de subprocesos predeterminado de llamada a procedimiento remoto (RPC)**

-   Windows 8 y Windows 7: para mejorar la escalabilidad y reducir los recuentos de subprocesos, RPC ha cambiado al grupo de subprocesos de NT (grupo predeterminado). En Windows Vista, RPC usaba un grupo de subprocesos privados:

    -   Para los archivos binarios compilados para Windows 7 y versiones posteriores de Windows, se usa el grupo predeterminado.
    -   Si \_ se llama a I RpcMgmtEnableDedicatedThreadPool antes de llamar a cualquier API de RPC, se usa el grupo de subprocesos privados (comportamiento de vista).
    -   Si \_ se llama a RpcMgmtEnableDedicatedThreadPool después de una llamada RPC, se usa el grupo predeterminado, I \_ RpcMgmtEnableDedicatedThreadPool devuelve el error 1764 y no se admite la operación solicitada.

-   Windows Vista (valor predeterminado): para los archivos binarios compilados para Windows Vista y versiones anteriores de Windows, se usa el grupo privado.

**Bloqueo DirectDraw**

-   Windows 8 y Windows 7: las aplicaciones con manifiesto para Windows 7 y versiones posteriores del sistema operativo no pueden llamar a la API de bloqueo en DDRAW para bloquear el búfer de vídeo del escritorio primario. Si lo hace, se producirá un error y se devolverá un puntero nulo para el principal. Este comportamiento se aplica incluso si Administrador de ventanas de escritorio composición no está activada. Las aplicaciones con compatibilidad declarada para Windows 7 y versiones posteriores no deben bloquear el búfer de vídeo primario para que se represente.
-   Windows Vista (valor predeterminado): las aplicaciones pueden adquirir un bloqueo en el búfer de vídeo principal, ya que las aplicaciones heredadas dependen de este comportamiento. la ejecución de la aplicación desactiva Administrador de ventanas de escritorio.

**Transferencia de bloque de bits de DirectDraw (bitblt) a principal sin ventana de recorte**

-   Windows 8 y Windows 7: las aplicaciones con manifiesto para Windows 7 y versiones posteriores de Windows no pueden realizar una operación bitblt en el búfer de vídeo de escritorio primario sin una ventana de recorte. Si lo hace, se producirá un error y el área de bitblt no se representará. Windows aplica este comportamiento incluso si no activa Administrador de ventanas de escritorio composición. Las aplicaciones con compatibilidad declarada para Windows 7 y versiones posteriores deben ejecutar bitblt en una ventana de recorte.
-   Windows Vista (valor predeterminado): las aplicaciones deben ser capaces de ejecutar bitblt en la principal sin una ventana de recorte, ya que las aplicaciones heredadas dependen de este comportamiento. al ejecutar esta aplicación, se desactiva el Administrador de ventanas de escritorio.

**API de GetOverlappedResult**

-   Windows 8 y Windows 7: resuelve una condición de carrera en la que una aplicación multiproceso que usa **GetOverlappedResult** puede devolver sin restablecer el evento en la estructura superpuesta, lo que hace que la siguiente llamada a esta función devuelva prematuramente.
-   Windows Vista (valor predeterminado): proporciona el comportamiento con la condición de carrera en la que las aplicaciones pueden tener una dependencia. Las aplicaciones que deben evitar esta carrera antes del comportamiento de Windows 7 deben esperar en el evento superpuesto y, cuando se señalice, llamar a GetOverlappedResult con bWait = = FALSE.

**Estado de los temas de Shell en el modo de contraste alto**

-   Windows 8: devuelve el estado real de los Estados de en el modo de contraste alto.
-   Windows 7: devuelve como no disponible en el modo de contraste alto porque DWM todavía está activado.
-   Windows Vista (valor predeterminado): devuelve como no disponible en el modo de contraste alto porque DWM todavía está activado.

**Shell iPersistFile:: Save (método)**

-   Windows 8: CShellLink:: Save ahora determina si se llama al controlador IPersistFile con un argumento de ruta de acceso relativa y produce un error en la llamada si es.

    La [documentación pública](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) que describe este comportamiento indica que el argumento de ruta de acceso debe ser una ruta de acceso absoluta:

-   Windows 7 y versiones anteriores (valor predeterminado): CShellLink:: Save no determina si el controlador iPersistFile envía una comprobación de ruta de acceso relativa y permite que las aplicaciones sigan trabajando con rutas de acceso absolutas o relativas.

**Asistente para la compatibilidad de programas (PCA)**

-   Windows 8: las aplicaciones con la sección de compatibilidad no obtienen la mitigación del PCA.
-   Windows 7: se realiza un seguimiento de las aplicaciones con la sección de compatibilidad para detectar posibles problemas de compatibilidad con los cambios de Windows 8 (descritos en este documento).
-   Windows Vista (valor predeterminado): las aplicaciones que no se instalan correctamente o se bloquean durante el tiempo de ejecución en algunas circunstancias específicas obtienen la mitigación del PCA. Para obtener más información, consulte la sección de recursos.

## <a name="leveraging-feature-capabilities"></a>Aprovechar las capacidades de características

Actualice el manifiesto de la aplicación con la información de compatibilidad más reciente para la compatibilidad con el sistema operativo. En esta sección se describen las adiciones al manifiesto:

**Espacio de nombres:** Compatibility. v1 (xmlns = "urn: schemas-microsoft-com: Compatibility. v1" >)

**Nombre de sección:** Compatibilidad (nueva sección)

**Compatibles:** GUID del sistema operativo compatible: los GUID que se asignan a los sistemas operativos admitidos son los siguientes:

-   {e2011457-1546-43c5-a5fe-008deee3d3f0}

    en **Windows Vista**: este es el valor predeterminado para el contexto Switchback

-   {35138b9a-5d96-4fbd-8e2d-a2440225f93a}

    en **Windows 7**: las aplicaciones que establecen este valor en el manifiesto de la aplicación obtienen el comportamiento de Windows 7.

-   {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}

    para **Windows 8**: las aplicaciones que establecen este valor en el manifiesto de aplicación obtienen el comportamiento de Windows 8.

Microsoft generará y publicará GUID para futuras versiones de Windows según sea necesario.

Un ejemplo XML de un manifiesto actualizado:

> [!Note]  
> Los nombres de atributo y etiqueta en el manifiesto de la aplicación distinguen mayúsculas de minúsculas.

 


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



Los GUID de todos los sistemas operativos en el ejemplo anterior proporcionan compatibilidad de nivel inferior. Las aplicaciones que admiten varias plataformas no necesitan manifiestos independientes para cada plataforma.

## <a name="tests"></a>Pruebas

Una aplicación puede especificar varios identificadores de sistema operativo compatibles. Debe agregar un identificador de sistema operativo compatible Si ha probado o está realizando pruebas en el sistema operativo de la aplicación. Windows Vista y versiones anteriores del sistema operativo no prestan atención a estas entradas. A partir de Windows 7, Windows elegirá el GUID de versión más alto del manifiesto hasta la versión de Windows en ejecución y proporcionará el soporte técnico de la aplicación en ese nivel. Para comprobar que la aplicación funciona con la nueva sección compatibilidad del manifiesto de la aplicación:

1.  Pruebe la aplicación con la nueva sección de compatibilidad y el ID. de Supported = {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} para asegurarse de que la aplicación funciona correctamente con el comportamiento más reciente de Windows 8.
2.  Pruebe la aplicación con la nueva sección de compatibilidad y el ID. de Supported = {35138b9a-5d96-4fbd-8e2d-a2440225f93a} para asegurarse de que la aplicación funciona correctamente con el comportamiento de Windows 7.
3.  Pruebe la aplicación con la nueva sección de compatibilidad y el ID. de Supported = {e2011457-1546-43c5-a5fe-008deee3d3f0} para asegurarse de que la aplicación funciona correctamente con el comportamiento de Windows Vista.

## <a name="resources"></a>Recursos

-   [QueryActCtxW función)](../sbscs/application-manifests.md)
-   [Manifiesto de UAC](/previous-versions/bb756929(v=msdn.10))
-   [Manifiestos de aplicación para aplicaciones Windows](../sbscs/application-manifests.md)
-   [Administrador de ventanas de escritorio (DWM)](../dwm/dwm-overview.md)
-   [Actualización de coincidencia de contexto](https://support.microsoft.com/kb/978637)
-   [Asistente para la compatibilidad de programas](/previous-versions/bb756937(v=msdn.10))

 

 