---
description: Se usa para ejecutar tareas de forma asincrónica y se crea con D3DX10CreateThreadPump.
ms.assetid: 8d03c94a-9b64-464c-b0f4-4e5f5a00503f
title: Interfaz ID3DX10ThreadPump (D3DX10.h)
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
ms.openlocfilehash: ef95e4087d2d50e00bf7637119038f35378b8ef1657c23ac8b7a11e62acad3a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046873"
---
# <a name="id3dx10threadpump-interface"></a>Interfaz ID3DX10ThreadPump

Se usa para ejecutar tareas de forma asincrónica y se crea con [**D3DX10CreateThreadPump**](d3dx10createthreadpump.md). Hay varias API D3DX10 que, opcionalmente, pueden tomar una bomba de subprocesos como parámetro, como [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) y [**D3DX10CompileFromFile**](d3dx10compilefromfile.md) (vea los comentarios para obtener una lista completa). Si el bombeo de subprocesos se pasa a estas API, se ejecutará de forma asincrónica en un subproceso de bombeo de subprocesos independiente. La ventaja de hacerlo es que puede hacer que la carga y el procesamiento de grandes cantidades de datos se realicen sin ver una ralentización observable en el rendimiento en pantalla.

## <a name="members"></a>Miembros

La **interfaz ID3DX10ThreadPump** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10ThreadPump** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX10ThreadPump** tiene estos métodos.



| Método                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddWorkItem**](id3dx10threadpump-addworkitem.md)                       | Agregue un elemento de trabajo al bombeo de subprocesos.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**GetQueueStatus**](id3dx10threadpump-getqueuestatus.md)                 | Obtiene el número de elementos de cada una de las tres colas dentro de la bomba de subprocesos.<br/>                                                                                                                                                                                                                                                                                                                                           |
| [**GetWorkItemCount**](id3dx10threadpump-getworkitemcount.md)             | Obtiene el número de elementos de trabajo que hay actualmente en la bomba de subprocesos.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| [**ProcessDeviceWorkItems**](id3dx10threadpump-processdeviceworkitems.md) | Establezca los elementos de trabajo en el dispositivo una vez que terminen de cargarse y procesarse. Cuando el bombeo de subprocesos haya terminado de cargar y procesar un recurso o sombreador, lo mantendrá en una cola hasta que se llame a esta API, momento en el que los elementos procesados se establecerán en el dispositivo. Esto es útil para controlar la cantidad de procesamiento que se dedica a enlazar recursos al dispositivo para cada fotograma. Vea Notas.<br/> |
| [**PurgeAllItems**](id3dx10threadpump-purgeallitems.md)                   | Borre todos los elementos de trabajo del bombeo de subprocesos.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**WaitForAllItems**](id3dx10threadpump-waitforallitems.md)               | Espere a que finalicen todos los elementos de trabajo del bombeo de subprocesos.<br/>                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Comentarios

El bombeo de subprocesos carga y procesa los datos en un proceso de 3 pasos. Va a:

1.  Cargue y descomprima los datos con un cargador de datos. El objeto del cargador de datos tiene tres métodos a los que llamará internamente el bombeo de subprocesos mientras carga y descomprime los datos: [**ID3DX10DataLoader::Load**](id3dx10dataloader-load.md), [**ID3DX10DataLoader::D ecompress**](id3dx10dataloader-decompress.md)e [**ID3DX10DataLoader::D estroy**](id3dx10dataloader-destroy.md). La funcionalidad específica de estas tres API difiere en función del tipo de datos que se cargan y descomprimen. La interfaz del cargador de datos también se puede heredar y sus API se pueden cambiar si se carga un archivo de datos definido en su propio formato personalizado.
2.  Procesar los datos con un procesador de datos. El objeto de procesador de datos tiene tres métodos a los que llamará internamente el bombeo de subprocesos mientras procesa los datos: [**ID3DX10DataProcessor::P rocess,**](id3dx10dataprocessor-process.md) [**ID3DX10DataProcessor::CreateDeviceObject**](id3dx10dataprocessor-createdeviceobject.md)y [**ID3DX10DataProcessor::D estroy**](id3dx10dataprocessor-destroy.md). La forma en que procesa los datos será diferente en función del tipo de datos. Por ejemplo, si los datos son una textura almacenada como JPEG, **ID3DX10DataProcessor::P rocess** realizará la descompresión jpeg para obtener los bits de imagen sin procesar de la imagen. Si los datos son un sombreador, **ID3DX10DataProcessor::P compile** el HLSL en el código de bytes. Una vez procesados los datos, se creará un objeto de dispositivo para los datos (con **ID3DX10DataProcessor::CreateDeviceObject)** y el objeto se agregará a una cola de objetos de dispositivo. La interfaz del procesador de datos también se puede heredar y sus API se pueden cambiar si se está procesando un archivo de datos definido en su propio formato personalizado.
3.  Enlace el objeto de dispositivo al dispositivo. Esto se hace cuando una aplicación llama a [**ID3DX10ThreadPump::P rocessDeviceWorkItems**](id3dx10threadpump-processdeviceworkitems.md), que enlazará un número especificado de objetos de la cola de objetos de dispositivo al dispositivo.

El bombeo de subprocesos se puede usar para cargar datos de una de estas dos maneras: llamando a una API que toma un bombeo de subprocesos como parámetro, como [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) y [**D3DX10CompileFromFile,**](d3dx10compilefromfile.md)o llamando a [**ID3DX10ThreadPump::AddWorkItem**](id3dx10threadpump-addworkitem.md). En el caso de las API que toman una bomba de subprocesos, el cargador de datos y el procesador de datos se crean internamente. En el caso de **AddWorkItem,** el cargador de datos y el procesador de datos deben crearse con antelación y, a continuación, pasarse a AddWorkItem. D3DX10 proporciona un conjunto de API para crear cargadores de datos y procesadores de datos que tienen funcionalidad para cargar y procesar formatos de datos comunes (consulte comentarios para obtener una lista completa de las API). En el caso de los formatos de datos personalizados, se deben heredar las interfaces del cargador de datos y del procesador de datos y se deben volver a definir sus métodos.

El objeto de bombeo de subprocesos ocupa una cantidad considerable de recursos, por lo que, por lo general, solo se debe crear uno por aplicación.

Cargadores de datos D3DX10 integrados



|                                                                           |  Descripción                                        |
|----------------------------------------------------------------------------|------------------------------------------|
| [**D3DX10CreateAsyncFileLoader**](d3dx10createasyncfileloader.md)         | Cree un cargador de archivos de forma asincrónica.     |
| [**D3DX10CreateAsyncMemoryLoader**](d3dx10createasyncmemoryloader.md)     | Cree un cargador de datos de forma asincrónica.     |
| [**D3DX10CreateAsyncResourceLoader**](d3dx10createasyncresourceloader.md) | Cree un cargador de recursos de forma asincrónica. |



 

Procesadores de datos D3DX10 integrados



|                                                                                                 |  Descripción                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md)                   | Cree un procesador de datos que se usará con una bomba de subprocesos. Esta API es similar a D3DX10CreateAsyncTextureInfoProcessor, pero también carga la textura. |
| [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md)           | Cree un procesador de datos que se usará con una bomba de subprocesos.                                                                                             |
| [**D3DX10CreateAsyncShaderCompilerProcessor**](d3dx10createasyncshadercompilerprocessor.md)     | Compile un sombreador y cree un procesador de datos de forma asincrónica.                                                                                       |
| [**D3DX10CreateAsyncEffectCompilerProcessor**](d3dx10createasynceffectcompilerprocessor.md)     | Cree un efecto con un procesador de datos de forma asincrónica.                                                                                             |
| [**D3DX10CreateAsyncEffectCreateProcessor**](d3dx10createasynceffectcreateprocessor.md)         | Cree un grupo de efectos de forma asincrónica.                                                                                                              |
| [**D3DX10CreateAsyncEffectPoolCreateProcessor**](d3dx10createasynceffectpoolcreateprocessor.md) | Cree un procesador de datos de forma asincrónica.                                                                                                            |
| [**D3DX10CreateAsyncShaderPreprocessProcessor**](d3dx10createasyncshaderpreprocessprocessor.md) | Cree un procesador de datos para un sombreador de forma asincrónica.                                                                                               |



 

API que toman un bombeo de subprocesos como parámetro.



|                                                                                                 | Descripción                                                                 |
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**D3DX10CompileFromFile**](d3dx10compilefromfile.md)                                           | Compile un sombreador a partir de un archivo.                                    |
| [**D3DX10CompileFromMemory**](d3dx10compilefrommemory.md)                                       | Compile un sombreador que resida en la memoria.                             |
| [**D3DX10CompileFromResource**](d3dx10compilefromresource.md)                                   | Compile un sombreador a partir de un recurso.                                |
| [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md)                                 | Cree un efecto a partir de un archivo.                                    |
| [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md)                             | Cree un efecto a partir de la memoria.                                    |
| [**D3DX10CreateEffectFromResource**](d3dx10createeffectfromresource.md)                         | Cree un efecto a partir de un recurso.                                |
| [**D3DX10CreateEffectPoolFromFile**](d3dx10createeffectpoolfromfile.md)                         | Cree un grupo de efectos a partir de un archivo.                               |
| [**D3DX10CreateEffectPoolFromMemory**](d3dx10createeffectpoolfrommemory.md)                     | Cree un grupo de efectos a partir de un archivo que resida en memoria.            |
| [**D3DX10CreateEffectPoolFromResource**](d3dx10createeffectpoolfromresource.md)                 | Cree un grupo de efectos a partir de un recurso.                           |
| [**D3DX10PreprocessShaderFromFile**](d3dx10preprocessshaderfromfile.md)                         | Cree un sombreador a partir de un archivo sin compilarlo.                |
| [**D3DX10PreprocessShaderFromMemory**](d3dx10preprocessshaderfrommemory.md)                     | Cree un sombreador a partir de la memoria sin compilarlo.                |
| [**D3DX10PreprocessShaderFromResource**](d3dx10preprocessshaderfromresource.md)                 | Cree un sombreador a partir de un recurso sin compilarlo.            |
| [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md)         | Cree una vista de sombreador y recurso a partir de un archivo.                       |
| [**D3DX10CreateShaderResourceViewFromMemory**](d3dx10createshaderresourceviewfrommemory.md)     | Cree una vista de sombreador y recurso a partir de un archivo en memoria.             |
| [**D3DX10CreateShaderResourceViewFromResource**](d3dx10createshaderresourceviewfromresource.md) | Cree una vista shader-resource a partir de un recurso.                   |
| [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md)                                 | Recupera información sobre un archivo de imagen determinado.                  |
| [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)                             | Obtenga información sobre una imagen ya cargada en la memoria.       |
| [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md)                         | Recupera información sobre una imagen determinada en un recurso.         |
| [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)                               | Cree un recurso de textura a partir de un archivo.                           |
| [**D3DX10CreateTextureFromMemory**](d3dx10createtexturefrommemory.md)                           | Cree un recurso de textura a partir de un archivo que resida en la memoria del sistema. |
| [**D3DX10CreateTextureFromResource**](d3dx10createtexturefromresource.md)                       | Cree un recurso de textura a partir de otro recurso.                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
