---
title: IDXCoreAdapter::GetProperty
description: Recupera el valor de la propiedad del adaptador especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c8a7f7b36fdb0128b4047335051823da07a074c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359349"
---
# <a name="idxcoreadaptergetproperty-method"></a>IDXCoreAdapter:: GetProperty (método)

Recupera el valor de la propiedad del adaptador especificado. Antes de llamar a **GetProperty** para un tipo de propiedad, llame a [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que el tipo de propiedad está disponible para este adaptador y sistema operativo (SO). Además, antes de llamar a **GetProperty**, llame a [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para determinar el tamaño necesario del búfer en el que se va a recibir el valor de propiedad.

## <a name="syntax"></a>Sintaxis

```cpp
virtual HRESULT STDMETHODCALLTYPE GetProperty(
  DXCoreAdapterProperty property,
  size_t bufferSize,
  _Out_writes_bytes_(bufferSize) void *propertyData) = 0;

template <class T>
HRESULT GetProperty( 
  DXCoreAdapterProperty property,
  _Out_writes_bytes_(sizeof(T)) T *propertyData);
```

## <a name="parameters"></a>Parámetros

### <a name="property"></a>propiedad

Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Tipo de la propiedad cuyo valor se desea recuperar. Vea la tabla en [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) para obtener más información sobre cada propiedad del adaptador.

### <a name="buffersize"></a>bufferSize

Tipo: **size_t**

El tamaño, en bytes, del búfer de salida que asigna y proporciona en *propertyData*.

### <a name="propertydata-out"></a>propertyData [out]

Tipo: **void \***

Un puntero a un búfer de salida que se asigna en la aplicación y que la función rellena. Llame a [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para determinar el tamaño que debe tener el búfer *propertyData* para una propiedad de adaptador determinada.

## <a name="returns"></a>Devoluciones

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la función se ejecuta correctamente, devuelve **S_OK**. De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valor devuelto|Descripción|
|-|-|
|DXGI_ERROR_INVALID_CALL|Este sistema operativo (SO) no reconoce el tipo de propiedad especificado en la *propiedad* . Llame a [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que el tipo de propiedad está disponible para este adaptador y sistema operativo (SO).|
|DXGI_ERROR_UNSUPPORTED|El adaptador no admite el tipo de propiedad especificado en la *propiedad* . Llame a [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que el tipo de propiedad está disponible para este adaptador y sistema operativo (SO).|
|E_INVALIDARG|En *propertyData*, se proporciona un tamaño de búfer insuficiente. Llame a [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para determinar el tamaño que debe tener el búfer *propertyData* para una propiedad de adaptador determinada.|
|E_POINTER|`nullptr` se proporcionó para *propertyData*.|

## <a name="remarks"></a>Observaciones

Puede llamar a **GetProperty** en un adaptador que ya no sea válido &mdash; . la función no producirá un error como resultado de eso. Esta función pone en cero el búfer de *propertyData* antes de rellenarlo.

## <a name="see-also"></a>Vea también

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)