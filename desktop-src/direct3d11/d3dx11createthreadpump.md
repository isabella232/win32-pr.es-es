---
title: Función D3DX11CreateThreadPump (D3DX11core.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Vea la sección Comentarios. Cree una bomba de subprocesos.
ms.assetid: 8983a2e2-185f-43c0-baf0-a4c883d91220
keywords:
- Función D3DX11CreateThreadPump Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5551cd22a4c134570c2059cc6aeaa9538311b19
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060855"
---
# <a name="d3dx11createthreadpump-function"></a>Función D3DX11CreateThreadPump

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Vea la sección Comentarios.

 

Cree una bomba de subprocesos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX11ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cIoThreads* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Número de subprocesos de E/S que se crearán. Si se especifica 0, Direct3D intentará calcular el número óptimo de subprocesos en función de la configuración de hardware.

</dd> <dt>

*cProcThreads* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Número de subprocesos de proceso que se crearán. Si se especifica 0, Direct3D intentará calcular el número óptimo de subprocesos en función de la configuración de hardware.

</dd> <dt>

*ppThreadPump* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***

El bombeo de subprocesos creado. Vea [**ID3DX11ThreadPump (interfaz).**](id3dx11threadpump.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno [de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Observaciones

Un bombeo de subprocesos es un objeto que consume muchos recursos. Solo se debe crear un bombeo de subprocesos por aplicación.

No hay ninguna implementación del cargador asincrónico fuera de D3DX 10 y D3DX 11.

Para Windows Store, los ejemplos de DirectX (por ejemplo, el [ejemplo de tutorial de Direct3D)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)incluyen el módulo **BasicLoader** que usa el modelo de programación asincrónica de Windows Runtime [**(AsyncBase).**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))

En el caso de las aplicaciones de escritorio Win32, puede usar el Runtime de simultaneidad [para](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) implementar algo similar al modelo de programación asincrónica de Windows Runtime.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

