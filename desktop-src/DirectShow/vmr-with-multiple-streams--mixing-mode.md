---
description: VMR con varias secuencias (modo de combinación)
ms.assetid: 053edb70-8631-4fe4-a137-2fe54e02ab9e
title: VMR con varias secuencias (modo de combinación)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21a954b0ad78afbceabf0fde493f920961b90dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678075"
---
# <a name="vmr-with-multiple-streams-mixing-mode"></a>VMR con varias secuencias (modo de combinación)

VMR puede representar varios flujos de entrada. En esta configuración, denominada modo de combinación, VMR carga su mezclador y compositor para realizar la combinación y la mezcla antes de la representación. Se puede usar el modo de combinación mientras VMR está en modo de ventana o modo sin ventanas.

El modo de mezcla requiere que el controlador de gráficos admita las \_ marcas de capacidad DDCAPS BLTFOURCC y DDCAPS \_ BLTSTRETCH (conversión de espacio de colores y Stretch blitting, respectivamente). Casi todos los controladores de gráficos nuevos tienen esas capacidades. Además, el controlador debe admitir la creación de destinos de representación de Direct3D para la profundidad del píxel de la pantalla actual. Algunos dispositivos no admiten las operaciones de Direct3D cuando la pantalla se establece en 24 bits por píxel. Para obtener más información, consulte la documentación del SDK de gráficos de DirectX.

> [!Note]  
> Cuando el VMR mezcla varias secuencias de vídeo, el gráfico de filtros no se busca correctamente. Si necesita buscar varias secuencias de vídeo, debe crear gráficos de filtro independientes que compartan el mismo objeto de presentador personalizado.

 

**Configuración de VMR-7 para varias secuencias**

Para representar varios flujos de entrada con VMR-7, haga lo siguiente:

1.  Antes de conectar cualquiera de los pin de entrada de VMR, llame al método [**IVMRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams) con el número de flujos. Esto hace que VMR cargue el mezclador y el compositor, y para crear el número especificado de clavijas de entrada.
2.  Llame a [**IVMRFilterConfig:: SetRenderingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingprefs) para especificar varias preferencias de representación.
3.  Conecte los pin a los filtros de nivel superior. La forma más fácil de hacerlo es llamar a [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) para cada flujo de entrada. Si el PIN de salida en el filtro de nivel superior (normalmente un descodificador) y el PIN de entrada en VMR no pueden estar de acuerdo en una conexión, se creará una nueva instancia de VMR con la configuración predeterminada. Esto producirá una nueva ventana con "ActiveMovie" en la barra de título. Para evitar que esto suceda, la aplicación siempre debe comprobar que se está usando la instancia correcta de VMR llamando a un método como [**IPin:: ConnectTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto). Otra opción consiste en agregar el filtro de origen y, a continuación, conectar los pin mediante **IGraphBuilder:: Connect**.
4.  Use la interfaz [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) en VMR para controlar los parámetros de cada secuencia, como el valor alfa, el orden Z y el rectángulo de salida.
5.  Ejecute el gráfico de filtro.

**Configuración de VMR-9 para varias secuencias**

De forma predeterminada, VMR-9 crea cuatro clavijas de entrada. Si desea mezclar más de cuatro transmisiones de vídeo, llame a [**IVMRFilterConfig9:: SetNumberOfStreams**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setnumberofstreams) antes de conectar cualquier clavija de entrada. Use la interfaz [**IVMRMixerControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9) para establecer los parámetros de flujo, como alfa, orden Z y posición.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el modo de mezcla de VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



