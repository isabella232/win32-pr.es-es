---
title: Actualización de los complementos de DSP existentes
description: Actualización de los complementos de DSP existentes
ms.assetid: 0525030e-eb30-41a0-8191-4a5727736857
keywords:
- Reproductor de Windows Media complementos, procesamiento de señales digitales (DSP)
- complementos, procesamiento de señales digitales (DSP)
- complementos de procesamiento de señales digitales, actualización
- Complementos de DSP, actualización
- versiones de Reproductor de Windows Media,complementos DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393cde356e0d86bb920825e731bb12ee0b7c2818
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465803"
---
# <a name="updating-existing-dsp-plug-ins"></a>Actualización de los complementos de DSP existentes

Es posible que los complementos DE DSP creados antes del lanzamiento del SDK de Reproductor de Windows Media 11 no funcionen como se esperaba con Reproductor de Windows Media 11 que se ejecuta en Windows Vista. Para asegurarse de que los clientes que ejecutan Reproductor de Windows Media 11 en Windows Vista pueden usar sus complementos, debe realizar algunos cambios en el código del complemento DSP, volver a compilar el proyecto y distribuir el complemento actualizado a los clientes.

Los proyectos creados con la versión más reciente del Reproductor de Windows Media complemento contendrán las actualizaciones necesarias. Consulte [Updates to the DSP Plug-in Wizard for Reproductor de Windows Media 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)(Actualizaciones del Asistente para complementos de DSP para Reproductor de Windows Media 11). (Es una buena idea ejecutar el asistente para crear un nuevo proyecto de ejemplo y, a continuación, usar una herramienta como Windiff.exe, que viene con Visual Studio, para inspeccionar las diferencias entre el código de ejemplo y el código de producción).

Hay tres cambios principales que deberá realizar en los complementos de DSP existentes:

-   Cambie la forma en que se registra el complemento. El complemento existente probablemente registre el modelo de subprocesos como "Apartment". Reproductor de Windows Media 11 que se ejecuta en Windows Vista requiere que los complementos de DSP registren el modelo de subprocesos como "Ambos". Para solucionar este problema, cambie el valor del modelo de subprocesos en el archivo .rgs *de nombre* del proyecto, como se muestra a continuación:

    ```C++
    val ThreadingModel = s 'Both'
    
    ```

    

    > [!Note]  
    > Al especificar el modelo de subprocesos como "Ambos", se quita cualquier serialización que COM proporciona para las llamadas a interfaces personalizadas. Si realiza llamadas a las interfaces personalizadas desde varios subprocesos, debe proporcionar esta serialización usted mismo.

     

    Reproductor de Windows Media 11 garantiza que las llamadas a DMO interfaces se serializan correctamente.

    1.  Agregue llamadas a [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) e [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) con un nuevo tipo de complemento: WMP PLUGINTYPE DSP OUTOFPROC en DllRegisterServer y DllUnregisterServer en el archivo \_ \_ \_ *projectnamedll*.cpp. Consulte las páginas de referencia de estos métodos para obtener más información.
    2.  Cree y distribuya un archivo DLL de proxy o código auxiliar para habilitar la serialización COM de cualquier interfaz personalizada implementada en o creada por la clase de complemento. Una interfaz personalizada es cualquier interfaz propietaria que defina e implemente para que la use el objeto de complemento. Esto incluye la interfaz personalizada que usa la página de propiedades, si ha proporcionado una, pero también puede incluir interfaces que se conectan a complementos de interfaz de usuario, por ejemplo. Un ejemplo de una interfaz personalizada creada por el asistente para complementos es *Iprojectname*. Algunos ejemplos de interfaces que no son interfaces personalizadas son **IMediaObject** **e IWMPPluginEnable.**

Si el complemento DSP procesa audio, también debe agregar compatibilidad con los siguientes formatos de audio nuevos:

-   FORMATO WAVE \_ \_ IEEE \_ FLOAT
-   WAVE \_ FORMAT EXTENSIBLE con \_ subformato KSDATAFORMAT \_ SUBTYPE IEEE \_ \_ FLOAT.

Si el complemento DSP procesa vídeo, debe agregar compatibilidad con el formato de vídeo NV12.

Vea el complemento DSP de audio o vídeo de ejemplo que crea el asistente para obtener un ejemplo de cómo procesar estos tipos de formato.

## <a name="about-the-proxystub-project"></a>Acerca del proxy o código auxiliar Project

Quizás la manera más sencilla de crear un proyecto dll de proxy o código auxiliar para el complemento DSP es ejecutar el Asistente para complementos de DSP. Esto creará un proyecto de proxy o código auxiliar de ejemplo que puede modificar para trabajar con el código existente. Deberá realizar los siguientes cambios:

1.  Quite las definiciones existentes para las interfaces personalizadas del código. Por ejemplo, el asistente del complemento DSP del SDK de Reproductor de Windows Media 10 creó la definición de interfaz *Iprojectname* en el archivo *projectname*.h mediante la palabra clave **interface.**
2.  Defina las interfaces personalizadas en el archivo IDL del proyecto de proxy/stub.
3.  Compile el proyecto de proxy/stub antes del proyecto principal. Puede configurar Visual Studio para hacerlo automáticamente si ambos proyectos forman parte de la misma solución.
4.  El compilador MIDL creará un nuevo archivo de encabezado con un nombre con el formato *nombrede proyecto* \_ h.h. Debe incluir este encabezado en el proyecto principal (en *projectname*.h). Contiene las definiciones de las interfaces personalizadas.

## <a name="distributing-the-updated-plug-in"></a>Distribución del complemento actualizado

Puede instalar el complemento actualizado en los equipos de los usuarios exactamente como lo ha hecho en el pasado. Sin embargo, ahora también debe distribuir y registrar el archivo DLL de proxy o código auxiliar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción al desarrollador del complemento DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




