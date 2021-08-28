---
title: Método ID3DX11ThreadPump GetQueueStatus (D3DX11core.h)
description: 'Nota: La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Obtiene el número de elementos de cada una de las tres colas dentro de la bomba de subprocesos.'
ms.assetid: 69e1c786-6c7d-4432-bf34-3bf7606a07f6
keywords:
- Método GetQueueStatus Direct3D 11
- Método GetQueueStatus Direct3D 11, interfaz ID3DX11ThreadPump
- Interfaz ID3DX11ThreadPump Direct3D 11, método GetQueueStatus
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.GetQueueStatus
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41535dba7c5abb96c132714ecbc6ee4e02f1f42fcb6a45ebe8795286d8613c66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851505"
---
# <a name="id3dx11threadpumpgetqueuestatus-method"></a>Método ID3DX11ThreadPump::GetQueueStatus

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

Obtiene el número de elementos de cada una de las tres colas dentro de la bomba de subprocesos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pIoQueue* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)\***

Número de elementos de la cola de E/S.

</dd> <dt>

*pProcessQueue* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)\***

Número de elementos de la cola de procesos.

</dd> <dt>

*pDeviceQueue* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)\***

Número de elementos de la cola del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno [de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

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

 

