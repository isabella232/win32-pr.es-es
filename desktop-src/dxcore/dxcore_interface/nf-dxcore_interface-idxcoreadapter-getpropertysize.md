---
title: IDXCoreAdapter::GetPropertySize
description: Para una propiedad de adaptador especificada, recupera el tamaño del búfer, en bytes, que es necesario para una llamada a [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ff077d3c4c827a55f7fd9b10dfe93f1271649f72
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105720148"
---
# <a name="idxcoreadaptergetpropertysize-method"></a>IDXCoreAdapter:: GetPropertySize (método)

Para una propiedad de adaptador especificada, recupera el tamaño del búfer, en bytes, que es necesario para una llamada a [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md). Antes de llamar a **GetPropertySize** para un tipo de propiedad, llame a [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que el tipo de propiedad está disponible para este adaptador y sistema operativo (SO).

## <a name="syntax"></a>Sintaxis

```cpp
virtual HRESULT STDMETHODCALLTYPE GetPropertySize(
  DXCoreAdapterProperty property,
  _Out_ size_t *bufferSize) = 0;
```

## <a name="parameters"></a>Parámetros

### <a name="property"></a>propiedad

Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Tipo de la propiedad cuyo tamaño, en bytes, se desea recuperar.

### <a name="buffersize-out"></a>bufferSize [out]

Tipo: **size_t \***

Puntero a un valor de **size_t** . La función desreferencia el puntero y establece el valor en el tamaño, en bytes, del búfer de salida que se debe asignar y pasar como argumento *propertyData* en la llamada a [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).

## <a name="returns"></a>Devoluciones

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la función se ejecuta correctamente, devuelve **S_OK**. De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valor devuelto|Descripción|
|-|-|
|DXGI_ERROR_INVALID_CALL|Este sistema operativo (SO) no reconoce el tipo de propiedad especificado en la *propiedad* . Llame a [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que el tipo de propiedad está disponible para este adaptador y sistema operativo (SO).|
|DXGI_ERROR_UNSUPPORTED|El adaptador no admite el tipo de propiedad especificado en la *propiedad* . Llame a [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que el tipo de propiedad está disponible para este adaptador y sistema operativo (SO).|
|E_POINTER|`nullptr` se proporcionó para *buffersize*.|

## <a name="remarks"></a>Observaciones

Puede llamar a **GetPropertySize** en un adaptador que ya no sea válido &mdash; . la función no producirá un error.

## <a name="see-also"></a>Vea también

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)