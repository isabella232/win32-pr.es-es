---
title: Interfaz ID3DX11ThreadPump (D3DX11core.h)
description: Un bombeo de subprocesos ejecuta tareas de forma asincrónica.
ms.assetid: 1a99f728-149d-4800-a6e4-e3a00cf8cf4f
keywords:
- Interfaz ID3DX11ThreadPump Direct3D 11
- Interfaz ID3DX11ThreadPump Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06f50e489503d02a6ea772be65678022dd36f6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566693"
---
# <a name="id3dx11threadpump-interface"></a>Interfaz ID3DX11ThreadPump

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para las aplicaciones de Windows Store.

 

Un bombeo de subprocesos ejecuta tareas de forma asincrónica. Se crea llamando a [**D3DX11CreateThreadPump.**](d3dx11createthreadpump.md) Hay varias API que toman una bomba de subprocesos opcional como parámetro, como [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) y [**D3DX11CompileFromFile**](d3dx11compilefromfile.md); Si pasa una interfaz de bombeo de subprocesos a estas API, las funciones se ejecutarán de forma asincrónica en un subproceso independiente. Especialmente en máquinas con varios procesadores, una bomba de subprocesos puede cargar recursos y procesar datos sin una disminución notable del rendimiento.

## <a name="members"></a>Members

La **interfaz ID3DX11ThreadPump** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ID3DX11ThreadPump** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX11ThreadPump** tiene estos métodos.




| Método | Descripción | 
|--------|-------------|
| <a href="id3dx11threadpump-addworkitem.md"><strong>AddWorkItem</strong></a> | <blockquote>[!Note]<br />La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para las aplicaciones de Windows Store.</blockquote><br /> Agrega un elemento de trabajo al bombeo de subprocesos.<br /> | 
| <a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a> | <blockquote>[!Note]<br />La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para las aplicaciones de Windows Store.</blockquote><br /> Obtiene el número de elementos de cada una de las tres colas dentro de la bomba de subprocesos.<br /> | 
| <a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a> | <blockquote>[!Note]<br />La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para las aplicaciones de Windows Store.</blockquote><br /> Obtiene el número de elementos de trabajo en el bombeo de subprocesos.<br /> | 
| <a href="id3dx11threadpump-processdeviceworkitems.md"><strong>ProcessDeviceWorkItems</strong></a> | <blockquote>[!Note]<br />La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para las aplicaciones de Windows Store.</blockquote><br /> Establece los elementos de trabajo en el dispositivo una vez que han terminado de cargarse y procesarse.<br /> | 
| <a href="id3dx11threadpump-purgeallitems.md"><strong>PurgeAllItems</strong></a> | <blockquote>[!Note]<br />La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para las aplicaciones de Windows Store.</blockquote><br /> Borra todos los elementos de trabajo de la bomba de subprocesos.<br /> | 
| <a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a> | <blockquote>[!Note]<br />La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para las aplicaciones de Windows Store.</blockquote><br /> Espera a que finalicen todos los elementos de trabajo de la bomba de subprocesos.<br /> | 




 

## <a name="remarks"></a>Observaciones

### <a name="using-a-thread-pump"></a>Uso de una bomba de subprocesos

La bomba de subprocesos carga y procesa los datos mediante el siguiente proceso de tres pasos:

1.  Cargue y descomprima los datos con un cargador [**de datos**](id3dx11dataloader.md). El objeto del cargador de datos tiene tres métodos a los que llamará internamente el bombeo de subprocesos mientras carga y descomprime los datos: [**ID3DX11DataLoader::Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader::D ecompress**](id3dx11dataloader-decompress.md)e [**ID3DX11DataLoader::D estroy**](id3dx11dataloader-destroy.md). La funcionalidad específica de estas tres API difiere en función del tipo de datos que se cargan y descomprimen. La interfaz del cargador de datos también se puede heredar y sus API se pueden cambiar si se carga un archivo de datos definido en el propio formato personalizado.
2.  Procese los datos con un [**procesador de datos**](id3dx11dataprocessor.md). El objeto de procesador de datos tiene tres métodos a los que llamará internamente el bombeo de subprocesos mientras procesa los datos: [**ID3DX11DataProcessor::P rocess,**](id3dx11dataprocessor-process.md) [**ID3DX11DataProcessor::CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)y [**ID3DX11DataProcessor::D estroy**](id3dx11dataprocessor-destroy.md). La forma en que procesa los datos será diferente en función del tipo de datos. Por ejemplo, si los datos son una textura almacenada como JPEG, [**ID3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md) realizará la descompresión JPEG para obtener los bits de imagen sin procesar de la imagen. Si los datos son un sombreador, [**ID3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md) compilará hlsl en código de bytes. Una vez procesados los datos, se creará un objeto de dispositivo para los datos (con [**ID3DX11DataProcessor::CreateDeviceObject)**](id3dx11dataprocessor-createdeviceobject.md)y el objeto se agregará a una cola de objetos de dispositivo. La interfaz del procesador de datos también se puede heredar y sus API se pueden cambiar si se está procesando un archivo de datos definido en su propio formato personalizado.
3.  Enlace el objeto de dispositivo al dispositivo. Esto se hace cuando la aplicación llama a [**ID3DX11ThreadPump::P rocessDeviceWorkItems**](id3dx11threadpump-processdeviceworkitems.md), que enlazará un número especificado de objetos de la cola de objetos de dispositivo al dispositivo.

El bombeo de subprocesos se puede usar para cargar datos de dos maneras: llamando a una API que toma un bombeo de subprocesos como parámetro, como [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) y [**D3DX11CompileFromFile**](d3dx11compilefromfile.md), o llamando a [**ID3DX11ThreadPump::AddWorkItem**](id3dx11threadpump-addworkitem.md). En el caso de las API que toman una bomba de subprocesos, el cargador de datos y el procesador de datos se crean internamente. En el caso de AddWorkItem, el cargador de datos y el procesador de datos deben crearse con antelación y, a continuación, pasarse a AddWorkItem. D3DX11 proporciona un conjunto de API para crear cargadores de datos y procesadores de datos que tienen funcionalidad para cargar y procesar formatos de datos comunes. En el caso de los formatos de datos personalizados, se deben heredar las interfaces del cargador de datos y del procesador de datos y se deben volver a definir sus métodos.

El objeto de bombeo de subprocesos ocupa una cantidad considerable de recursos, por lo que generalmente solo se debe crear uno por aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>D3DX11core.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

