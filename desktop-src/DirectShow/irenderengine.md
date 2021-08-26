---
description: 'La interfaz IRenderEngine representa un proyecto DirectShow Editing Services (DES) mediante la construcción de un gráfico de filtros a partir de una escala de tiempo. DES proporciona dos componentes que implementan esta interfaz: el motor de representación básico crea una salida sin comprimir.'
ms.assetid: e2a91b34-ee4d-405e-81bf-29d15ea6342a
title: Interfaz IRenderEngine (Qedit.h)
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
ms.openlocfilehash: a13d51eb41a917dc4790c75a8a1f8a881dbcb8489364722ff8805bdf26fc77f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051315"
---
# <a name="irenderengine-interface"></a>IRenderEngine (interfaz)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `IRenderEngine` interfaz representa un proyecto DirectShow Editing [Services](directshow-editing-services.md) (DES) mediante la construcción de un gráfico de filtros a partir de una escala de tiempo.

DES proporciona dos componentes que implementan esta interfaz:

-   El *motor de representación básico* crea una salida sin comprimir. Puede usar la salida para la versión preliminar o enrutarla a través de filtros de compresión y escribirla en un archivo.
-   El *motor de representación inteligente* crea una salida comprimida mediante la *recompresión inteligente*. Con la recompresión inteligente, un archivo de origen se vuelve a comprimir solo si su formato difiere del formato de salida. Un origen con un formato de coincidencia se escribe directamente en el archivo de salida. En función del escenario, la recompresión inteligente puede mejorar enormemente el tiempo de representación.

El motor de representación inteligente también admite la [**interfaz ISmartRenderEngine.**](ismartrenderengine.md)

Aunque una aplicación puede crear un gráfico de filtros y pasarlo a un motor de representación, el escenario típico es que el motor de representación cree el gráfico de filtros. La creación del gráfico es un proceso de dos fases. En primer lugar, compile el front-end mediante una llamada [**al método IRenderEngine::ConnectFrontEnd.**](irenderengine-connectfrontend.md) A continuación, conecte los pines de salida del front-end a los filtros de representación deseados:

-   Representadores de vídeo y audio para la versión preliminar o
-   Escritores, multiplexores y escritores de archivos para generar la salida final.

## <a name="members"></a>Miembros

La **interfaz IRenderEngine** hereda de [**la interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IRenderEngine** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IRenderEngine** tiene estos métodos.



| Método                                                                             | Descripción                                                                           |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Cometer**](irenderengine-commit.md)                                             | Sin implementar.<br/>                                                           |
| [**ConnectFrontEnd**](irenderengine-connectfrontend.md)                           | Compila el front-end del gráfico de filtros a partir de la escala de tiempo actual.<br/>        |
| [**Desacomprimido**](irenderengine-decommit.md)                                         | Sin implementar.<br/>                                                           |
| [**DoSmartRecompression**](irenderengine-dosmartrecompression.md)                 | No compatible.<br/>                                                             |
| [**GetCaps**](irenderengine-getcaps.md)                                           | Sin implementar.<br/>                                                           |
| [**GetFilterGraph**](irenderengine-getfiltergraph.md)                             | Recupera el gráfico de filtro que ha construido el motor de representación, si lo hay.<br/> |
| [**GetGroupOutputPin**](irenderengine-getgroupoutputpin.md)                       | Recupera el pin de salida para el grupo especificado.<br/>                          |
| [**GetTimelineObject**](irenderengine-gettimelineobject.md)                       | Recupera la escala de tiempo que el motor de representación está usando actualmente.<br/>          |
| [**GetVendorString**](irenderengine-getvendorstring.md)                           | Recupera la cadena de proveedor.<br/>                                               |
| [**RenderOutputPins**](irenderengine-renderoutputpins.md)                         | Crea la parte de vista previa del gráfico de filtro.<br/>                        |
| [**ScrapIt**](irenderengine-scrapit.md)                                           | Descarta el gráfico de filtros del motor de representación y todos los objetos asociados.<br/>      |
| [**SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)         | Establece el nivel de reconexión dinámica durante la representación.<br/>                   |
| [**SetFilterGraph**](irenderengine-setfiltergraph.md)                             | Especifica un gráfico de filtros para el motor de representación que se usará.<br/>                     |
| [**SetInterestRange**](irenderengine-setinterestrange.md)                         | No compatible.<br/>                                                             |
| [**SetInterestRange2**](irenderengine-setinterestrange2.md)                       | No compatible.<br/>                                                             |
| [**SetRenderRange**](irenderengine-setrenderrange.md)                             | Establece el intervalo de tiempo que se va a representar.<br/>                                     |
| [**SetRenderRange2**](irenderengine-setrenderrange2.md)                           | Establece el intervalo de tiempo que se va a representar, como **un valor double.**<br/>                    |
| [**SetSourceConnectCallback**](irenderengine-setsourceconnectcallback.md)         | No compatible.<br/>                                                             |
| [**SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md)           | Especifica cómo el motor de representación valida los nombres de archivo.<br/>                      |
| [**SetTimelineObject**](irenderengine-settimelineobject.md)                       | Establece la escala de tiempo que usará el motor de representación.<br/>                            |
| [**UseInSmartRecompressionGraph**](irenderengine-useinsmartrecompressiongraph.md) | No compatible.<br/>                                                             |



 

## <a name="remarks"></a>Comentarios

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Representación de un Project](rendering-a-project.md)
</dt> </dl>

 

 
