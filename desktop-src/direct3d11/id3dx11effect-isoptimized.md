---
title: Método ID3DX11Effect IsOptimized (D3dx11effect.h)
description: Pruebe un efecto para ver si los metadatos de reflexión se han quitado de la memoria.
ms.assetid: fb0a876b-7419-45b7-97fe-8352dd97d8c5
keywords:
- Método IsOptimized Direct3D 11
- Método IsOptimized Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método IsOptimized
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsOptimized
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd04bf43869f23bfec38db34be1b83b2c4f3953c7017120ebe2f0c985504b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124510"
---
# <a name="id3dx11effectisoptimized-method"></a>Método ID3DX11Effect::IsOptimized

Pruebe un efecto para ver si los metadatos de reflexión se han quitado de la memoria.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsOptimized();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

**TRUE** si el efecto está optimizado; en caso **contrario, FALSE**.

## <a name="remarks"></a>Comentarios

Un efecto usa el espacio de memoria de dos maneras diferentes: para almacenar la información requerida por el tiempo de ejecución para ejecutar un efecto y para almacenar los metadatos necesarios para reflejar la información en una aplicación mediante la API. Puede minimizar la cantidad de memoria necesaria para un efecto llamando a [**ID3DX11Effect::Optimize,**](id3dx11effect-optimize.md) que quita los metadatos de reflexión de la memoria. Por supuesto, los métodos de API para leer variables ya no funcionarán una vez que se hayan quitado los datos de reflexión.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

