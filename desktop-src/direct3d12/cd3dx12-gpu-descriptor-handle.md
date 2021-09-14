---
title: CD3DX12_GPU_DESCRIPTOR_HANDLE estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE.
ms.assetid: 6E405AD6-D370-4B87-849A-C52D64C79BF7
keywords:
- CD3DX12_GPU_DESCRIPTOR_HANDLE estructura
topic_type:
- apiref
api_name:
- CD3DX12_GPU_DESCRIPTOR_HANDLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429d41d401b7d3e928bc4ab76850b36ae41b1e8a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060800"
---
# <a name="cd3dx12_gpu_descriptor_handle-structure"></a>Estructura DEL IDENTIFICADOR DEL DESCRIPTOR de GPU CD3DX12 \_ \_ \_

Estructura auxiliar para permitir la inicialización sencilla de una [**estructura D3D12 \_ GPU DESCRIPTOR \_ \_ HANDLE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_GPU_DESCRIPTOR_HANDLE  : public D3D12_GPU_DESCRIPTOR_HANDLE{
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE();
                                  explicit CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &o);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(CD3DX12_DEFAULT);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &other, INT offsetScaledByIncrementSize);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_GPU_DESCRIPTOR_HANDLE&  Offset(INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_GPU_DESCRIPTOR_HANDLE&  Offset(INT offsetScaledByIncrementSize);
  bool                            inline operator==( _In_ const D3D12_GPU_DESCRIPTOR_HANDLE& other) const;
  bool                            inline operator!=( _In_ const D3D12_GPU_DESCRIPTOR_HANDLE& other) const;
  CD3DX12_GPU_DESCRIPTOR_HANDLE & operator=(const D3D12_GPU_DESCRIPTOR_HANDLE &other);
  void                            inline InitOffsetted(_In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            inline InitOffsetted(_In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_GPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_GPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
};
```



## <a name="members"></a>Members

<dl> <dt>

**IDENTIFICADOR DEL \_ DESCRIPTOR DE GPU CD3DX12() \_ \_**
</dt> <dd>

Crea una nueva instancia sin inicializar de un IDENTIFICADOR DE DESCRIPTOR de GPU CD3DX12. \_ \_ \_

</dd> <dt>

**identificador explícito del \_ DESCRIPTOR de GPU CD3DX12(const \_ \_ D3D12 \_ IDENTIFICADOR DEL DESCRIPTOR de GPU &\_ \_ o)**
</dt> <dd>

Crea una nueva instancia de un IDENTIFICADOR DE DESCRIPTOR de GPU CD3DX12, inicializado con el contenido de otra estructura DE IDENTIFICADOR \_ \_ DE DESCRIPTOR de \_ [**\_ \_ GPU \_ D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)

</dd> <dt>

**IDENTIFICADOR DEL DESCRIPTOR DE GPU CD3DX12 \_ \_ \_ (CD3DX12 \_ PREDETERMINADO)**
</dt> <dd>

Crea una nueva instancia de un IDENTIFICADOR DE DESCRIPTOR de GPU CD3DX12, inicializado con parámetros predeterminados \_ \_ \_ (establece el puntero en cero).

</dd> <dt>

**IDENTIFICADOR DEL DESCRIPTOR de GPU CD3DX12(const \_ \_ \_ D3D12 \_ GPU DESCRIPTOR HANDLE &\_ \_ otros, INT offsetScaledByIncrementSize)**
</dt> <dd>

Crea una nueva instancia de un IDENTIFICADOR \_ DE DESCRIPTOR de GPU CD3DX12, \_ \_ inicializando los parámetros siguientes:

Identificador del DESCRIPTOR de GPU D3D12 \_ \_ &\_ otro

INT offsetScaledByIncrementSize: número de incrementos por los que se va a desplazar.

</dd> <dt>

**CD3DX12 \_ \_ GPU DESCRIPTOR \_ HANDLE(const D3D12 \_ GPU DESCRIPTOR HANDLE &\_ \_ other, INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Crea una nueva instancia de un IDENTIFICADOR \_ DE DESCRIPTOR de GPU CD3DX12, \_ \_ inicializando los parámetros siguientes:

Identificador del DESCRIPTOR de GPU D3D12 \_ \_ &\_ otro

INT offsetInDescriptors: número de descriptores por los que se va a incrementar.

Descriptor de UINTIncrementSize: cantidad por la que se va a incrementar para cada descriptor, incluido el relleno.

</dd> <dt>

**Offset(INT offsetInDescriptors, descriptor UINTIncrementSize)**
</dt> <dd>

Establece el desplazamiento según el número especificado de descriptores y la cantidad que se va a incrementar para cada descriptor. Usa los parámetros siguientes:

INT offsetInDescriptors: número de descriptores por los que se va a incrementar.

Descriptor de UINTIncrementSize: cantidad por la que se va a incrementar para cada descriptor, incluido el relleno.

</dd> <dt>

**Offset(INT offsetScaledByIncrementSize)**
</dt> <dd>

Establece el desplazamiento en función del número de incrementos especificado. Usa los parámetros siguientes:

INT offsetScaledByIncrementSize: número de incrementos por los que se va a desplazar.

</dd> <dt>

**inline operator==( \_ In \_ const D3D12 \_ GPU DESCRIPTOR HANDLE& \_ \_ other) const**
</dt> <dd>

Comprueba la igualdad entre el identificador del DESCRIPTOR de GPU CD3DX12 actual y el identificador del DESCRIPTOR de GPU D3D12 o el identificador del \_ \_ DESCRIPTOR de GPU \_ \_ \_ \_ CD3DX12 \_ \_ \_ especificado.

</dd> <dt>

**inline operator!=( \_ In \_ const D3D12 \_ GPU DESCRIPTOR HANDLE& \_ \_ other) const**
</dt> <dd>

Comprueba si hay desigualdad entre el identificador del DESCRIPTOR de GPU CD3DX12 actual y el identificador del descriptor de GPU D3D12 o el identificador del descriptor de \_ \_ GPU \_ \_ \_ \_ CD3DX12 \_ \_ \_ especificado.

</dd> <dt>

**operator=(const D3D12 \_ GPU DESCRIPTOR HANDLE &\_ \_ other)**
</dt> <dd>

Establece el identificador de descriptor de GPU CD3DX12 actual en los mismos valores que el identificador de descriptor de GPU D3D12 o el identificador de \_ \_ descriptor de GPU \_ \_ \_ \_ CD3DX12 \_ \_ \_ especificados.

</dd> <dt>

**inline InitOffsetted( \_ In \_ const D3D12 \_ GPU DESCRIPTOR HANDLE &\_ \_ base, INT offsetScaledByIncrementSize)**
</dt> <dd>

Inicializa una estructura [**D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) con el número especificado de elementos. Usa los parámetros siguientes:

\_En \_ const D3D12 GPU DESCRIPTOR HANDLE &base: dirección base desde la que \_ se va a \_ \_ desplazar.

INT offsetScaledByIncrementSize: número de incrementos por los que se va a desplazar.

</dd> <dt>

**inline InitOffsetted( \_ In \_ const D3D12 \_ GPU DESCRIPTOR HANDLE &\_ \_ base, INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Inicializa una estructura [**D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) con un desplazamiento, utilizando el número especificado de descriptores del tamaño especificado. Usa los parámetros siguientes:

\_En \_ const D3D12 GPU DESCRIPTOR HANDLE &base: dirección base desde la que \_ se va a \_ \_ desplazar.

INT offsetInDescriptors: número de descriptores por los que se va a desplazar.

Descriptor de UINTIncrementSize: cantidad por la que se va a incrementar para cada descriptor, incluido el relleno.

</dd> <dt>

**static inline InitOffsetted( \_ Out \_ D3D12 \_ GPU DESCRIPTOR HANDLE &\_ \_ handle, In \_ \_ const D3D12 \_ GPU DESCRIPTOR HANDLE &\_ \_ base, INT offsetScaledByIncrementSize)**
</dt> <dd>

Inicializa una estructura [**D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) con un desplazamiento, utilizando el número especificado de descriptores del tamaño especificado. Usa los parámetros siguientes:

\_Controlador \_ de descriptor de GPU D3D12 &identificador: genera el identificador del DESCRIPTOR de GPU \_ \_ \_ D3D12 \_ \_ \_ resultante.

\_En \_ const D3D12 GPU DESCRIPTOR HANDLE &base: dirección base desde la que \_ se va a \_ \_ desplazar.

INT offsetScaledByIncrementSize: número de incrementos por los que se va a desplazar.

</dd> <dt>

**static inline InitOffsetted( \_ Out \_ D3D12 \_ GPU DESCRIPTOR HANDLE &\_ \_ handle, \_ \_ Inst D3D12 \_ GPU DESCRIPTOR HANDLE &\_ \_ base, INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Inicializa una estructura [**D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) con un desplazamiento, utilizando el número especificado de descriptores del tamaño especificado. Usa los parámetros siguientes:

\_Controlador \_ de descriptor de GPU D3D12 &identificador: genera el identificador del DESCRIPTOR de GPU \_ \_ \_ D3D12 \_ \_ \_ resultante.

\_En \_ const D3D12 GPU DESCRIPTOR HANDLE &base: dirección base desde la que \_ se va a \_ \_ desplazar.

INT offsetInDescriptors: número de descriptores por los que se va a desplazar.

Descriptor de UINTIncrementSize: cantidad por la que se va a incrementar para cada descriptor, incluido el relleno.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDENTIFICADOR DEL DESCRIPTOR DE GPU D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





