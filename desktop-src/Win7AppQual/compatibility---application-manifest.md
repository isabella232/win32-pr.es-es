---
description: Manifiesto de aplicación
ms.assetid: f022374d-ea3f-477f-9b59-3188b775ed64
title: Manifiesto de aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c52b8eb2af87c271151be3d7989f50b2903084
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088593"
---
# <a name="application-manifest"></a>Manifiesto de aplicación

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes:** Windows 7  
**Servidores:** Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** baja  
**Frecuencia:** baja  





## <a name="description"></a>Descripción

Windows 7 presenta una nueva sección en el manifiesto de aplicación denominada "Compatibilidad". Esta sección ayuda a Windows a determinar las versiones de Windows a las que se diseñó una aplicación como destino y permite a Windows proporcionar el comportamiento esperado por la aplicación en función de la versión de Windows de destino de la aplicación.

La sección Compatibilidad permite a Windows proporcionar un nuevo comportamiento al nuevo software creado por el desarrollador y mantener la compatibilidad con el software existente. Esta sección también ayuda a Windows a ofrecer mayor compatibilidad en versiones futuras de Windows. Por ejemplo, una aplicación que declara compatibilidad solo para Windows 7 en la sección Compatibilidad seguirá recibiendo el comportamiento de Windows 7 en la versión futura de Windows.

## <a name="manifestation-of-change"></a>Demostración del cambio

Las aplicaciones sin una sección Compatibilidad de su manifiesto recibirán el comportamiento de Windows Vista de forma predeterminada en Windows 7 y versiones futuras de Windows. Tenga en cuenta que Windows XP y Windows Vista omiten esta sección de manifiesto y no tiene ningún impacto en ellos.

Los siguientes componentes de Windows proporcionan un comportamiento divergente en función de la sección Compatibilidad de Windows 7:

**Grupo de subprocesos predeterminado de RPC**

-   **Windows 7:** Para mejorar la escalabilidad y reducir los recuentos de subprocesos, RPC cambió al grupo de subprocesos nt (grupo predeterminado). Para Windows Vista, RPC usaba un grupo de subprocesos privado.
    -   En el caso de los archivos binarios compilados para Win7, se usa el grupo predeterminado
    -   Si se llama a I RpcMgmtEnableDedicatedThreadPool antes de llamar a cualquier API de RPC, se usa el grupo de subprocesos privado \_ (comportamiento de Vista)
    -   Si se llama a I RpcMgmtEnableDedicatedThreadPool después de una llamada RPC, se usa el grupo \_ predeterminado, I \_ RpcMgmtEnableDedicatedThreadPool devuelve el error 1764 y no se admite la operación solicitada.
-   **Windows Vista (valor predeterminado):** En el caso de los archivos binarios compilados para Windows Vista y versiones siguientes, se usa el grupo privado.

**Bloqueo de DirectDraw**

-   **Windows 7:** Las aplicaciones manifestadas para Windows 7 no pueden llamar a Lock API en DDRAW para bloquear el búfer de vídeo de escritorio principal. Si lo hace, se producirá un error y se devolverá el puntero **NULL** para la principal. Este comportamiento se aplica incluso si Administrador de ventanas de escritorio Composition no está activado. Las aplicaciones compatibles con Windows 7 no deben bloquear el búfer de vídeo principal que se va a representar.
-   **Windows Vista (valor predeterminado):** Las aplicaciones podrán adquirir un bloqueo en el búfer de vídeo principal, ya que las aplicaciones heredadas dependen de este comportamiento. La ejecución de la aplicación se desactiva Administrador de ventanas de escritorio.

**DirectDraw Bit Block Transfer (Blt) to Primary without Clipping Window**

-   **Windows 7:** Se impide que las aplicaciones manifestadas para Windows 7 realicen Blt en el búfer de vídeo de escritorio principal sin una ventana de recorte. Si lo hace, se producirá un error y el área Blt no se representará. Windows aplica este comportamiento incluso si no se activa Administrador de ventanas de escritorio Composition. Las aplicaciones compatibles con Windows 7 deben ir a una ventana de recorte.
-   **Windows Vista (valor predeterminado):** Las aplicaciones deben poder ir a la principal sin una ventana de recorte, ya que las aplicaciones heredadas dependen de este comportamiento. La ejecución de esta aplicación desactiva el Administrador de ventanas de escritorio.

**GetOverlappedResult API**

-   **Windows 7:** Resuelve una condición de carrera en la que una aplicación multiproceso mediante GetOverlappedResult puede devolver sin restablecer el evento en la estructura superpuesta, lo que hace que la siguiente llamada a esta función vuelva prematuramente.
-   **Windows Vista (valor predeterminado):** Proporciona el comportamiento con la condición de carrera de la que las aplicaciones pueden tener una dependencia. Las aplicaciones que quieran evitar esta carrera antes del comportamiento de Windows 7 deben esperar en el evento superpuesto y, cuando se señalen, llamar a GetOverlappedResult con bWait == **FALSE**.

**Asistente para la compatibilidad de programas (PCA)**

-   **Windows 7:** La sección Aplicaciones con compatibilidad no obtiene la mitigación de PCA.
-   **Windows Vista (valor predeterminado):** Las aplicaciones que no se instalan correctamente o se bloquean durante el tiempo de ejecución en determinadas circunstancias tendrán la mitigación de PCA. Para más información, consulte la sección de referencia.

## <a name="leveraging-feature-capabilities"></a>Aprovechamiento de las funcionalidades de características

Actualice el manifiesto de aplicación con la información de compatibilidad más reciente para la compatibilidad con el sistema operativo. En la sección se describen las adiciones al manifiesto:

-   **Espacio de nombres:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)

-   **Nombre de sección:** Compatibilidad (nueva sección)

-   **SupportedOS:** GUID del sistema operativo compatible: los GUID que se asignan a los sistemas operativos compatibles son:

    -   {e2011457-1546-43c5-a5fe-008deee3d3f0} para Windows Vista: este es el valor predeterminado para el contexto de conmutación por recuperación.
    -   {35138b9a-5d96-4fbd-8e2d-a2440225f93a} para Windows 7: las aplicaciones que establecen este valor en el manifiesto de aplicación obtienen el comportamiento de Windows 7.

    > [!Note]  
    > Microsoft generará y publicará GUID para futuras versiones de Windows según sea necesario.

     

A continuación se muestra un ejemplo de un manifiesto actualizado.

> [!Note]  
> Los nombres de atributo y etiqueta del manifiesto de aplicación distinguen mayúsculas de minúsculas.

 


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

1.  Pruebe la aplicación con la nueva sección de compatibilidad y asegúrese de que la aplicación funciona correctamente `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` con el comportamiento más reciente de Windows 7.
2.  Pruebe la aplicación con la nueva sección de compatibilidad y (o sin esta sección por completo) para asegurarse de que la aplicación funciona correctamente con los comportamientos de `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` Windows Vista en Windows 7

## <a name="known-issues"></a>Problemas conocidos

**Error de coincidencia de contexto** Una aplicación se ejecuta en un contexto de Windows Vista en lugar de en un contexto de Windows 7 en un equipo que ejecuta una edición x64 de Windows 7 o Windows Server 2008 R2.

**Solución** Hay actualizaciones disponibles para corregir esto en todas las versiones compatibles basadas en x64 de Windows 7 y Windows Server 2008 R2, así como para todas las versiones compatibles basadas en Itanium de Windows Server 2008 R2. Vaya a la página Soporte técnico de Microsoft de [KB 978637:](https://support.microsoft.com/kb/978637) una aplicación se ejecuta en un contexto de Windows Vista en lugar de en un contexto de Windows 7 en un equipo que ejecuta una edición x64 de Windows 7 o de Windows Server 2008 R2 para obtener más detalles y descargar la versión correcta para el sistema.

**Diagnóstico de volcado de memoria bloqueado**

**Solución** Vaya a la página Soporte técnico de Microsoft de [KB 976038:](https://support.microsoft.com/kb/976038) Las excepciones que se inician desde una aplicación que se ejecuta en una versión de 64 bits de Windows se omiten para obtener más detalles.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [**QueryActCtxW (Función)**](/windows/win32/api/winbase/nf-winbase-queryactctxw)
-   [Manifiesto de UAC](/previous-versions/bb756929(v=msdn.10))
-   [Manifiestos de aplicación para aplicaciones Windows](../sbscs/application-manifests.md)
-   [Administrador de ventanas de escritorio (DWM)](../dwm/dwm-overview.md)
-   [Actualización de la discrepancia de contexto](https://support.microsoft.com/kb/978637)

 

 
