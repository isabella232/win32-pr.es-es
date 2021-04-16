---
title: CD3DX12_CPU_DESCRIPTOR_HANDLE estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ \_ estructura de identificador de descriptor de CPU de D3D12 \_ .
ms.assetid: 91736069-7D13-47B0-B78C-0F6F104F97EB
keywords:
- Estructura de CD3DX12_CPU_DESCRIPTOR_HANDLE
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
ms.openlocfilehash: 5d1045202c531aa200745fc89ed067628a175486
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649388"
---
# <a name="cd3dx12_cpu_descriptor_handle-structure"></a>CD3DX12 \_ \_ estructura de identificador de descriptor de CPU \_

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ \_ identificador de descriptor de CPU de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) .

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

**\_Identificador de \_ descriptor de CPU de CD3DX12 \_ ()**
</dt> <dd>

Crea una nueva instancia no inicializada de un \_ \_ identificador de descriptor de CPU de CD3DX12 \_ .

</dd> <dt>

**identificador de \_ descriptor de CPU de CD3DX12 explícito \_ \_ (const D3D12 \_ \_ identificador del descriptor de CPU \_ &o)**
</dt> <dd>

Crea una nueva instancia de un \_ identificador de \_ descriptor de CPU de CD3DX12 \_ , inicializado con el contenido de otra estructura de [**\_ \_ \_ identificador de descriptor de CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) .

</dd> <dt>

**\_Identificador de \_ descriptor de CPU de CD3DX12 \_ ( \_ valor predeterminado de CD3DX12)**
</dt> <dd>

Crea una nueva instancia de un \_ identificador de \_ descriptor de CPU de CD3DX12 \_ , inicializado con los parámetros predeterminados (puntero establecido en cero).

</dd> <dt>

**\_ \_ Identificador de descriptor de CPU de CD3DX12 \_ ( \_ \_ identificador de descriptor de CPU const D3D12 \_ &otro, int offsetScaledByIncrementSize)**
</dt> <dd>

Crea una nueva instancia de un \_ identificador de \_ descriptor de CPU de CD3DX12 \_ , inicializando los siguientes parámetros:

D3D12 \_ \_ identificador de descriptor de CPU \_ &otro

INT offsetScaledByIncrementSize: número de incrementos que se van a desplazar.

</dd> <dt>

**\_ \_ Identificador de descriptor de CPU de CD3DX12 \_ ( \_ \_ identificador de descriptor de CPU const D3D12 \_ &otro, int offsetInDescriptors, uint descriptorIncrementSize)**
</dt> <dd>

Crea una nueva instancia de un \_ identificador de \_ descriptor de CPU de CD3DX12 \_ , inicializando los siguientes parámetros:

D3D12 \_ \_ identificador de descriptor de CPU \_ &otro

INT offsetInDescriptors: número de descriptores por los que se va a incrementar.

UINT descriptorIncrementSize: cantidad por la que se va a incrementar para cada descriptor, incluido el relleno.

</dd> <dt>

**Offset (INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Establece el desplazamiento en función del número especificado de descriptores y la cantidad de incremento para cada descriptor. Usa los siguientes parámetros:

INT offsetInDescriptors: número de descriptores por los que se va a incrementar.

UINT descriptorIncrementSize: cantidad por la que se va a incrementar para cada descriptor, incluido el relleno.

</dd> <dt>

**Offset (INT offsetScaledByIncrementSize)**
</dt> <dd>

Establece el desplazamiento en función del número de incrementos especificado. Usa los siguientes parámetros:

INT offsetScaledByIncrementSize: número de incrementos que se van a desplazar.

</dd> <dt>

**operador = = ( \_ en el \_ \_ identificador de descriptor de CPU const D3D12 \_ \_& otros) Const**
</dt> <dd>

Comprueba la igualdad entre el identificador del \_ descriptor de la CPU de CD3DX12 actual \_ y el identificador de \_ descriptor de CPU D3D12 especificado o el identificador del descriptor \_ \_ \_ de \_ CPU CD3DX12 \_ \_ .

</dd> <dt>

**operador! = ( \_ en el \_ \_ identificador de descriptor de CPU const D3D12 \_ \_& otros) Const**
</dt> <dd>

Comprueba la desigualdad entre el identificador del descriptor de la CPU de CD3DX12 actual \_ \_ \_ y el identificador del descriptor de CPU de D3D12 o el identificador del descriptor de la \_ \_ \_ \_ CPU CD3DX12 \_ \_ .

</dd> <dt>

**Operator = (const D3D12 \_ \_ identificador del descriptor de CPU \_ &otro)**
</dt> <dd>

Establece el identificador del \_ descriptor de la CPU de CD3DX12 actual \_ \_ en los mismos valores que el identificador de descriptor de CPU D3D12 especificado o el identificador del descriptor \_ \_ \_ de \_ CPU CD3DX12 \_ \_ .

</dd> <dt>

**InitOffsetted en línea ( \_ en \_ const D3D12 \_ \_ identificador del descriptor de CPU \_ &base, int offsetScaledByIncrementSize)**
</dt> <dd>

Inicializa una estructura [**de \_ \_ \_ identificador de descriptor de CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con el número de elementos especificado. Usa los siguientes parámetros:

\_En \_ \_ \_ el identificador de descriptor de CPU const D3D12 \_ &base: la dirección base de la que se va a desplazar.

INT offsetScaledByIncrementSize: número de incrementos que se van a desplazar.

</dd> <dt>

**InitOffsetted en línea ( \_ en \_ const D3D12 \_ \_ identificador del descriptor de CPU \_ &base, int offsetInDescriptors, uint descriptorIncrementSize)**
</dt> <dd>

Inicializa una estructura [**de \_ \_ \_ identificador de descriptor de CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con un desplazamiento, utilizando el número especificado de descriptores del tamaño dado. Usa los siguientes parámetros:

\_En \_ \_ \_ el identificador de descriptor de CPU const D3D12 \_ &base: la dirección base de la que se va a desplazar.

INT offsetInDescriptors: número de descriptores por los que se va a desplazar.

UINT descriptorIncrementSize: cantidad por la que se va a incrementar para cada descriptor, incluido el relleno.

</dd> <dt>

**Static inline InitOffsetted ( \_ salida \_ D3D12 \_ identificador \_ de descriptor \_ de CPU &identificador, \_ en \_ const D3D12 \_ CPU \_ \_ handler &base, int offsetScaledByIncrementSize)**
</dt> <dd>

Inicializa una estructura [**de \_ \_ \_ identificador de descriptor de CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con un desplazamiento, utilizando el número especificado de descriptores del tamaño dado. Usa los siguientes parámetros:

\_Out \_ \_ &identificador \_ de descriptor de CPU D3D12 \_ : genera \_ el \_ identificador de descriptor de CPU D3D12 resultante \_ .

\_En \_ \_ \_ el identificador de descriptor de CPU const D3D12 \_ &base: la dirección base de la que se va a desplazar.

INT offsetScaledByIncrementSize: número de incrementos que se van a desplazar.

</dd> <dt>

**Static inline InitOffsetted ( \_ salida \_ D3D12 \_ identificador \_ de descriptor \_ de CPU &identificador, \_ en \_ const D3D12 \_ CPU \_ \_ handler &base, int offsetInDescriptors, uint descriptorIncrementSize)**
</dt> <dd>

Inicializa una estructura [**de \_ \_ \_ identificador de descriptor de CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) con un desplazamiento, utilizando el número especificado de descriptores del tamaño dado. Usa los siguientes parámetros:

\_Out \_ \_ &identificador \_ de descriptor de CPU D3D12 \_ : genera \_ el \_ identificador de descriptor de CPU D3D12 resultante \_ .

\_En \_ \_ \_ el identificador de descriptor de CPU const D3D12 \_ &base: la dirección base de la que se va a desplazar.

INT offsetInDescriptors: número de descriptores por los que se va a desplazar.

UINT descriptorIncrementSize: cantidad por la que se va a incrementar para cada descriptor, incluido el relleno.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





