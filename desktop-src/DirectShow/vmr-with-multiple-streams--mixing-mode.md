---
description: VMR con varias Secuencias (modo de combinación)
ms.assetid: 053edb70-8631-4fe4-a137-2fe54e02ab9e
title: VMR con varias Secuencias (modo de combinación)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f958d8c95372325229dffc1cc37aff579213c48940f93ad090d0fbd9359b79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290785"
---
# <a name="vmr-with-multiple-streams-mixing-mode"></a>VMR con varias Secuencias (modo de combinación)

VmR puede representar varios flujos de entrada. En esta configuración, denominada modo de combinación, vmr carga su mezclador y compositor para realizar la mezcla y la mezcla antes de la representación. El modo de combinación se puede usar mientras vmr está en modo de ventana o sin ventana.

El modo de combinación requiere que el controlador de gráficos admita las marcas de funcionalidad DDCAPS \_ BLTFOURCC y DDCAPS BLTSTRETCH (conversión de espacio de color y borrado \_ elástico, respectivamente). Casi todos los controladores de gráficos nuevos tienen esas funcionalidades. Además, el controlador debe admitir la creación de destinos de representación de Direct3D para la profundidad de píxeles de presentación actual. Algunos dispositivos no admiten operaciones de Direct3D cuando la pantalla está establecida en 24 bits por píxel. Para más información, consulte la documentación del SDK de gráficos de DirectX.

> [!Note]  
> Cuando vmr mezcla varias secuencias de vídeo, el gráfico de filtros no busca correctamente. Si necesita buscar varias secuencias de vídeo, debe crear gráficos de filtro independientes que compartan el mismo objeto personalizado allocator-presenter.

 

**Configuración de VMR-7 para varias Secuencias**

Para representar varios flujos de entrada con VMR-7, haga lo siguiente:

1.  Antes de conectar cualquiera de los pines de entrada de VMR, llame al método [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams) con el número de secuencias. Esto hace que vmr cargue el mezclador y el compositor y cree el número especificado de pines de entrada.
2.  Llame [**a IVMRFilterConfig::SetRenderingPrefs para**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingprefs) especificar varias preferencias de representación.
3.  Conectar los pines a los filtros ascendentes. La manera más fácil de hacerlo es llamar a [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) para cada flujo de entrada. Si el pin de salida del filtro ascendente (normalmente un descodificador) y el pin de entrada del VMR no pueden coincidir en una conexión, se creará una nueva instancia de VMR con la configuración predeterminada. Esto dará como resultado una nueva ventana con "ActiveMovie" en la barra de título. Para evitar que esto suceda, la aplicación siempre debe comprobar que se está utilizando la instancia correcta de VMR mediante una llamada a un método como [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto). Otra opción es agregar el filtro de origen y, a continuación, conectar los pines **mediante IGraphBuilder::Conectar**.
4.  Use la [**interfaz IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) en vmr para controlar los parámetros de cada secuencia, como el valor alfa, la ordenación Z y el rectángulo de salida.
5.  Ejecute el gráfico de filtro.

**Configuración de VMR-9 para varias Secuencias**

De forma predeterminada, VMR-9 crea cuatro pines de entrada. Si desea mezclar más de cuatro secuencias de vídeo, llame a [**IVMRFilterConfig9::SetNumberOfStreams**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setnumberofstreams) antes de conectar los pines de entrada. Use la [**interfaz IVMRMixerControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9) para establecer los parámetros de flujo, como alfa, orden Z y posición.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del modo de combinación de VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



