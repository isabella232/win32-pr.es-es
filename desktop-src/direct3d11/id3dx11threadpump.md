---
title: Interfaz ID3DX11ThreadPump (D3DX11core. h)
description: Un bombeo de subprocesos ejecuta las tareas de forma asincrónica.
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
ms.openlocfilehash: b60cedaa4ef84cb9f3ea31cd619d7335cc09324e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149988"
---
# <a name="id3dx11threadpump-interface"></a>Interfaz ID3DX11ThreadPump

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 

Un bombeo de subprocesos ejecuta las tareas de forma asincrónica. Se crea llamando a [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md). Hay varias API que toman un bombeo de subprocesos opcional como parámetro, como [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) y [**D3DX11CompileFromFile**](d3dx11compilefromfile.md). Si pasa una interfaz de bombeo de subprocesos a estas API, las funciones se ejecutarán de forma asincrónica en un subproceso independiente. Especialmente en equipos con varios procesadores, un bombeo de subprocesos puede cargar recursos y procesar datos sin una disminución apreciable en el rendimiento.

## <a name="members"></a>Miembros

La interfaz **ID3DX11ThreadPump** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ID3DX11ThreadPump** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DX11ThreadPump** tiene estos métodos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Método</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11threadpump-addworkitem.md"><strong>AddWorkItem</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/> Agrega un elemento de trabajo al bombeo de subprocesos.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/> Obtiene el número de elementos de cada una de las tres colas dentro del bombeo de subprocesos.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/> Obtiene el número de elementos de trabajo en el bombeo de subprocesos.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>ProcessDeviceWorkItems</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/> Establece los elementos de trabajo en el dispositivo una vez que han finalizado la carga y el procesamiento.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11threadpump-purgeallitems.md"><strong>PurgeAllItems</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/> Borra todos los elementos de trabajo del bombeo de subprocesos.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/> Espera a que finalicen todos los elementos de trabajo en el bombeo de subprocesos.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

### <a name="using-a-thread-pump"></a>Usar un bombeo de subprocesos

El bombeo de subprocesos carga y procesa los datos mediante el siguiente proceso de tres pasos:

1.  Cargar y descomprimir los datos con un [**cargador de datos**](id3dx11dataloader.md). El objeto del cargador de datos tiene tres métodos a los que el bombeo de subprocesos llamará internamente a medida que se cargan y descomprimen los datos: [**ID3DX11DataLoader:: Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader::D ecompress**](id3dx11dataloader-decompress.md)y [**ID3DX11DataLoader::D estroy**](id3dx11dataloader-destroy.md). La funcionalidad específica de estas tres API varía en función del tipo de datos que se cargan y descomprimen. También se puede heredar la interfaz del cargador de datos y se pueden cambiar sus API si se está cargando un archivo de datos definido en un formato personalizado propio.
2.  Procese los datos con un [**procesador de datos**](id3dx11dataprocessor.md). El objeto de procesador de datos tiene tres métodos a los que el bombeo de subprocesos llamará internamente a medida que procesa los datos: [**ID3DX11DataProcessor::P rador**](id3dx11dataprocessor-process.md), [**ID3DX11DataProcessor:: CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)y [**ID3DX11DataProcessor::D estroy**](id3dx11dataprocessor-destroy.md). La forma en que se procesan los datos será diferente en función del tipo de datos. Por ejemplo, si los datos son una textura almacenada como JPEG, [**ID3DX11DataProcessor::P rador**](id3dx11dataprocessor-process.md) realizará la descompresión JPEG para obtener los bits de imagen sin formato de la imagen. Si los datos son un sombreador, [**ID3DX11DataProcessor::P rador**](id3dx11dataprocessor-process.md) compilará el HLSL en código de bytes. Una vez procesados los datos, se creará un objeto de dispositivo para esos datos (con [**ID3DX11DataProcessor:: CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)) y el objeto se agregará a una cola de objetos de dispositivo. También se puede heredar la interfaz del procesador de datos y se pueden cambiar sus API si se está procesando un archivo de datos definido en un formato personalizado propio.
3.  Enlazar el objeto de dispositivo al dispositivo. Esto se hace cuando una aplicación de una de las llamadas a [**ID3DX11ThreadPump::P rocessdeviceworkitems**](id3dx11threadpump-processdeviceworkitems.md), que enlazará un número especificado de objetos en la cola de objetos de dispositivo al dispositivo.

El bombeo de subprocesos se puede utilizar para cargar datos de una de las dos maneras siguientes: llamando a una API que toma un bombeo de subprocesos como parámetro, como [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) y [**D3DX11CompileFromFile**](d3dx11compilefromfile.md), o llamando a [**ID3DX11ThreadPump:: AddWorkItem**](id3dx11threadpump-addworkitem.md). En el caso de las API que toman un bombeo de subprocesos, el cargador de datos y el procesador de datos se crean internamente. En el caso de AddWorkItem, el cargador de datos y el procesador de datos se deben crear de antemano y, a continuación, pasarse a AddWorkItem. D3DX11 proporciona un conjunto de API para crear cargadores de datos y procesadores de datos que tienen funcionalidad para cargar y procesar formatos de datos comunes. En el caso de los formatos de datos personalizados, las interfaces del cargador de datos y del procesador de datos deben heredarse y sus métodos deben redefinirse.

El objeto de bombeo de subprocesos ocupa una cantidad considerable de recursos, por lo que generalmente solo se debe crear uno por aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>D3DX11core. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

