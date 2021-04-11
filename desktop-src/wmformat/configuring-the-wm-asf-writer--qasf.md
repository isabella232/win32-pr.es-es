---
title: Configuración del escritor ASF de WM (QASF)
description: Configuración del escritor ASF de WM (QASF)
ms.assetid: 0f49ed5a-c228-456a-9551-8d277adccd0e
keywords:
- Windows Media Format SDK, configurar WM ASF Writer (QASF)
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, WM ASF Writer
- SDK de Windows Media Format, QASF
- Advanced Systems Format (ASF), configurar WM ASF Writer (QASF)
- ASF (Advanced Systems Format), configurar WM ASF Writer (QASF)
- Advanced Systems Format (ASF), WM ASF Writer
- ASF (formato de sistemas avanzados), escritor ASF de WM
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Advanced Systems Format (ASF), QASF
- ASF (formato de sistemas avanzados), QASF
- DirectShow, configuración de WM ASF Writer (QASF)
- DirectShow, escritor ASF de WM
- DirectShow, QASF
- Escritor ASF de WM, configurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f954522c4acae89e6f6dd001561811088c2a9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149527"
---
# <a name="configuring-the-wm-asf-writer-qasf"></a>Configuración del escritor ASF de WM (QASF)

Cuando se crea el filtro de [escritura ASF de WM](wm-asf-writer-filter.md) , se configura automáticamente con el \_ perfil WMProfile V80 \_ 256Video como valor predeterminado. Dado que este perfil usa los códecs Windows Media Audio y Windows Media Video versión 8, se recomienda crear un perfil personalizado que use los códecs de la serie Windows Media 9 y, a continuación, pasar su puntero [**IWMProfile**](iwmprofile.md) al filtro mediante el método [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) . El filtro debe agregarse al gráfico antes de que se pueda configurar el filtro y debe configurarse antes de que se pueda conectar a los filtros de nivel superior. El filtro usa el perfil para determinar el tipo de archivo de formato de Windows Media que se va a escribir, el número de clavijas de entrada que se configurarán y los tipos de medios que los pin pueden aceptar.

El filtro permite restablecer los perfiles mientras se conectan sus clavijas de entrada, siempre que el nuevo perfil no requiera ninguna clavija de entrada adicional. Por ejemplo, si cambia el perfil de un perfil de sólo audio de una entrada a un perfil de audio y vídeo de dos entradas, solo el PIN de audio será reconnectedAll los datos de entrada deben estar marcados con el tiempo y todos los pin de entrada deben estar conectados para poder ejecutar o pausar el filtro. Esto significa que si configura el filtro con un perfil que tiene una secuencia de audio y una secuencia de vídeo, el filtro creará un PIN de entrada de audio y vídeo, y ambos PIN deben estar conectados para poder ejecutar el filtro.

Agregar extensiones de unidad de datos

Puede configurar una secuencia de perfil para las extensiones de unidad de datos, como los códigos de tiempo SMPTE, antes o después de que se conecte el filtro, siempre que siga este orden de operaciones:

1.  Agregue una o más extensiones de unidad de datos a la secuencia mediante [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).
2.  Llame a [**WMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) para actualizar el perfil.
3.  Llame a [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) con el objeto de perfil actualizado.
4.  Busque el PIN de entrada de vídeo y llame a su método [**IAMWMBufferPass:: SetNotify**](iamwmbufferpass-setnotify.md) para registrar la interfaz [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) definida por la aplicación.

Cuando se ejecute el gráfico, se llamará al método [**IAMWMBufferPassCallback:: Notify**](iamwmbufferpasscallback-notify.md) para cada fotograma y podrá obtener y establecer propiedades en el ejemplo mediante sus métodos de interfaz [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) .

> [!Note]  
> En algunos escenarios de uso intensivo del procesador, como el Telecine inverso, el escritor ASF de WM puede requerir más búferes de salida de los que pueden admitir algunos filtros de nivel inferior. Por ejemplo, el descodificador de DV no aceptará más de un búfer para su PIN de salida y se aplica lo mismo para el descompresor de AVI en determinadas condiciones. Si surgen problemas al intentar conectarse a estos filtros o, posiblemente, al ejecutar el gráfico, puede que sea necesario escribir un filtro intermediario que acepte cualquier número de búferes en su PIN de salida.

 

 

 