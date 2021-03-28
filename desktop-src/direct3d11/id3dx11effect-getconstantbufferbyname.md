---
title: Método ID3DX11Effect GetConstantBufferByName (D3dx11effect. h)
description: Obtiene un búfer de constantes por nombre.
ms.assetid: 11757615-4068-430d-9ab0-f83f02af8e55
keywords:
- Método GetConstantBufferByName Direct3D 11
- Método GetConstantBufferByName Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método GetConstantBufferByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa01d20bfeebfa3f689a58aae5c5face8b879e3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914790"
---
# <a name="id3dx11effectgetconstantbufferbyname-method"></a>ID3DX11Effect:: GetConstantBufferByName (método)

Obtiene un búfer de constantes por nombre.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nombre del búfer de constantes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

Puntero al búfer de constantes indicado por el nombre. Vea [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).

## <a name="remarks"></a>Observaciones

Un efecto que contiene una variable que una aplicación va a leer o escribir requiere al menos un búfer de constantes. Para obtener el mejor rendimiento, un efecto debe organizar las variables en uno o varios búferes de constantes según su frecuencia de actualización.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects. Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

