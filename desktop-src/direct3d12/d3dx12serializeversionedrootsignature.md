---
title: Función D3DX12SerializeVersionedRootSignature (D3dx12.h)
description: Ayuda a habilitar las características de firma raíz 1.1 cuando están disponibles y no requiere mantener dos rutas de acceso de código para crear firmas raíz. Este método auxiliar reconstruye una firma raíz de la versión 1.0 cuando no se admite la versión 1.1.
ms.assetid: 0F6BA6C1-9A33-4E99-BF34-4A0358E7427D
keywords:
- Función D3DX12SerializeVersionedRootSignature
topic_type:
- apiref
api_name:
- D3DX12SerializeVersionedRootSignature
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70a9d0424f7f7a7f89edde18273c5d1fa22fae28
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359813"
---
# <a name="d3dx12serializeversionedrootsignature-function"></a>Función D3DX12SerializeVersionedRootSignature

Ayuda a habilitar las características de firma raíz 1.1 cuando están disponibles y no requiere mantener dos rutas de acceso de código para crear firmas raíz. Este método auxiliar reconstruye una firma raíz de la versión 1.0 cuando no se admite la versión 1.1.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT inline D3DX12SerializeVersionedRootSignature(
  _In_      const D3D12_VERSIONED_ROOT_SIGNATURE_DESC *pRootSignatureDesc,
                  D3D_ROOT_SIGNATURE_VERSION          MaxVersion,
  _Out_           ID3DBlob                            **ppBlob,
  _Out_opt_       ID3DBlob                            **ppErrorBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pRootSignatureDesc* \[ En\]
</dt> <dd>

Tipo: **const D3D12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC \***

Especifica un [**\_ \_ \_ \_ DESC D3D12 VERSIONED ROOT SIGNATURE que**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) contiene una descripción de cualquier versión de una firma raíz.

</dd> <dt>

*Maxversion* 
</dt> <dd>

Tipo: **D3D \_ ROOT SIGNATURE \_ \_ VERSION**

Especifica el número máximo admitido de [**D3D \_ ROOT \_ SIGNATURE \_ VERSION.**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)

</dd> <dt>

*ppBlob* \[ out\]
</dt> <dd>

Tipo: **\* \* ID3DBlob**

Puntero a un bloque de memoria que recibe un puntero a la interfaz [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que puede usar para tener acceso a la firma raíz serializada.

</dd> <dt>

*ppErrorBlob* \[ out, opcional\]
</dt> <dd>

Tipo: **\* \* ID3DBlob**

Puntero a un bloque de memoria que recibe un puntero a la interfaz [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que puede usar para tener acceso a los mensajes de error del serializador, o **NULL** si no hay errores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve **S \_ OK si** se realiza correctamente; de lo contrario, devuelve uno de los códigos de retorno de [Direct3D 12](d3d12-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Esta función se publicó para coincidir con la actualización Windows 10 aniversario (14393). Para admitir versiones Windows 10 anteriores a esta, el uso de esta función requiere que se configure d3d12.lib para la *carga retrasada.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature)
</dt> <dt>

[Funciones auxiliares de D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

