---
title: IDXCoreAdapterFactory::GetAdapterByLuid
description: Recupera el objeto de adaptador DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) para un LUID especificado, si está disponible.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 30835948978e5c7f3f11f903322e4fa41f71d210
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421139"
---
# <a name="idxcoreadapterfactorygetadapterbyluid-method"></a>IDXCoreAdapterFactory:: GetAdapterByLuid (método)

Recupera el objeto de adaptador DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) para un LUID especificado, si está disponible. Para obtener instrucciones de programación y ejemplos de código, vea [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintaxis

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
   REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a>Parámetros

### <a name="adapterluid"></a>adapterLUID

Tipo: **[LUID](/windows/win32/api/winnt/ns-winnt-luid) const\&**

Valor único local que identifica la instancia del adaptador.

### <a name="riid-in"></a>riid [in]

Tipo: **REFIID**

Referencia al identificador único global (GUID) de la interfaz que desea que se devuelva en *ppvAdapter*. Se espera que sea el identificador de interfaz (IID) de [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).

### <a name="ppvadapter-out"></a>ppvAdapter [out]

Tipo: **void \* \***

Dirección de un puntero a una interfaz con el IID especificado en el parámetro *riid* . Si la devolución es correcta, *\* ppvAdapter* (la dirección desreferenciada) contiene un puntero al adaptador DXCore creado.

## <a name="returns"></a>Devoluciones

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la función se ejecuta correctamente, devuelve **S_OK**. De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valor devuelto|Descripción|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|Se reconoce el LUID de adaptador pasado en *adapterLUID* , pero el adaptador ya no tiene un estado válido.|
|E_INVALIDARG|No se dispone de este LUID de adaptador como el valor pasado en *adapterLUID* a través de DXCore.|
|E_NOINTERFACE|Se proporcionó un valor no válido para *riid*.|
|E_POINTER|`nullptr` se proporcionó para *ppvAdapter*.|

## <a name="remarks"></a>Observaciones

Varias llamadas que pasan el mismo [LUID](/windows/win32/api/winnt/ns-winnt-luid) devuelven punteros de interfaz idénticos. Como resultado, es seguro comparar los punteros de interfaz para determinar si varios punteros hacen referencia al mismo objeto de adaptador.

## <a name="see-also"></a>Vea también

[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)