---
description: 'La interfaz IRenderEngine representa un proyecto de servicios de edición de DirectShow (DES) mediante la creación de un gráfico de filtro a partir de una escala de tiempo. DES proporciona dos componentes que implementan esta interfaz: el motor de representación básico crea una salida sin comprimir.'
ms.assetid: e2a91b34-ee4d-405e-81bf-29d15ea6342a
title: Interfaz IRenderEngine (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d8c57e976fac877a02c3f3993fb3fe4d27f9033b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681027"
---
# <a name="irenderengine-interface"></a>Interfaz IRenderEngine

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IRenderEngine` interfaz representa un proyecto de [servicios de edición de DirectShow](directshow-editing-services.md) (des) mediante la creación de un gráfico de filtro a partir de una escala de tiempo.

DES proporciona dos componentes que implementan esta interfaz:

-   El *motor de representación básico* crea una salida sin comprimir. Puede usar la salida de la vista previa o enrutarla a través de filtros de compresión y escribirla en un archivo.
-   El *motor de representación inteligente* crea una salida comprimida mediante la *recompresión inteligente*. Con la recompresión inteligente, un archivo de código fuente se vuelve a comprimir solo si su formato difiere del formato de salida. Un origen con un formato coincidente se escribe directamente en el archivo de salida. Dependiendo del escenario, la recompresión inteligente puede mejorar considerablemente el tiempo de representación.

El motor de representación inteligente también admite la interfaz [**ISmartRenderEngine**](ismartrenderengine.md) .

Aunque una aplicación puede crear un gráfico de filtro y pasarlo a un motor de representación, el escenario típico es que el motor de representación cree el gráfico de filtro. La compilación del gráfico es un proceso de dos fases. En primer lugar, compile el front-end llamando al método [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) . A continuación, conecte los terminales de salida en el front-end a los filtros de representación deseados:

-   Representadores de vídeo y audio para la versión preliminar, o
-   Compresores, Multiplexores y escritores de archivos para generar la salida final.

## <a name="members"></a>Miembros

La interfaz **IRenderEngine** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IRenderEngine** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IRenderEngine** tiene estos métodos.



| Método                                                                             | Descripción                                                                           |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Promete**](irenderengine-commit.md)                                             | Sin implementar.<br/>                                                           |
| [**ConnectFrontEnd**](irenderengine-connectfrontend.md)                           | Crea el front-end del gráfico de filtro a partir de la escala de tiempo actual.<br/>        |
| [**Anular**](irenderengine-decommit.md)                                         | Sin implementar.<br/>                                                           |
| [**DoSmartRecompression**](irenderengine-dosmartrecompression.md)                 | No se admite.<br/>                                                             |
| [**GetCaps**](irenderengine-getcaps.md)                                           | Sin implementar.<br/>                                                           |
| [**GetFilterGraph**](irenderengine-getfiltergraph.md)                             | Recupera el gráfico de filtro que el motor de representación ha construido, si existe.<br/> |
| [**GetGroupOutputPin**](irenderengine-getgroupoutputpin.md)                       | Recupera el PIN de salida para el grupo especificado.<br/>                          |
| [**GetTimelineObject**](irenderengine-gettimelineobject.md)                       | Recupera la escala de tiempo que el motor de representación está usando actualmente.<br/>          |
| [**GetVendorString**](irenderengine-getvendorstring.md)                           | Recupera la cadena de proveedor.<br/>                                               |
| [**RenderOutputPins**](irenderengine-renderoutputpins.md)                         | Crea la parte de vista previa del gráfico de filtro.<br/>                        |
| [**ScrapIt**](irenderengine-scrapit.md)                                           | Descarta el gráfico de filtro del motor de representación y todos los objetos asociados.<br/>      |
| [**SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)         | Establece el nivel de reconexión dinámica durante la representación.<br/>                   |
| [**SetFilterGraph**](irenderengine-setfiltergraph.md)                             | Especifica un gráfico de filtro para que lo use el motor de representación.<br/>                     |
| [**SetInterestRange**](irenderengine-setinterestrange.md)                         | No se admite.<br/>                                                             |
| [**SetInterestRange2**](irenderengine-setinterestrange2.md)                       | No se admite.<br/>                                                             |
| [**SetRenderRange**](irenderengine-setrenderrange.md)                             | Establece el intervalo de tiempo que se va a representar.<br/>                                     |
| [**SetRenderRange2**](irenderengine-setrenderrange2.md)                           | Establece el intervalo de tiempo que se va a representar, como un **valor de tipo Double**.<br/>                    |
| [**SetSourceConnectCallback**](irenderengine-setsourceconnectcallback.md)         | No se admite.<br/>                                                             |
| [**SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md)           | Especifica cómo valida el motor de representación los nombres de archivo.<br/>                      |
| [**SetTimelineObject**](irenderengine-settimelineobject.md)                       | Establece la escala de tiempo que va a usar el motor de representación.<br/>                            |
| [**UseInSmartRecompressionGraph**](irenderengine-useinsmartrecompressiongraph.md) | No se admite.<br/>                                                             |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Representar un proyecto](rendering-a-project.md)
</dt> </dl>

 

 
