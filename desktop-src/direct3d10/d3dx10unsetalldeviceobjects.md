---
description: Quita todos los recursos del dispositivo estableciendo sus punteros en NULL. Se debe llamar a este método durante el cierre de la aplicación. Ayuda a garantizar que, cuando se liberan todos sus recursos, ninguno de ellos está enlazado al dispositivo.
ms.assetid: f41ce97e-5a81-43a4-a8c7-7411b43c0d61
title: Función D3DX10UnsetAllDeviceObjects (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10UnsetAllDeviceObjects
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 079c5f1b437c2755bf7125dee6be10baed1a91b4a37276997e70543c72904036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128347"
---
# <a name="d3dx10unsetalldeviceobjects-function"></a>Función D3DX10UnsetAllDeviceObjects

Quita todos los recursos del dispositivo estableciendo sus punteros en **NULL.** Se debe llamar a este método durante el cierre de la aplicación. Ayuda a garantizar que, cuando se liberan todos sus recursos, ninguno de ellos está enlazado al dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10UnsetAllDeviceObjects(
  _In_ ID3D10Device *pDevice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Puntero al dispositivo. Vea [**ID3D10Dispositivo interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[De uso general Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




