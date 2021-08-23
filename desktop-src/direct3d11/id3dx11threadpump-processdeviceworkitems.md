---
title: Método ID3DX11ThreadPump ProcessDeviceWorkItems (D3DX11core.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para las aplicaciones de Windows Store. Establece los elementos de trabajo en el dispositivo una vez que han terminado de cargarse y procesarse.
ms.assetid: 154e6ea5-0a88-4c8a-9c20-e7fbf95f1946
keywords:
- Método ProcessDeviceWorkItems Direct3D 11
- Método ProcessDeviceWorkItems Direct3D 11, interfaz ID3DX11ThreadPump
- Interfaz ID3DX11ThreadPump Direct3D 11, método ProcessDeviceWorkItems
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.ProcessDeviceWorkItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a6918e9ecea9d66c3ebca034628387ea471e9173b4b14f24e9b7f866897325
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608675"
---
# <a name="id3dx11threadpumpprocessdeviceworkitems-method"></a>Método ID3DX11ThreadPump::P rocessDeviceWorkItems

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

Establece los elementos de trabajo en el dispositivo una vez que han terminado de cargarse y procesarse.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iWorkItemCount* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Número de elementos de trabajo que se establecerán en el dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno [de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Cuando el bombeo de subprocesos haya terminado de cargar y procesar un recurso o sombreador, lo mantendrá en una cola hasta que se llame a esta API, momento en el que los elementos procesados se establecerán en el dispositivo. Esto es útil para controlar la cantidad de procesamiento que se dedica a enlazar recursos al dispositivo para cada fotograma.

Como ejemplo de cómo se podría usar esta API, diga que está cerca del final de un nivel del juego y que quiere empezar a cargar previamente las texturas, los sombreadores y otros recursos para el siguiente nivel. La bomba de subprocesos comenzará a cargar, descomprimir y procesar los recursos y sombreadores en un subproceso independiente hasta que estén listos para establecerse en el dispositivo, momento en el que los dejará en una cola. Es posible que no desee establecer todos los recursos y sombreadores en el dispositivo a la vez, ya que esto puede provocar una notable ralentización temporal en el rendimiento del juego. Por lo tanto, se podría llamar a esta API una vez por fotograma para que solo se establezca un número pequeño de elementos de trabajo en el dispositivo en cada fotograma, con lo que se propagará la carga de trabajo de los recursos de enlace al dispositivo en varios fotogramas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11ThreadPump](id3dx11threadpump.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

