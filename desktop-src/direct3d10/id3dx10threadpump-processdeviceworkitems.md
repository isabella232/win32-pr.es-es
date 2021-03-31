---
description: Establezca los elementos de trabajo en el dispositivo una vez que hayan finalizado la carga y el procesamiento.
ms.assetid: 67a9fcb2-3513-413d-ac3d-9988ef7b5a1f
title: ID3DX10ThreadPump::P método rocessDeviceWorkItems (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.ProcessDeviceWorkItems
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 88b98d68e4e0e47b2c8e7f9a2e095565c53e2561
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157261"
---
# <a name="id3dx10threadpumpprocessdeviceworkitems-method"></a>ID3DX10ThreadPump::P método rocessDeviceWorkItems

Establezca los elementos de trabajo en el dispositivo una vez que hayan finalizado la carga y el procesamiento. Cuando el bombeo de subprocesos ha terminado de cargar y procesar un recurso o sombreador, lo mantendrá en una cola hasta que se llame a esta API, momento en que los elementos procesados se establecerán en el dispositivo. Esto resulta útil para controlar la cantidad de procesamiento que se emplea en los recursos de enlace al dispositivo para cada fotograma. Vea Notas.

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

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de elementos de trabajo que se van a establecer en el dispositivo. ProcessDeviceObjectCreation creará como máximo objetos iWorkItemCount. Si no hay suficientes elementos de trabajo en la cola para procesar los objetos iWorkItemCount, ProcessDeviceObjectCreation creará tantos objetos de dispositivo como elementos haya en la cola.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Como ejemplo de cómo se puede usar esta API, supuesto que está llegando al final de un nivel del juego y desea comenzar a cargar previamente las texturas, los sombreadores y otros recursos para el siguiente nivel. El bombeo de subprocesos comenzará a cargar, descomprimir y procesar los recursos y los sombreadores en un subproceso independiente hasta que estén listos para su establecimiento en el dispositivo, momento en el que los dejará en una cola. Es posible que no quiera establecer todos los recursos y sombreadores en el dispositivo de una sola vez, ya que esto puede provocar que una temporal advertible se ralentice en el rendimiento del juego. Por lo tanto, se puede llamar a esta API una vez por fotograma para que solo se establezca un número pequeño de elementos de trabajo en el dispositivo en cada fotograma, con lo que se propagará la carga de trabajo de los recursos de enlace al dispositivo a través de varios fotogramas y se minimizará la posibilidad de que una observable se ralentice en el rendimiento del juego.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10ThreadPump](id3dx10threadpump.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
