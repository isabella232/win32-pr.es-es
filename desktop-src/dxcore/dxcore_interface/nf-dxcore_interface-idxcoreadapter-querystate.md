---
title: IDXCoreAdapter::QueryState
description: Recupera el estado actual del elemento especificado en el adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 61fc5c601904011de8f343777a95385a16ec3d7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105720159"
---
# <a name="idxcoreadapterquerystate-method"></a>IDXCoreAdapter:: QueryState (método)

Recupera el estado actual del elemento especificado en el adaptador. Antes de llamar a **QueryState** para un tipo de propiedad, llame a [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) para confirmar que la consulta de la clase de estado está disponible para este adaptador y sistema operativo (SO).

## <a name="syntax"></a>Sintaxis

```cpp
virtual HRESULT STDMETHODCALLTYPE QueryState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t outputBufferSize,
  _Out_writes_bytes_(outputBufferSize) void *outputBuffer) = 0;

template <class T1, class T2>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _In_reads_bytes_opt_(sizeof(T1)) const T1 *inputStateDetails,
  _Out_writes_bytes_(sizeof(T2)) T2 *outputBuffer);

template <class T>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _Out_writes_bytes_(sizeof(T)) T *outputBuffer);
```

## <a name="parameters"></a>Parámetros

### <a name="state"></a>state

Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

El tipo de elemento de estado en el adaptador cuyo estado desea recuperar. Vea la tabla en [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obtener más información sobre cada tipo de estado del adaptador.

### <a name="inputstatedetailssize"></a>inputStateDetailsSize

Tipo: **size_t**

El tamaño, en bytes, del búfer de detalles de estado de entrada que se asigna y proporciona de forma opcional en *inputStateDetails*.

### <a name="inputstatedetails-in"></a>inputStateDetails [in]

Tipo: **void const \***

Un puntero opcional a un búfer de detalles de estado de entrada constante que se asigna en la aplicación, que contiene información sobre la solicitud que se requiere para la clase de estado que se especifica en el *Estado*. Vea la tabla en [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obtener más información sobre cualquier requisito de búfer de entrada para un tipo de estado determinado.

### <a name="outputbuffersize"></a>outputBufferSize

Tipo: **size_t**

El tamaño, en bytes, del búfer de salida que asigna y proporciona en *outputBuffer*.

### <a name="outputbuffer-out"></a>outputBuffer [out]

Tipo: **void \***

Un puntero a un búfer de salida que se asigna en la aplicación y que la función rellena. Vea la tabla en [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obtener más información sobre el requisito de búfer de salida para un tipo de estado determinado.

## <a name="returns"></a>Devoluciones

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la función se ejecuta correctamente, devuelve **S_OK**. De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valor devuelto|Descripción|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|El adaptador ya no tiene un estado válido.|
|DXGI_ERROR_INVALID_CALL|Este sistema operativo (SO) no reconoce la clase de estado especificada en *Estado* . Llame a [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) para confirmar que la consulta de la clase de estado está disponible para este adaptador y sistema operativo (SO).|
|DXGI_ERROR_UNSUPPORTED|El adaptador no admite la clase de estado especificada en el *Estado* . Llame a [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) para confirmar que la consulta de la clase de estado está disponible para este adaptador y sistema operativo (SO).|
|E_INVALIDARG|Se proporciona un tamaño de búfer insuficiente para *outputBuffer* (o para *inputStateDetails* cuando se necesita un búfer de detalles de estado de entrada).|
|E_POINTER|`nullptr` se proporcionó para *outputBuffer* (o para *inputStateDetails* cuando se necesita un búfer de detalles de estado de entrada).|

## <a name="remarks"></a>Observaciones

Consulte [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obtener más información sobre cada tipo de estado del adaptador y qué entradas y salidas se usan. Esta función pone en cero el búfer de *outputBuffer* antes de rellenarlo.

## <a name="see-also"></a>Vea también

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)