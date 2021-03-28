---
title: Método Optimize ID3DX11Effect (D3dx11effect. h)
description: Minimizar la cantidad de memoria necesaria para un efecto.
ms.assetid: fa1d0769-6746-44f6-9979-31a534646884
keywords:
- Optimizar el método Direct3D 11
- Optimizar el método Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método Optimize
topic_type:
- apiref
api_name:
- ID3DX11Effect.Optimize
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33fd6d200f6b22af46e648040e8299f40ec9ebae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998604"
---
# <a name="id3dx11effectoptimize-method"></a>ID3DX11Effect:: Optimize (método)

Minimizar la cantidad de memoria necesaria para un efecto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Optimize();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Un efecto usa el espacio de memoria de dos maneras diferentes: almacenar la información requerida por el motor en tiempo de ejecución para ejecutar un efecto y almacenar los metadatos necesarios para reflejar información de nuevo en una aplicación mediante la API. Puede minimizar la cantidad de memoria requerida por un efecto llamando a **ID3DX11Effect:: Optimize** , que quita los metadatos de reflexión de la memoria. Los métodos de API para leer variables dejarán de funcionar una vez que se hayan quitado los datos de reflexión.

Se producirá un error en los siguientes métodos después de haber llamado a Optimize en un efecto.

-   [**ID3DX11Effect::GetConstantBufferByIndex**](id3dx11effect-getconstantbufferbyindex.md)
-   [**ID3DX11Effect::GetConstantBufferByName**](id3dx11effect-getconstantbufferbyname.md)
-   [**ID3DX11Effect::GetDesc**](id3dx11effect-getdesc.md)
-   [**ID3DX11Effect:: GetDevice**](id3dx11effect-getdevice.md)
-   [**ID3DX11Effect::GetTechniqueByIndex**](id3dx11effect-gettechniquebyindex.md)
-   [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md)
-   [**ID3DX11Effect::GetVariableByIndex**](id3dx11effect-getvariablebyindex.md)
-   [**ID3DX11Effect::GetVariableByName**](id3dx11effect-getvariablebyname.md)
-   [**ID3DX11Effect::GetVariableBySemantic**](id3dx11effect-getvariablebysemantic.md)

> [!Note]  
> Las referencias recuperadas con estos métodos antes de llamar a **ID3DX11Effect:: Optimize** siguen siendo válidas después de llamar a **ID3DX11Effect:: Optimize** . Esto permite a la aplicación obtener todas las variables, técnicas y pases que usará, llamar a Optimize y, a continuación, usar el efecto.

 

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

 

 





