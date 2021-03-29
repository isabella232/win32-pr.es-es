---
title: Actualización de complementos de DSP existentes
description: Actualización de complementos de DSP existentes
ms.assetid: 0525030e-eb30-41a0-8191-4a5727736857
keywords:
- Complementos de Windows Media Player, procesamiento de señal digital (DSP)
- complementos, procesamiento de señal digital (DSP)
- Complementos de procesamiento de señal digital, actualizar
- Complementos DSP, actualizar
- versiones de Windows Media Player, Complementos DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393cde356e0d86bb920825e731bb12ee0b7c2818
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788745"
---
# <a name="updating-existing-dsp-plug-ins"></a>Actualización de complementos de DSP existentes

Los complementos DSP creados antes de la versión del SDK de Windows Media Player 11 podrían no funcionar según lo esperado con Windows Media Player 11 en Windows Vista. Para asegurarse de que los clientes que ejecutan Windows Media Player 11 en Windows Vista pueden usar los complementos, debe realizar algunos cambios en el código del complemento DSP, volver a compilar el proyecto y distribuir el complemento actualizado a sus clientes.

Los proyectos creados con la versión más reciente del Asistente para complementos de Windows Media Player contendrán las actualizaciones necesarias. Vea [actualizaciones del Asistente para complementos de DSP para Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md). (Se recomienda ejecutar el Asistente para crear un nuevo proyecto de ejemplo y, a continuación, usar una herramienta como Windiff.exe, que se incluye con Visual Studio, para inspeccionar las diferencias entre el código de ejemplo y el código de producción).

Hay tres cambios principales que debe realizar en los complementos de DSP existentes:

-   Cambiar la manera en que se registra el complemento. El complemento existente probablemente registra el modelo de subprocesos como "Apartamento". Windows Media Player 11, que se ejecuta en Windows Vista, requiere que los complementos de DSP registren el modelo de subprocesos como "ambos". Puede corregir esto cambiando el valor del modelo de subprocesos en el archivo *projectname*. RGS, como se indica a continuación:

    ```C++
    val ThreadingModel = s 'Both'
    
    ```

    

    > [!Note]  
    > Al especificar el modelo de subprocesos como "ambos", se quita cualquier serialización que COM proporcione para las llamadas a interfaces personalizadas. Si realiza llamadas a las interfaces personalizadas desde varios subprocesos, debe proporcionar esta serialización usted mismo.

     

    Windows Media Player 11 garantiza que las llamadas a las interfaces de DMO se serializan correctamente.

    1.  Agregue llamadas a [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) y [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) con un nuevo tipo de complemento: wmp \_ PLUGINTYPE \_ DSP \_ OUTOFPROC en DllRegisterServer y DllUnregisterServer en el archivo *projectnamedll*. cpp. Para obtener más información, consulte las páginas de referencia de estos métodos.
    2.  Cree y distribuya un archivo DLL de proxy/stub para habilitar el cálculo de referencias COM de cualquier interfaz personalizada implementada o creada por la clase de complemento. Una interfaz personalizada es cualquier interfaz propietaria que defina e implemente para que la use el objeto de complemento. Esto incluye la interfaz personalizada usada por la página de propiedades, si proporcionó una, pero también puede incluir interfaces que se conectan a complementos de la interfaz de usuario, por ejemplo. Un ejemplo de una interfaz personalizada creada por el Asistente para complementos es *Iprojectname*. Entre los ejemplos de interfaces que no son interfaces personalizadas se incluyen **IMediaObject** y **IWMPPluginEnable**.

Si el complemento de DSP procesa audio, también debe agregar compatibilidad con los siguientes formatos de audio nuevos:

-   \_formato Wave \_ IEEE \_ float
-   \_Formato \_ de onda extensible con SUBformato KSDATAFORMAT \_ SubType \_ IEEE \_ float.

Si el complemento de DSP procesa vídeo, debe agregar compatibilidad con el formato de vídeo NV12.

Vea el complemento DSP de audio o vídeo de ejemplo que crea el Asistente para obtener un ejemplo de cómo procesar estos tipos de formato.

## <a name="about-the-proxystub-project"></a>Acerca del proyecto de proxy o código auxiliar

Quizás la manera más sencilla de crear un proyecto DLL de proxy/stub para el complemento de DSP es ejecutar el Asistente para complementos de DSP. Se creará un proyecto de proxy/código auxiliar de ejemplo que puede modificar para que funcione con el código existente. Tendrá que realizar los cambios siguientes:

1.  Quite todas las definiciones existentes de las interfaces personalizadas del código. Por ejemplo, el Asistente para complementos de DSP del SDK de Windows Media Player 10 creó la definición de la interfaz *Iprojectname* en el archivo *projectname*. h mediante la palabra clave **interface** .
2.  Defina las interfaces personalizadas en el archivo IDL del proyecto de proxy o código auxiliar.
3.  Compile el proyecto de proxy o código auxiliar antes del proyecto principal. Puede configurar Visual Studio para que lo haga automáticamente si ambos proyectos forman parte de la misma solución.
4.  El compilador MIDL creará un nuevo archivo de encabezado con un nombre con el formato *projectname* \_ h.h. Debe incluir este encabezado en el proyecto principal (en *projectname*. h). Contiene las definiciones de las interfaces personalizadas.

## <a name="distributing-the-updated-plug-in"></a>Distribuir el complemento actualizado

Puede instalar el complemento actualizado en los equipos de los usuarios exactamente como tenía en el pasado. Sin embargo, ahora debe distribuir y registrar también el archivo DLL de proxy/código auxiliar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción al desarrollador de complementos de DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




