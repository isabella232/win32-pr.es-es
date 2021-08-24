---
description: Manifiesto de aplicación
ms.assetid: f022374d-ea3f-477f-9b59-3188b775ed64
title: Manifiesto de aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ea81440458bb5ac106fd891cc370ebb2b2fcc1db2a70022bf746bd81dd1acd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680215"
---
# <a name="application-manifest"></a>Manifiesto de aplicación

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes:** Windows 7  
**Servidores:** Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** baja  
**Frecuencia:** baja  





## <a name="description"></a>Descripción

Windows 7 presenta una nueva sección en el manifiesto de aplicación denominada "Compatibilidad". Esta sección ayuda Windows a determinar las versiones de Windows a las que se diseñó una aplicación de destino y permite a Windows proporcionar el comportamiento esperado por la aplicación en función de la versión de Windows de destino de la aplicación.

La sección Compatibilidad permite a Windows proporcionar un nuevo comportamiento al nuevo software creado por el desarrollador al tiempo que se mantiene la compatibilidad con el software existente. Esta sección también ayuda a Windows ofrecer una mayor compatibilidad en versiones futuras de Windows también. Por ejemplo, una aplicación que declara compatibilidad solo para Windows 7 en la sección Compatibilidad seguirá recibiendo un comportamiento de Windows 7 en la versión futura de Windows.

## <a name="manifestation-of-change"></a>Demostración del cambio

Las aplicaciones que no tienen una sección Compatibilidad en su manifiesto recibirán un comportamiento Windows Vista de forma predeterminada en Windows 7 y versiones Windows posteriores. Tenga en cuenta Windows XP y Windows Vista omiten esta sección de manifiesto y no tiene ningún impacto en ellos.

Los siguientes componentes Windows proporcionan un comportamiento divergente en función de la sección Compatibilidad de Windows 7:

**Grupo de subprocesos predeterminado de RPC**

-   **Windows 7:** Para mejorar la escalabilidad y reducir los recuentos de subprocesos, RPC cambió al grupo de subprocesos nt (grupo predeterminado). Para Windows Vista, RPC usó un grupo de subprocesos privado.
    -   En el caso de los archivos binarios compilados para Win7, se usa el grupo predeterminado
    -   Si se llama a I RpcMgmtEnableDedicatedThreadPool antes de llamar a cualquier API rpc, se usa el grupo de subprocesos privado \_ (comportamiento de Vista)
    -   Si se llama a I RpcMgmtEnableDedicatedThreadPool después de una llamada RPC, se usa el grupo \_ predeterminado, I \_ RpcMgmtEnableDedicatedThreadPool devuelve el error 1764 y no se admite la operación solicitada.
-   **Windows Vista (valor predeterminado):** Para los archivos binarios compilados para Windows Vista y versiones inferiores, se usa el grupo privado.

**Bloqueo de DirectDraw**

-   **Windows 7:** Las aplicaciones manifestadas para Windows 7 no pueden llamar a lock API en DDRAW para bloquear el búfer de vídeo principal del escritorio. Si lo hace, se producirá un error y se devolverá el puntero **NULL** para la principal. Este comportamiento se aplica incluso si Administrador de ventanas de escritorio Composition no está activado. Windows 7 aplicaciones compatibles no deben bloquear el búfer de vídeo principal que se va a representar.
-   **Windows Vista (valor predeterminado):** Las aplicaciones podrán adquirir un bloqueo en el búfer de vídeo principal, ya que las aplicaciones heredadas dependen de este comportamiento. La ejecución de la aplicación desactiva Administrador de ventanas de escritorio.

**Transferencia de bloques de bits de DirectDraw (Blt) a principal sin ventana de recorte**

-   **Windows 7:** Las aplicaciones manifestadas para Windows 7 no pueden realizar Blt en el búfer de vídeo de escritorio principal sin una ventana de recorte. Si lo hace, se producirá un error y el área Blt no se representará. Windows aplica este comportamiento incluso si no se activa Administrador de ventanas de escritorio Composition. Windows 7 aplicaciones compatibles deben ir a una ventana de recorte.
-   **Windows Vista (valor predeterminado):** Las aplicaciones deben poder ir a la principal sin una ventana de recorte, ya que las aplicaciones heredadas dependen de este comportamiento. La ejecución de esta aplicación desactiva el Administrador de ventanas de escritorio.

**GetOverlappedResult API**

-   **Windows 7:** Resuelve una condición de carrera en la que una aplicación multiproceso mediante GetOverlappedResult puede devolver sin restablecer el evento en la estructura superpuesta, lo que hace que la siguiente llamada a esta función vuelva prematuramente.
-   **Windows Vista (valor predeterminado):** Proporciona el comportamiento con la condición de carrera de la que las aplicaciones pueden tener una dependencia. Las aplicaciones que desean evitar esta carrera antes del comportamiento de Windows 7 deben esperar en el evento superpuesto y, cuando se le señale, llamar a GetOverlappedResult con bWait == **FALSE**.

**Asistente para la compatibilidad de programas (PCA)**

-   **Windows 7:** La sección Aplicaciones con compatibilidad no obtiene la mitigación de PCA.
-   **Windows Vista (valor predeterminado):** Las aplicaciones que no se instalan correctamente o se bloquean durante el tiempo de ejecución en determinadas circunstancias tendrán la mitigación de PCA. Para más información, consulte la sección de referencia.

## <a name="leveraging-feature-capabilities"></a>Aprovechamiento de las funcionalidades de características

Actualice el manifiesto de aplicación con la información de compatibilidad más reciente para la compatibilidad con el sistema operativo. En la sección se describen las adiciones al manifiesto:

-   **Espacio de nombres:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)

-   **Nombre de sección:** Compatibilidad (nueva sección)

-   **SupportedOS:** GUID del sistema operativo compatible: los GUID que se asignan a los sistemas operativos compatibles son:

    -   {e2011457-1546-43c5-a5fe-008deee3d3f0} para Windows Vista: este es el valor predeterminado para el contexto de conmutación por recuperación.
    -   {35138b9a-5d96-4fbd-8e2d-a2440225f93a} para Windows 7: Las aplicaciones que establecen este valor en el manifiesto de aplicación obtienen el comportamiento Windows 7.

    > [!Note]  
    > Microsoft generará y publicará GUID para futuras versiones Windows según sea necesario.

     

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

1.  Pruebe la aplicación con la nueva sección de compatibilidad y asegúrese de que la aplicación funciona correctamente con el comportamiento `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` más reciente Windows 7.
2.  Pruebe la aplicación con la nueva sección de compatibilidad y (o sin esta sección por completo) para asegurarse de que la aplicación funciona correctamente con los comportamientos de `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` Windows Vista en Windows 7

## <a name="known-issues"></a>Problemas conocidos

**Error de coincidencia de contexto** Una aplicación se ejecuta en un contexto de Windows Vista en lugar de en un contexto de Windows 7 en un equipo que ejecuta una edición x64 de Windows 7 o Windows Server 2008 R2.

**Solución** Hay actualizaciones disponibles para corregirlo en todas las versiones compatibles basadas en x64 de Windows 7 y Windows Server 2008 R2, así como para todas las versiones compatibles basadas en Itanium de Windows Server 2008 R2. Vaya a la página Soporte técnico de Microsoft de KB 978637: una aplicación se ejecuta en un contexto de Windows Vista en lugar de en un contexto de Windows 7 en un equipo que ejecuta una edición x64 de Windows 7 o [de Windows Server 2008 R2](https://support.microsoft.com/kb/978637) para obtener más detalles y descargar la versión correcta para el sistema.

**Diagnóstico de volcado de memoria bloqueado**

**Solución** Vaya a la página Soporte técnico de Microsoft de KB 976038: Las excepciones que se inician desde una aplicación que se ejecuta en una versión de [64](https://support.microsoft.com/kb/976038) bits de Windows se omiten para obtener más detalles.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [**QueryActCtxW (Función)**](/windows/win32/api/winbase/nf-winbase-queryactctxw)
-   [Manifiesto de UAC](/previous-versions/bb756929(v=msdn.10))
-   [Manifiestos de aplicación para Windows aplicaciones](../sbscs/application-manifests.md)
-   [Administrador de ventanas de escritorio (DWM)](../dwm/dwm-overview.md)
-   [Actualización de error de coincidencia de contexto](https://support.microsoft.com/kb/978637)

 

 
