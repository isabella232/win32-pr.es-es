---
title: Método ID3DX11ThreadPump ProcessDeviceWorkItems (D3DX11core. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Establece los elementos de trabajo en el dispositivo una vez que han finalizado la carga y el procesamiento.
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
ms.openlocfilehash: 5ad570785ac7dc36fb5dd9d464e97ef46f52ca93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986899"
---
# <a name="id3dx11threadpumpprocessdeviceworkitems-method"></a>ID3DX11ThreadPump::P método rocessDeviceWorkItems

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 

Establece los elementos de trabajo en el dispositivo una vez que han finalizado la carga y el procesamiento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iWorkItemCount* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Número de elementos de trabajo que se van a establecer en el dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Cuando el bombeo de subprocesos ha terminado de cargar y procesar un recurso o sombreador, lo mantendrá en una cola hasta que se llame a esta API, momento en que los elementos procesados se establecerán en el dispositivo. Esto resulta útil para controlar la cantidad de procesamiento que se emplea en los recursos de enlace al dispositivo para cada fotograma.

Como ejemplo de cómo se puede usar esta API, supuesto que está llegando al final de un nivel del juego y desea comenzar a cargar previamente las texturas, los sombreadores y otros recursos para el siguiente nivel. El bombeo de subprocesos comenzará a cargar, descomprimir y procesar los recursos y los sombreadores en un subproceso independiente hasta que estén listos para su establecimiento en el dispositivo, momento en el que los dejará en una cola. Es posible que no quiera establecer todos los recursos y sombreadores en el dispositivo de una sola vez, ya que esto puede provocar una disminución temporal apreciable en el rendimiento del juego. Por lo tanto, se puede llamar a esta API una vez por cada fotograma para que solo se establezca un número pequeño de elementos de trabajo en el dispositivo en cada fotograma, con lo que se propagará la carga de trabajo de los recursos de enlace al dispositivo en varios fotogramas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11ThreadPump](id3dx11threadpump.md)
</dt> <dt>

[Interfaces de D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

