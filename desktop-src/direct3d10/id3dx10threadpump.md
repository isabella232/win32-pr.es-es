---
description: Se utiliza para ejecutar tareas de forma asincrónica y se crean con D3DX10CreateThreadPump.
ms.assetid: 8d03c94a-9b64-464c-b0f4-4e5f5a00503f
title: Interfaz ID3DX10ThreadPump (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9fe3f0ca5955963864ef18de5d86fe03083d3f3b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157260"
---
# <a name="id3dx10threadpump-interface"></a>Interfaz ID3DX10ThreadPump

Se utiliza para ejecutar tareas de forma asincrónica y se crean con [**D3DX10CreateThreadPump**](d3dx10createthreadpump.md). Hay varias API de D3DX10 que, opcionalmente, pueden tomar un bombeo de subprocesos como parámetro, como [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) y [**D3DX10CompileFromFile**](d3dx10compilefromfile.md) (consulte la sección Comentarios para obtener una lista completa). Si el bombeo de subprocesos se pasa a estas API, se ejecutarán de forma asincrónica en un subproceso de bombeo de subprocesos independiente. La ventaja de hacerlo es que puede hacer que la carga y el procesamiento de grandes cantidades de datos se produzcan sin ver una ralentización del rendimiento en la pantalla.

## <a name="members"></a>Miembros

La interfaz **ID3DX10ThreadPump** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10ThreadPump** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DX10ThreadPump** tiene estos métodos.



| Método                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddWorkItem**](id3dx10threadpump-addworkitem.md)                       | Agregue un elemento de trabajo al bombeo de subprocesos.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**GetQueueStatus**](id3dx10threadpump-getqueuestatus.md)                 | Obtiene el número de elementos de cada una de las tres colas dentro del bombeo de subprocesos.<br/>                                                                                                                                                                                                                                                                                                                                           |
| [**GetWorkItemCount**](id3dx10threadpump-getworkitemcount.md)             | Obtiene el número de elementos de trabajo actualmente en el bombeo de subprocesos.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| [**ProcessDeviceWorkItems**](id3dx10threadpump-processdeviceworkitems.md) | Establezca los elementos de trabajo en el dispositivo una vez que hayan finalizado la carga y el procesamiento. Cuando el bombeo de subprocesos ha terminado de cargar y procesar un recurso o sombreador, lo mantendrá en una cola hasta que se llame a esta API, momento en que los elementos procesados se establecerán en el dispositivo. Esto resulta útil para controlar la cantidad de procesamiento que se emplea en los recursos de enlace al dispositivo para cada fotograma. Vea Notas.<br/> |
| [**PurgeAllItems**](id3dx10threadpump-purgeallitems.md)                   | Borre todos los elementos de trabajo del bombeo de subprocesos.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**WaitForAllItems**](id3dx10threadpump-waitforallitems.md)               | Esperar a que finalicen todos los elementos de trabajo en el bombeo de subprocesos.<br/>                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Observaciones

El bombeo de subprocesos carga y procesa los datos en un proceso de tres pasos. Va:

1.  Cargar y descomprimir los datos con un cargador de datos. El objeto del cargador de datos tiene tres métodos a los que el bombeo de subprocesos llamará internamente a medida que se cargan y descomprimen los datos: [**ID3DX10DataLoader:: Load**](id3dx10dataloader-load.md), [**ID3DX10DataLoader::D ecompress**](id3dx10dataloader-decompress.md)y [**ID3DX10DataLoader::D estroy**](id3dx10dataloader-destroy.md). La funcionalidad específica de estas tres API varía en función del tipo de datos que se cargan y descomprimen. También se puede heredar la interfaz del cargador de datos y se pueden cambiar sus API si se está cargando un archivo de datos definido en un formato personalizado propio.
2.  Procese los datos con un procesador de datos. El objeto de procesador de datos tiene tres métodos a los que el bombeo de subprocesos llamará internamente a medida que procesa los datos: [**ID3DX10DataProcessor::P rador**](id3dx10dataprocessor-process.md), [**ID3DX10DataProcessor:: CreateDeviceObject**](id3dx10dataprocessor-createdeviceobject.md)y [**ID3DX10DataProcessor::D estroy**](id3dx10dataprocessor-destroy.md). La forma en que se procesan los datos será diferente en función del tipo de datos. Por ejemplo, si los datos son una textura almacenada como JPEG, **ID3DX10DataProcessor::P rador** realizará la descompresión JPEG para obtener los bits de imagen sin formato de la imagen. Si los datos son un sombreador, **ID3DX10DataProcessor::P rador** compilará el HLSL en código de bytes. Una vez procesados los datos, se creará un objeto de dispositivo para esos datos (con **ID3DX10DataProcessor:: CreateDeviceObject**) y el objeto se agregará a una cola de objetos de dispositivo. También se puede heredar la interfaz del procesador de datos y se pueden cambiar sus API si se está procesando un archivo de datos definido en un formato personalizado propio.
3.  Enlazar el objeto de dispositivo al dispositivo. Esto se hace cuando una aplicación de una de las llamadas a [**ID3DX10ThreadPump::P rocessdeviceworkitems**](id3dx10threadpump-processdeviceworkitems.md), que enlazará un número especificado de objetos en la cola de objetos de dispositivo al dispositivo.

El bombeo de subprocesos se puede utilizar para cargar datos de una de las dos maneras siguientes: llamando a una API que toma un bombeo de subprocesos como parámetro, como [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) y [**D3DX10CompileFromFile**](d3dx10compilefromfile.md), o llamando a [**ID3DX10ThreadPump:: AddWorkItem**](id3dx10threadpump-addworkitem.md). En el caso de las API que toman un bombeo de subprocesos, el cargador de datos y el procesador de datos se crean internamente. En el caso de **AddWorkItem**, el cargador de datos y el procesador de datos se deben crear de antemano y, a continuación, pasarse a AddWorkItem. D3DX10 proporciona un conjunto de API para crear cargadores de datos y procesadores de datos que tienen funcionalidad para cargar y procesar formatos de datos comunes (consulte la sección Comentarios para obtener una lista completa de las API). En el caso de los formatos de datos personalizados, las interfaces del cargador de datos y del procesador de datos deben heredarse y sus métodos deben redefinirse.

El objeto de bombeo de subprocesos ocupa una cantidad considerable de recursos, por lo que generalmente solo se debe crear uno por aplicación.

Cargadores de datos D3DX10 integrados



|                                                                            |                                          |
|----------------------------------------------------------------------------|------------------------------------------|
| [**D3DX10CreateAsyncFileLoader**](d3dx10createasyncfileloader.md)         | Cree un cargador de archivos de forma asincrónica.     |
| [**D3DX10CreateAsyncMemoryLoader**](d3dx10createasyncmemoryloader.md)     | Cree un cargador de datos de forma asincrónica.     |
| [**D3DX10CreateAsyncResourceLoader**](d3dx10createasyncresourceloader.md) | Cree un cargador de recursos de forma asincrónica. |



 

Procesadores de datos D3DX10 integrados



|                                                                                                  |                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md)                   | Cree un procesador de datos para usarlo con un bombeo de subprocesos. Esta API es similar a D3DX10CreateAsyncTextureInfoProcessor, pero también carga la textura. |
| [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md)           | Cree un procesador de datos para usarlo con un bombeo de subprocesos.                                                                                             |
| [**D3DX10CreateAsyncShaderCompilerProcessor**](d3dx10createasyncshadercompilerprocessor.md)     | Compilar un sombreador y crear un procesador de datos de forma asincrónica.                                                                                       |
| [**D3DX10CreateAsyncEffectCompilerProcessor**](d3dx10createasynceffectcompilerprocessor.md)     | Cree un efecto con un procesador de datos de forma asincrónica.                                                                                             |
| [**D3DX10CreateAsyncEffectCreateProcessor**](d3dx10createasynceffectcreateprocessor.md)         | Cree un grupo de efectos de forma asincrónica.                                                                                                              |
| [**D3DX10CreateAsyncEffectPoolCreateProcessor**](d3dx10createasynceffectpoolcreateprocessor.md) | Cree un procesador de datos de forma asincrónica.                                                                                                            |
| [**D3DX10CreateAsyncShaderPreprocessProcessor**](d3dx10createasyncshaderpreprocessprocessor.md) | Cree un procesador de datos para un sombreador de forma asincrónica.                                                                                               |



 

API que toman un bombeo de subprocesos como parámetro.



|                                                                                                  |                                                                  |
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**D3DX10CompileFromFile**](d3dx10compilefromfile.md)                                           | Compilar un sombreador desde un archivo.                                    |
| [**D3DX10CompileFromMemory**](d3dx10compilefrommemory.md)                                       | Compilar un sombreador que resida en la memoria.                             |
| [**D3DX10CompileFromResource**](d3dx10compilefromresource.md)                                   | Compilar un sombreador desde un recurso.                                |
| [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md)                                 | Cree un efecto a partir de un archivo.                                    |
| [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md)                             | Cree un efecto a partir de la memoria.                                    |
| [**D3DX10CreateEffectFromResource**](d3dx10createeffectfromresource.md)                         | Cree un efecto a partir de un recurso.                                |
| [**D3DX10CreateEffectPoolFromFile**](d3dx10createeffectpoolfromfile.md)                         | Cree un grupo de efectos a partir de un archivo.                               |
| [**D3DX10CreateEffectPoolFromMemory**](d3dx10createeffectpoolfrommemory.md)                     | Cree un grupo de efectos a partir de un archivo que reside en la memoria.            |
| [**D3DX10CreateEffectPoolFromResource**](d3dx10createeffectpoolfromresource.md)                 | Cree un grupo de efectos a partir de un recurso.                           |
| [**D3DX10PreprocessShaderFromFile**](d3dx10preprocessshaderfromfile.md)                         | Cree un sombreador a partir de un archivo sin compilarlo.                |
| [**D3DX10PreprocessShaderFromMemory**](d3dx10preprocessshaderfrommemory.md)                     | Cree un sombreador a partir de la memoria sin compilarlo.                |
| [**D3DX10PreprocessShaderFromResource**](d3dx10preprocessshaderfromresource.md)                 | Cree un sombreador a partir de un recurso sin compilarlo.            |
| [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md)         | Cree una vista de recursos del sombreador a partir de un archivo.                       |
| [**D3DX10CreateShaderResourceViewFromMemory**](d3dx10createshaderresourceviewfrommemory.md)     | Cree una vista de recursos del sombreador desde un archivo en la memoria.             |
| [**D3DX10CreateShaderResourceViewFromResource**](d3dx10createshaderresourceviewfromresource.md) | Cree una vista de recursos del sombreador desde un recurso.                   |
| [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md)                                 | Recupera información sobre un archivo de imagen determinado.                  |
| [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)                             | Obtiene información acerca de una imagen ya cargada en la memoria.       |
| [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md)                         | Recupera información acerca de una imagen determinada en un recurso.         |
| [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)                               | Cree un recurso de textura a partir de un archivo.                           |
| [**D3DX10CreateTextureFromMemory**](d3dx10createtexturefrommemory.md)                           | Cree un recurso de textura a partir de un archivo que reside en la memoria del sistema. |
| [**D3DX10CreateTextureFromResource**](d3dx10createtexturefromresource.md)                       | Cree un recurso de textura desde otro recurso.                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
