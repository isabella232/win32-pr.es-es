---
title: IDXCoreAdapter::SetState
description: Establece el estado del elemento especificado en el adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8cbeacdb8c6020441b5dd74a9f9233a6c112b4f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105720158"
---
# <a name="idxcoreadaptersetstate-method"></a>IDXCoreAdapter:: SetState (método)

Establece el estado del elemento especificado en el adaptador. Antes de llamar a **SetState** para un tipo de propiedad, llame a [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) para confirmar que el establecimiento de la clase de estado está disponible para este adaptador y sistema operativo (SO).

## <a name="syntax"></a>Sintaxis

```cpp
virtual HRESULT STDMETHODCALLTYPE SetState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t inputDataSize,
  _In_reads_bytes_(inputDataSize) const void *inputData) = 0;

template <class T1, class T2>
HRESULT SetState( 
  DXCoreAdapterState state,
  const T1 *inputStateDetails,
  const T2 *inputData);
```

## <a name="parameters"></a>Parámetros

### <a name="state"></a>state

Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

El tipo de elemento de estado en el adaptador cuyo estado desea establecer. Vea la tabla en [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obtener más información sobre cada tipo de estado del adaptador.

### <a name="inputstatedetailssize"></a>inputStateDetailsSize

Tipo: **size_t**

El tamaño, en bytes, del búfer de detalles de estado de entrada que se asigna y proporciona de forma opcional en *inputStateDetails*.

### <a name="inputstatedetails-in"></a>inputStateDetails [in]

Tipo: **void const \***

Un puntero opcional a un búfer de detalles de estado de entrada constante que se asigna en la aplicación, que contiene información sobre la solicitud que se requiere para la clase de estado que se especifica en el *Estado*. Vea la tabla en [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obtener más información sobre cualquier requisito de búfer de entrada para un tipo de estado determinado.

### <a name="inputdatasize"></a>inputDataSize

Tipo: **size_t**

El tamaño, en bytes, del búfer de entrada que asigna y proporciona en *inputData*.

### <a name="inputdata-in"></a>inputData [in]

Tipo: **void \***

Un puntero a un búfer de entrada que se asigna en la aplicación, que contiene la información de estado que se va a establecer para el elemento de Estado cuyo tipo se especifica en el *Estado*. Vea la tabla en [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obtener más información sobre el requisito de búfer de entrada para un tipo de estado determinado.

## <a name="returns"></a>Devoluciones

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la función se ejecuta correctamente, devuelve **S_OK**. De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valor devuelto|Descripción|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|El adaptador ya no tiene un estado válido.|
|DXGI_ERROR_INVALID_CALL|Este sistema operativo (SO) no reconoce la clase de estado especificada en *Estado* . Llame a [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) para confirmar que el establecimiento de la clase de estado está disponible para este adaptador y sistema operativo (SO).|
|DXGI_ERROR_UNSUPPORTED|El adaptador no admite la clase de estado especificada en el *Estado* . Llame a [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) para confirmar que el establecimiento de la clase de estado está disponible para este adaptador y sistema operativo (SO).|
|E_INVALIDARG|Se proporciona un tamaño de búfer insuficiente para *inputData* (o para *inputStateDetails* cuando se necesita un búfer de detalles de estado de entrada).|
|E_POINTER|`nullptr` se proporcionó para *inputData* (o para *inputStateDetails* cuando se necesita un búfer de detalles de estado de entrada).|

## <a name="see-also"></a>Vea también

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)