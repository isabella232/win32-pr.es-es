---
title: IDXCoreAdapter::QueryState
description: Recupera el estado actual del elemento especificado en el adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 61fc5c601904011de8f343777a95385a16ec3d7e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966360"
---
# <a name="idxcoreadapterquerystate-method"></a>IDXCoreAdapter::QueryState (método)

Recupera el estado actual del elemento especificado en el adaptador. Antes de llamar a **QueryState** para un tipo de propiedad, llame a [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) para confirmar que la consulta del tipo de estado está disponible para este adaptador y sistema operativo (SO).

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

Tipo de elemento de estado en el adaptador cuyo estado desea recuperar. Consulte la tabla de [DXCoreAdapterState para](./ne-dxcore_interface-dxcoreadapterstate.md) obtener más información sobre cada tipo de estado del adaptador.

### <a name="inputstatedetailssize"></a>inputStateDetailsSize

Tipo: **size_t**

Tamaño, en bytes, del búfer de detalles de estado de entrada que se asigna (opcionalmente) y se proporciona en *inputStateDetails*.

### <a name="inputstatedetails-in"></a>inputStateDetails [in]

Tipo: **void \* const**

Puntero opcional a un búfer de detalles de estado de entrada constante que se asigna en la aplicación, que contiene cualquier información sobre la solicitud necesaria para el tipo de estado que especifique en *el estado*. Consulte la tabla de [DXCoreAdapterState para](./ne-dxcore_interface-dxcoreadapterstate.md) obtener más información sobre cualquier requisito de búfer de entrada para un tipo de estado determinado.

### <a name="outputbuffersize"></a>outputBufferSize

Tipo: **size_t**

Tamaño, en bytes, del búfer de salida que se asigna y se proporciona en *outputBuffer.*

### <a name="outputbuffer-out"></a>outputBuffer [out]

Tipo: **\* void**

Puntero a un búfer de salida que se asigna en la aplicación y que la función rellena. Consulte la tabla de [DXCoreAdapterState para](./ne-dxcore_interface-dxcoreadapterstate.md) obtener más información sobre el requisito de búfer de salida para un tipo de estado determinado.

## <a name="returns"></a>Devoluciones

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la función se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un [**código de**](../../com/structure-of-com-error-codes.md) error [HRESULT](../../com/com-error-codes-10.md).

|Valor devuelto|Descripción|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|El adaptador ya no está en un estado válido.|
|DXGI_ERROR_INVALID_CALL|Este sistema operativo (SO) *no* reconoce el tipo de estado especificado en estado. Llame [a IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) para confirmar que la consulta del tipo de estado está disponible para este adaptador y sistema operativo (SO).|
|DXGI_ERROR_UNSUPPORTED|El adaptador no admite el tipo *de* estado especificado en estado . Llame [a IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) para confirmar que la consulta del tipo de estado está disponible para este adaptador y sistema operativo (SO).|
|E_INVALIDARG|Se proporciona un tamaño de búfer insuficiente para *outputBuffer* (o *para inputStateDetails* cuando se necesita un búfer de detalles de estado de entrada).|
|E_POINTER|`nullptr` se proporcionó para *outputBuffer* (o *para inputStateDetails* donde es necesario un búfer de detalles de estado de entrada).|

## <a name="remarks"></a>Observaciones

Consulte [DXCoreAdapterState para](./ne-dxcore_interface-dxcoreadapterstate.md) obtener más información sobre cada tipo de estado de adaptador y qué entradas y salidas se usan. Esta función cero el búfer *outputBuffer* antes de rellenarlo.

## <a name="see-also"></a>Consulte también

[IDXCoreAdapter,](./nn-dxcore_interface-idxcoreadapter.md) [referencia de DXCore,](../dxcore-reference.md) [uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)