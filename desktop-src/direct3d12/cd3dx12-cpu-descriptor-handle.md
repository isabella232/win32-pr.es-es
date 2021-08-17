---
title: CD3DX12_CPU_DESCRIPTOR_HANDLE estructura (D3dx12.h)
description: Estructura del asistente para permitir la inicialización sencilla de una estructura handle del \_ DESCRIPTOR de CPU D3D12. \_ \_
ms.assetid: 91736069-7D13-47B0-B78C-0F6F104F97EB
keywords:
- CD3DX12_CPU_DESCRIPTOR_HANDLE estructura
topic_type:
- apiref
api_name:
- CD3DX12_CPU_DESCRIPTOR_HANDLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e6fd6ba75caccf19f3782e0c39581d1e652de0c4187c3c5a203bb5f3b7ceec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117913082"
---
# <a name="cd3dx12_cpu_descriptor_handle-structure"></a>Estructura DEL IDENTIFICADOR DEL \_ \_ DESCRIPTOR DE CPU CD3DX12 \_

Estructura del asistente para permitir la inicialización sencilla de una estructura handle del [**\_ DESCRIPTOR de CPU \_ D3D12. \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_CPU_DESCRIPTOR_HANDLE  : public D3D12_CPU_DESCRIPTOR_HANDLE{
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE();
                                  explicit CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &o);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(CD3DX12_DEFAULT);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &other, INT offsetScaledByIncrementSize);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_CPU_DESCRIPTOR_HANDLE&  Offset(INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_CPU_DESCRIPTOR_HANDLE&  Offset(INT offsetScaledByIncrementSize);
  bool                            operator==( _In_ const D3D12_CPU_DESCRIPTOR_HANDLE& other) const;
  bool                            operator!=(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE& other) const;
  CD3DX12_CPU_DESCRIPTOR_HANDLE & operator=(const D3D12_CPU_DESCRIPTOR_HANDLE &other);
  void                            inline InitOffsetted(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            inline InitOffsetted(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_CPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_CPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**IDENTIFICADOR DEL DESCRIPTOR DE \_ CPU CD3DX12() \_ \_**
</dt> <dd>

Crea una nueva instancia sin inicializar de un IDENTIFICADOR DE DESCRIPTOR DE CPU CD3DX12. \_ \_ \_

</dd> <dt>

**identificador explícito del \_ DESCRIPTOR de CPU CD3DX12(const \_ \_ D3D12 \_ CPU DESCRIPTOR HANDLE &\_ \_ o)**
</dt> <dd>

Crea una nueva instancia de un IDENTIFICADOR DE DESCRIPTOR de CPU CD3DX12, inicializado con el contenido de otra estructura de IDENTIFICADOR \_ \_ DEL DESCRIPTOR de \_ [**\_ \_ CPU \_ D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)

</dd> <dt>

**IDENTIFICADOR DEL DESCRIPTOR DE CPU CD3DX12 \_ \_ \_ (CD3DX12 \_ PREDETERMINADO)**
</dt> <dd>

Crea una nueva instancia de un IDENTIFICADOR DE DESCRIPTOR DE CPU CD3DX12, inicializado con parámetros \_ \_ predeterminados \_ (puntero establecido en cero).

</dd> <dt>

**IDENTIFICADOR DEL \_ DESCRIPTOR DE CPU CD3DX12(const \_ \_ D3D12 \_ CPU DESCRIPTOR HANDLE &\_ \_ otros, INT offsetScaledByIncrementSize)**
</dt> <dd>

Crea una nueva instancia de un IDENTIFICADOR DE DESCRIPTOR DE CPU CD3DX12, \_ \_ \_ inicializando los parámetros siguientes:

Identificador del DESCRIPTOR de CPU D3D12 \_ \_ &\_ otros

INT offsetScaledByIncrementSize: número de incrementos por los que se va a desplazar.

</dd> <dt>

**CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE(const D3D12 \_ CPU DESCRIPTOR HANDLE &\_ \_ other, INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Crea una nueva instancia de un IDENTIFICADOR DE DESCRIPTOR DE CPU CD3DX12, \_ \_ \_ inicializando los parámetros siguientes:

Identificador del DESCRIPTOR de CPU D3D12 \_ \_ &\_ otros

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

**operator==( \_ In \_ const D3D12 \_ CPU DESCRIPTOR HANDLE& \_ \_ other) const**
</dt> <dd>

Comprueba la igualdad entre el identificador actual del DESCRIPTOR de CPU CD3DX12 y el identificador del DESCRIPTOR de CPU D3D12 especificado o el identificador del \_ \_ DESCRIPTOR de CPU \_ \_ \_ \_ CD3DX12. \_ \_ \_

</dd> <dt>

**operator!=( \_ In \_ const D3D12 \_ CPU DESCRIPTOR HANDLE& \_ \_ other) const**
</dt> <dd>

Comprueba si hay desigualdad entre el identificador actual del DESCRIPTOR de CPU CD3DX12 y el identificador del DESCRIPTOR de CPU D3D12 especificado o el identificador del \_ \_ DESCRIPTOR de CPU \_ \_ \_ \_ CD3DX12. \_ \_ \_

</dd> <dt>

**operator=(const D3D12 \_ CPU DESCRIPTOR HANDLE &\_ \_ other)**
</dt> <dd>

Establece el identificador del DESCRIPTOR de CPU CD3DX12 actual en los mismos valores que el identificador del DESCRIPTOR de CPU D3D12 especificado o el identificador del DESCRIPTOR de \_ \_ CPU \_ \_ \_ \_ CD3DX12. \_ \_ \_

</dd> <dt>

**inline InitOffsetted( \_ In \_ const D3D12 \_ CPU DESCRIPTOR HANDLE &\_ \_ base, INT offsetScaledByIncrementSize)**
</dt> <dd>

Inicializa una estructura HANDLE del DESCRIPTOR de [**\_ \_ CPU \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con el número especificado de elementos. Usa los parámetros siguientes:

\_En \_ const D3D12 CPU DESCRIPTOR HANDLE &base: dirección base desde la que se \_ va a \_ \_ desplazar.

INT offsetScaledByIncrementSize: número de incrementos por los que se va a desplazar.

</dd> <dt>

**inline InitOffsetted( \_ In \_ const D3D12 \_ CPU DESCRIPTOR HANDLE &\_ \_ base, INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Inicializa una estructura HANDLE del DESCRIPTOR de [**\_ \_ CPU \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con un desplazamiento, utilizando el número especificado de descriptores del tamaño especificado. Usa los parámetros siguientes:

\_En \_ const D3D12 CPU DESCRIPTOR HANDLE &base: dirección base desde la que se \_ va a \_ \_ desplazar.

INT offsetInDescriptors: número de descriptores por los que se va a desplazar.

Descriptor de UINTIncrementSize: cantidad por la que se va a incrementar para cada descriptor, incluido el relleno.

</dd> <dt>

**static inline InitOffsetted( \_ Out \_ D3D12 \_ CPU DESCRIPTOR HANDLE &\_ \_ handle, In \_ \_ const D3D12 \_ CPU DESCRIPTOR HANDLE &\_ \_ base, INT offsetScaledByIncrementSize)**
</dt> <dd>

Inicializa una estructura HANDLE del DESCRIPTOR de [**\_ \_ CPU \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con un desplazamiento, utilizando el número especificado de descriptores del tamaño especificado. Usa los parámetros siguientes:

\_Out \_ D3D12 CPU DESCRIPTOR HANDLE &handle (Controlador de descriptor de \_ CPU \_ \_ D3D12 de salida): genera el identificador del DESCRIPTOR de CPU D3D12 \_ \_ \_ resultante.

\_En \_ const D3D12 CPU DESCRIPTOR HANDLE &base: dirección base desde la que se \_ va a \_ \_ desplazar.

INT offsetScaledByIncrementSize: número de incrementos por los que se va a desplazar.

</dd> <dt>

**static inline InitOffsetted( \_ Out \_ D3D12 \_ CPU DESCRIPTOR HANDLE &\_ \_ handle, In \_ \_ const D3D12 \_ CPU DESCRIPTOR HANDLE &\_ \_ base, INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Inicializa una estructura HANDLE del DESCRIPTOR de [**\_ \_ CPU \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con un desplazamiento, utilizando el número especificado de descriptores del tamaño especificado. Usa los parámetros siguientes:

\_Out \_ D3D12 CPU DESCRIPTOR HANDLE &handle (Controlador de descriptor de \_ CPU \_ \_ D3D12 de salida): genera el identificador del DESCRIPTOR de CPU D3D12 \_ \_ \_ resultante.

\_En \_ const D3D12 CPU DESCRIPTOR HANDLE &base: dirección base desde la que se \_ va a \_ \_ desplazar.

INT offsetInDescriptors: número de descriptores por los que se va a desplazar.

Descriptor de UINTIncrementSize: cantidad por la que se va a incrementar para cada descriptor, incluido el relleno.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





