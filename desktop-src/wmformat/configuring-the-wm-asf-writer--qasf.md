---
title: Configuración de WM ASF Writer (QASF)
description: Configuración de WM ASF Writer (QASF)
ms.assetid: 0f49ed5a-c228-456a-9551-8d277adccd0e
keywords:
- Windows SDK de formato multimedia, configuración de WM ASF Writer (QASF)
- Windows SDK de formato multimedia, DirectShow
- Windows SDK de formato multimedia,WM ASF Writer
- Windows SDK de formato multimedia, QASF
- Formato de sistemas avanzados (ASF), configurar WM ASF Writer (QASF)
- ASF (formato de sistemas avanzados), configurar WM ASF Writer (QASF)
- Advanced Systems Format (ASF),WM ASF Writer
- ASF (formato de sistemas avanzados),WM ASF Writer
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados),DirectShow
- Formato de sistemas avanzados (ASF),QASF
- ASF (formato de sistemas avanzados),QASF
- DirectShow,configuring WM ASF Writer (QASF)
- DirectShow,WM ASF Writer
- DirectShow,QASF
- WM ASF Writer, configurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba4559fc1780bdb9a9b398471cc842e2f3cf46f9c84a483229b01b3b6fa4a1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199181"
---
# <a name="configuring-the-wm-asf-writer-qasf"></a>Configuración de WM ASF Writer (QASF)

Cuando se crea el filtro [WM ASF Writer,](wm-asf-writer-filter.md) se configura automáticamente con el perfil WMProfile \_ V80 \_ 256Video como valor predeterminado. Dado que este perfil usa los códecs Windows Media Audio y Windows Media Video versión 8, se recomienda crear un perfil personalizado que use los códecs de la serie Windows Media 9 y, a continuación, pasar su puntero [**IWMProfile**](iwmprofile.md) al filtro mediante el método [**IConfigAsfWriter::ConfigureFilterUsingProfile.**](iconfigasfwriter-configurefilterusingprofile.md) El filtro debe agregarse al gráfico antes de configurar el filtro y debe configurarse para poder conectarse a los filtros ascendentes. El filtro usa el perfil para determinar qué tipo de archivo de formato multimedia se va Windows escribir, cuántos pines de entrada se configurarán y qué tipos de medios pueden aceptar los pines.

El filtro permite restablecer los perfiles mientras sus pines de entrada están conectados, siempre y cuando el nuevo perfil no requiera ningún pin de entrada adicional. Por ejemplo, si cambia el perfil de un perfil de solo audio de una entrada a un perfil de audio y vídeo de dos entradas, solo se volverá a conectar la clavija de audioTodos los datos de entrada deben tener marca de tiempo y todas las marcas de entrada deben estar conectadas antes de que se pueda ejecutar o pausar el filtro. Esto significa que si configura el filtro con un perfil que tiene una secuencia de audio y una secuencia de vídeo, el filtro creará un pin de entrada de audio y vídeo, y ambos pins deben estar conectados antes de que se pueda ejecutar el filtro.

Agregar extensiones de unidad de datos

Puede configurar un flujo de perfil para las extensiones de unidad de datos, como los códigos de tiempo de SMPTE, antes o después de conectar el filtro, siempre que siga este orden de operaciones:

1.  Agregue una o varias extensiones de unidad de datos a la secuencia [**mediante IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).
2.  Llame [**a WMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) para actualizar el perfil.
3.  Llame [**a IConfigAsfWriter::ConfigureFilterUsingProfile con**](iconfigasfwriter-configurefilterusingprofile.md) el objeto de perfil actualizado.
4.  Busque el pin de entrada de vídeo y llame a su [**método IAMWMBufferPass::SetNotify**](iamwmbufferpass-setnotify.md) para registrar la interfaz [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) definida por la aplicación.

Cuando se ejecuta el gráfico, se llamará al método [**IAMWMBufferPassCallback::Notify**](iamwmbufferpasscallback-notify.md) para cada fotograma y podrá obtener y establecer propiedades en el ejemplo mediante sus métodos de interfaz [**INSSBuffer3.**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)

> [!Note]  
> En algunos escenarios con un uso intensivo del procesador, como la tele telefónica inversa, WM ASF Writer puede requerir más búferes de salida de los que pueden admitir algunos filtros de bajada. El descodificador DV, por ejemplo, no aceptará más de un búfer para su pin de salida y lo mismo sucede con el descomprimidor AVI en determinadas condiciones. Si tiene problemas al intentar conectarse a estos filtros o, posiblemente, al ejecutar el gráfico, puede ser necesario escribir un filtro intermedio que acepte cualquier número de búferes en su pin de salida.

 

 

 