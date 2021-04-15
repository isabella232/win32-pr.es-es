---
description: Configuración del escritor ASF
ms.assetid: 5708c4a0-6197-4a42-adfd-01c6dfe86302
title: Configuración del escritor ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a6dfc1827743dce946188ebf9e050226b5c484
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666121"
---
# <a name="configuring-the-asf-writer"></a>Configuración del escritor ASF

Cuando se crea el filtro de [escritura ASF de WM](wm-asf-writer-filter.md) , se configura automáticamente con el \_ perfil 256Video de V80 de WMProfile \_ . Este perfil usa los códecs Windows Media Audio y Windows Media Video versión 8, que no son tan recientes como los códecs de la serie Windows Media 9. Se recomienda crear un perfil personalizado que use los códecs de la serie Windows Media 9 y configurar el escritor ASF de WM con el perfil personalizado, tal y como se describe en [configuración de perfiles y otras propiedades de archivo ASF](configuring-profiles-and-other-asf-file-properties.md). Debe agregar el filtro de escritor ASF de WM al gráfico de filtro antes de configurar el filtro, y configurar el filtro antes de conectarlo a cualquier otro filtro.

Todos los datos de entrada deben tener una marca de tiempo y todos los pin de entrada deben estar conectados para poder ejecutar o pausar el filtro. Por lo tanto, si configura el filtro con un perfil que tiene una secuencia de audio y una secuencia de vídeo, el filtro creará un PIN de entrada de audio y vídeo, y ambos PIN deben estar conectados para poder ejecutar el filtro. Dado que el SDK de Windows Media Format requiere que una secuencia de audio funcione, el escritor ASF de WM siempre debe tener un PIN de audio de entrada, incluso si se trata de un flujo ficticio, es decir, una secuencia de audio silenciada y de velocidad de bits baja.

Agregar extensiones de unidad de datos

Puede configurar una secuencia de perfil para las extensiones de unidad de datos, como los códigos de tiempo SMPTE, antes o después de que se conecte el filtro, siempre que siga este orden de operaciones:

1.  Agregue una o más extensiones de unidad de datos a la secuencia mediante **IWMStreamConfig2:: AddDataUnitExtension**.
2.  Llame a **IWMProfile:: ReconfigStream** para actualizar el perfil.
3.  Llame a [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) con el objeto de perfil actualizado.
4.  Busque el PIN de entrada de vídeo y llame a su método [**IAMWMBufferPass:: SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) para registrar la interfaz [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) definida por la aplicación.

Cuando se ejecute el gráfico, se llamará al método [**IAMWMBufferPassCallback:: Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) para cada fotograma y podrá obtener y establecer propiedades en el ejemplo mediante sus métodos de interfaz **INSSBuffer3** .

> [!Note]  
> En algunos escenarios de uso intensivo del procesador, como el Telecine inverso, el escritor ASF de WM puede requerir más búferes de salida de los que pueden admitir algunos filtros de nivel inferior. Por ejemplo, el descodificador de DV no aceptará más de un búfer para su PIN de salida y se aplica lo mismo para el descompresor de AVI en determinadas condiciones. Si surgen problemas al intentar conectarse a estos filtros o, posiblemente, al ejecutar el gráfico, puede que sea necesario escribir un filtro intermediario que acepte cualquier número de búferes en su PIN de salida.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear archivos ASF en DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



