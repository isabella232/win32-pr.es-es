---
description: Establezca los elementos de trabajo en el dispositivo una vez que terminen de cargarse y procesarse.
ms.assetid: 67a9fcb2-3513-413d-ac3d-9988ef7b5a1f
title: Método ID3DX10ThreadPump::P rocessDeviceWorkItems (D3DX10.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126884689"
---
# <a name="id3dx10threadpumpprocessdeviceworkitems-method"></a>Método ID3DX10ThreadPump::P rocessDeviceWorkItems

Establezca los elementos de trabajo en el dispositivo una vez que terminen de cargarse y procesarse. Cuando el bombeo de subprocesos haya terminado de cargar y procesar un recurso o sombreador, lo mantendrá en una cola hasta que se llame a esta API, momento en el que los elementos procesados se establecerán en el dispositivo. Esto es útil para controlar la cantidad de procesamiento que se dedica a enlazar recursos al dispositivo para cada fotograma. Vea Notas.

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

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de elementos de trabajo que se establecerán en el dispositivo. ProcessDeviceObjectCreation creará como máximo objetos iWorkItemCount. Si no hay suficientes elementos de trabajo en la cola para procesar objetos iWorkItemCount, ProcessDeviceObjectCreation creará tantos objetos de dispositivo como elementos de la cola.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Observaciones

Como ejemplo de cómo se podría usar esta API, diga que está cerca del final de un nivel del juego y que quiere empezar a cargar previamente las texturas, los sombreadores y otros recursos para el siguiente nivel. La bomba de subprocesos comenzará a cargar, descomprimir y procesar los recursos y sombreadores en un subproceso independiente hasta que estén listos para establecerse en el dispositivo, momento en el que los dejará en una cola. Es posible que no desee establecer todos los recursos y sombreadores en el dispositivo a la vez, ya que esto puede provocar una ralentización temporal reconocible en el rendimiento del juego. Por lo tanto, se podría llamar a esta API una vez por fotograma para que solo se establezca un número pequeño de elementos de trabajo en el dispositivo en cada fotograma, lo que propaga la carga de trabajo de los recursos de enlace al dispositivo en varios fotogramas y minimiza la posibilidad de una ralentización reconocible en el rendimiento del juego.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX10ThreadPump](id3dx10threadpump.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
