---
description: .
ms.assetid: f022374d-ea3f-477f-9b59-3188b775ed64
title: Manifiesto de aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf4fd1ae8a9f66dafbe65a3db09dd014dbef31e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717131"
---
# <a name="application-manifest"></a>Manifiesto de aplicación

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes** : Windows 7  
**Servidores** : Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

 **Gravedad** baja  
**Frecuencia** : baja  





## <a name="description"></a>Descripción

Windows 7 incluye una nueva sección en el manifiesto de aplicación denominada "compatibilidad". En esta sección se ayuda a Windows a determinar las versiones de Windows a las que se diseñó una aplicación y se permite a Windows proporcionar el comportamiento que espera la aplicación en función de la versión de Windows de destino de la aplicación.

La sección de compatibilidad permite a Windows proporcionar un nuevo comportamiento al nuevo software creado por el desarrollador, a la vez que mantiene la compatibilidad con el software existente. Esta sección también ayuda a Windows a ofrecer mayor compatibilidad en versiones futuras de Windows. Por ejemplo, una aplicación que declare solo compatibilidad con Windows 7 en la sección de compatibilidad seguirá recibiendo el comportamiento de Windows 7 en una versión futura de Windows.

## <a name="manifestation-of-change"></a>Manifiesto de cambio

Las aplicaciones sin una sección de compatibilidad en su manifiesto recibirán el comportamiento de Windows Vista de forma predeterminada en Windows 7 y versiones futuras de Windows. Tenga en cuenta que Windows XP y Windows Vista omiten esta sección del manifiesto y no tienen ningún impacto en ellos.

Los siguientes componentes de Windows proporcionan un comportamiento divergente basado en la sección de compatibilidad de Windows 7:

**Grupo de subprocesos predeterminado de RPC**

-   **Windows 7:** Para mejorar la escalabilidad y reducir los recuentos de subprocesos, RPC ha cambiado al grupo de subprocesos de NT (grupo predeterminado). En Windows Vista, RPC usaba un grupo de subprocesos privados.
    -   Para los archivos binarios compilados para Win7, se usa el grupo predeterminado
    -   Si \_ se llama a I RpcMgmtEnableDedicatedThreadPool antes de llamar a cualquier API de RPC, se usa el grupo de subprocesos privados (comportamiento de vista)
    -   Si \_ se llama a RpcMgmtEnableDedicatedThreadPool después de una llamada RPC, se usa el grupo predeterminado, I \_ RpcMgmtEnableDedicatedThreadPool devuelve el error 1764 y no se admite la operación solicitada.
-   **Windows Vista (valor predeterminado):** Para los archivos binarios compilados para Windows Vista y versiones anteriores, se usa el grupo privado.

**Bloqueo DirectDraw**

-   **Windows 7:** Las aplicaciones con manifiesto para Windows 7 no pueden llamar a la API de bloqueo en DDRAW para bloquear el búfer de vídeo del escritorio primario. Si lo hace, se producirá un error y se devolverá el puntero **null** para la principal. Este comportamiento se aplica incluso si Administrador de ventanas de escritorio composición no está activada. Las aplicaciones compatibles con Windows 7 no deben bloquear el búfer de vídeo principal para que se represente.
-   **Windows Vista (valor predeterminado):** Las aplicaciones podrán adquirir un bloqueo en el búfer de vídeo principal, ya que las aplicaciones heredadas dependen de este comportamiento. La ejecución de la aplicación desactiva Administrador de ventanas de escritorio.

**Transferencia de bloque de bits de DirectDraw (BLT) a principal sin ventana de recorte**

-   **Windows 7:** Las aplicaciones con manifiesto para Windows 7 no pueden realizar la ejecución de BLT en el búfer de vídeo de escritorio primario sin una ventana de recorte. Si lo hace, se producirá un error y el área BLT no se representará. Windows aplica este comportamiento incluso si no activa Administrador de ventanas de escritorio composición. Las aplicaciones compatibles con Windows 7 deben tener BLT en una ventana de recorte.
-   **Windows Vista (valor predeterminado):** Las aplicaciones deben ser capaces de iniciar sesión en la principal sin una ventana de recorte, ya que las aplicaciones heredadas dependen de este comportamiento. Al ejecutar esta aplicación, se desactiva el Administrador de ventanas de escritorio.

**API de GetOverlappedResult**

-   **Windows 7:** Resuelve una condición de carrera en la que una aplicación multiproceso que usa GetOverlappedResult puede devolver sin restablecer el evento en la estructura superpuesta, lo que hace que la siguiente llamada a esta función devuelva prematuramente.
-   **Windows Vista (valor predeterminado):** Proporciona el comportamiento con la condición de carrera en la que las aplicaciones pueden tener una dependencia. Las aplicaciones que quieran evitar esta carrera antes del comportamiento de Windows 7 deben esperar en el evento superpuesto y, cuando se señalice, llamar a GetOverlappedResult con bWait = = **false**.

**Asistente para la compatibilidad de programas (PCA)**

-   **Windows 7:** En la sección aplicaciones con compatibilidad no se obtiene la mitigación del PCA.
-   **Windows Vista (valor predeterminado):** Las aplicaciones que no se instalan correctamente o se bloquean durante el tiempo de ejecución en algunas circunstancias específicas obtendrán la mitigación del PCA. Para obtener más información, consulte la sección de referencia.

## <a name="leveraging-feature-capabilities"></a>Aprovechar las capacidades de características

Actualice el manifiesto de aplicación con la información de compatibilidad más reciente para la compatibilidad con el sistema operativo. En la sección se describen las adiciones al manifiesto:

-   **Espacio de nombres:** Compatibility. v1 (xmlns = "urn: schemas-microsoft-com: Compatibility. v1" >)

-   **Nombre de sección:** Compatibilidad (nueva sección)

-   **Compatibles:** GUID del sistema operativo compatible: los GUID que se asignan a los sistemas operativos admitidos son los siguientes:

    -   {e2011457-1546-43c5-a5fe-008deee3d3f0} para Windows Vista: este es el valor predeterminado para el contexto de Switchback.
    -   {35138b9a-5d96-4fbd-8e2d-a2440225f93a} para Windows 7: las aplicaciones que establecen este valor en el manifiesto de aplicación obtienen el comportamiento de Windows 7.

    > [!Note]  
    > Microsoft generará y publicará GUID para futuras versiones de Windows según sea necesario.

     

El siguiente es un ejemplo de manifiesto actualizado.

> [!Note]  
> Los nombres de atributo y etiqueta en el manifiesto de aplicación distinguen mayúsculas de minúsculas.

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?> 
  <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--The ID below indicates application support for Windows Vista --> 
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates application support for Windows 7 --> 
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/> 
      </application> 
    </compatibility>
  </assembly>
```



El valor de agregar GUID para ambos sistemas operativos en el ejemplo anterior es proporcionar compatibilidad de nivel inferior. Las aplicaciones que admiten ambas plataformas no necesitarán manifiestos independientes para cada plataforma.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

1.  Pruebe la aplicación con la nueva sección de compatibilidad y `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` para asegurarse de que la aplicación funciona correctamente con el comportamiento más reciente de Windows 7.
2.  Pruebe la aplicación con la nueva sección de compatibilidad y `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (o sin esta sección completamente) para asegurarse de que la aplicación funciona correctamente con los comportamientos de Windows Vista en Windows 7.

## <a name="known-issues"></a>Problemas conocidos

Error de **coincidencia de contexto** Una aplicación se ejecuta en un contexto de Windows Vista en lugar de en un contexto de Windows 7 en un equipo que ejecuta una edición x64 de Windows 7 o Windows Server 2008 R2.

**Solución** de Hay actualizaciones disponibles para corregir este fin en todas las versiones compatibles basadas en x64 de Windows 7 y Windows Server 2008 R2, así como para todas las versiones compatibles basadas en Itanium de Windows Server 2008 R2. Vaya a la página de Soporte técnico de Microsoft de [KB 978637: una aplicación se ejecuta en un contexto de Windows Vista en lugar de en un contexto de Windows 7 en un equipo que ejecuta una edición x64 de Windows 7 o Windows Server 2008 R2](https://support.microsoft.com/kb/978637) para obtener más detalles y descargar la versión correcta del sistema.

**Diagnóstico de volcado de bloqueo bloqueado**

**Solución** de Vaya a la página de Soporte técnico de Microsoft de [KB 976038: las excepciones que se inician desde una aplicación que se ejecuta en una versión de Windows de 64 bits se omiten](https://support.microsoft.com/kb/976038) para obtener más detalles.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [**QueryActCtxW función)**](/windows/win32/api/winbase/nf-winbase-queryactctxw)
-   [Manifiesto de UAC](/previous-versions/bb756929(v=msdn.10))
-   [Manifiestos de aplicación para aplicaciones Windows](../sbscs/application-manifests.md)
-   [Administrador de ventanas de escritorio (DWM)](../dwm/dwm-overview.md)
-   [Actualización de coincidencia de contexto](https://support.microsoft.com/kb/978637)

 

 
