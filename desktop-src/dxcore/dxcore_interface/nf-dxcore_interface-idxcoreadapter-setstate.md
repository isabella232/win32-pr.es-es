---
title: IDXCoreAdapter::SetState
description: Establece el estado del elemento especificado en el adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c80ca670be26ffdcefa5e89cee079d2225d204ee97e99e41f69686300a46230b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042913"
---
# <a name="idxcoreadaptersetstate-method"></a>IDXCoreAdapter::SetState (método)

Establece el estado del elemento especificado en el adaptador. Antes de llamar a **SetState** para un tipo de propiedad, llame a [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) para confirmar que el establecimiento del tipo de estado está disponible para este adaptador y sistema operativo (SO).

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

Tipo de elemento de estado en el adaptador cuyo estado desea establecer. Consulte la tabla de [DXCoreAdapterState para](./ne-dxcore_interface-dxcoreadapterstate.md) obtener más información sobre cada tipo de estado del adaptador.

### <a name="inputstatedetailssize"></a>inputStateDetailsSize

Tipo: **size_t**

Tamaño, en bytes, del búfer de detalles de estado de entrada que se asigna (opcionalmente) y se proporciona en *inputStateDetails*.

### <a name="inputstatedetails-in"></a>inputStateDetails [in]

Tipo: **void \* const**

Puntero opcional a un búfer de detalles de estado de entrada constante que se asigna en la aplicación, que contiene cualquier información sobre la solicitud necesaria para el tipo de estado que especifique en *el estado*. Consulte la tabla de [DXCoreAdapterState para](./ne-dxcore_interface-dxcoreadapterstate.md) obtener más información sobre cualquier requisito de búfer de entrada para un tipo de estado determinado.

### <a name="inputdatasize"></a>inputDataSize

Tipo: **size_t**

Tamaño, en bytes, del búfer de entrada que se asigna y se proporciona en *inputData.*

### <a name="inputdata-in"></a>inputData [in]

Tipo: **\* void**

Puntero a un búfer de entrada que se asigna en la aplicación, que contiene la información de estado que se va a establecer para el elemento de estado cuyo tipo especifique en *estado*. Consulte la tabla de [DXCoreAdapterState para](./ne-dxcore_interface-dxcoreadapterstate.md) obtener más información sobre el requisito de búfer de entrada para un tipo de estado determinado.

## <a name="returns"></a>Devoluciones

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la función se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un [**código de**](../../com/structure-of-com-error-codes.md) error [HRESULT](../../com/com-error-codes-10.md).

|Valor devuelto|Descripción|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|El adaptador ya no está en un estado válido.|
|DXGI_ERROR_INVALID_CALL|Este sistema operativo (SO) *no* reconoce el tipo de estado especificado en estado. Llame [a IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) para confirmar que la configuración del tipo de estado está disponible para este adaptador y sistema operativo (SO).|
|DXGI_ERROR_UNSUPPORTED|El adaptador no admite el tipo *de* estado especificado en estado . Llame [a IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) para confirmar que la configuración del tipo de estado está disponible para este adaptador y sistema operativo (SO).|
|E_INVALIDARG|Se proporciona un tamaño de búfer insuficiente para *inputData* (o *para inputStateDetails* cuando se necesita un búfer de detalles de estado de entrada).|
|E_POINTER|`nullptr` se proporcionó para *inputData* (o *para inputStateDetails* donde es necesario un búfer de detalles de estado de entrada).|

## <a name="see-also"></a>Vea también

[IDXCoreAdapter,](./nn-dxcore_interface-idxcoreadapter.md) [referencia de DXCore,](../dxcore-reference.md) [uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)