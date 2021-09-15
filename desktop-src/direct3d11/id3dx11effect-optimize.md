---
title: Método ID3DX11Effect Optimize (D3dx11effect.h)
description: Minimice la cantidad de memoria necesaria para un efecto.
ms.assetid: fa1d0769-6746-44f6-9979-31a534646884
keywords:
- Optimización del método Direct3D 11
- Optimización del método Direct3D 11, interfaz ID3DX11Effect
- ID3DX11Effect interface Direct3D 11 , Optimize (método)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465394"
---
# <a name="id3dx11effectoptimize-method"></a>Método ID3DX11Effect::Optimize

Minimice la cantidad de memoria necesaria para un efecto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Optimize();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Observaciones

Un efecto usa el espacio de memoria de dos maneras diferentes: para almacenar la información requerida por el tiempo de ejecución para ejecutar un efecto y para almacenar los metadatos necesarios para reflejar la información en una aplicación mediante la API. Puede minimizar la cantidad de memoria necesaria para un efecto llamando a **ID3DX11Effect::Optimize,** que quita los metadatos de reflexión de la memoria. Los métodos de API para leer variables ya no funcionarán una vez que se hayan quitado los datos de reflexión.

Se producirá un error en los métodos siguientes después de llamar a Optimize en un efecto.

-   [**ID3DX11Effect::GetConstantBufferByIndex**](id3dx11effect-getconstantbufferbyindex.md)
-   [**ID3DX11Effect::GetConstantBufferByName**](id3dx11effect-getconstantbufferbyname.md)
-   [**ID3DX11Effect::GetDesc**](id3dx11effect-getdesc.md)
-   [**ID3DX11Effect::GetDevice**](id3dx11effect-getdevice.md)
-   [**ID3DX11Effect::GetTechniqueByIndex**](id3dx11effect-gettechniquebyindex.md)
-   [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md)
-   [**ID3DX11Effect::GetVariableByIndex**](id3dx11effect-getvariablebyindex.md)
-   [**ID3DX11Effect::GetVariableByName**](id3dx11effect-getvariablebyname.md)
-   [**ID3DX11Effect::GetVariableBySemantic**](id3dx11effect-getvariablebysemantic.md)

> [!Note]  
> Las referencias recuperadas con estos métodos antes de llamar a **ID3DX11Effect::Optimize** siguen siendo válidas después de llamar a **ID3DX11Effect::Optimize.** Esto permite a la aplicación obtener todas las variables, técnicas y pases que usará, llamar a Optimize y, a continuación, usar el efecto.

 

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

 

 





