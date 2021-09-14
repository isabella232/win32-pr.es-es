---
title: IDXCoreAdapter::GetPropertySize
description: Para una propiedad de adaptador especificada, recupera el tamaño de búfer, en bytes, necesario para una llamada a [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ff077d3c4c827a55f7fd9b10dfe93f1271649f72
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966380"
---
# <a name="idxcoreadaptergetpropertysize-method"></a>IDXCoreAdapter::GetPropertySize (método)

Para una propiedad de adaptador especificada, recupera el tamaño de búfer, en bytes, necesario para una llamada a [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md). Antes de llamar a **GetPropertySize** para un tipo de propiedad, llame a [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que el tipo de propiedad está disponible para este adaptador y sistema operativo (SO).

## <a name="syntax"></a>Sintaxis

```cpp
virtual HRESULT STDMETHODCALLTYPE GetPropertySize(
  DXCoreAdapterProperty property,
  _Out_ size_t *bufferSize) = 0;
```

## <a name="parameters"></a>Parámetros

### <a name="property"></a>propiedad

Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Tipo de la propiedad cuyo tamaño, en bytes, desea recuperar.

### <a name="buffersize-out"></a>bufferSize [out]

Tipo: **size_t \***

Puntero a un **size_t** valor. La función desreferencia el puntero y establece el valor en el tamaño, en bytes, del búfer de salida que debe asignar y pasar como argumento *propertyData* en la llamada a [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).

## <a name="returns"></a>Devoluciones

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la función se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un [**código de**](../../com/structure-of-com-error-codes.md) error [HRESULT](../../com/com-error-codes-10.md).

|Valor devuelto|Descripción|
|-|-|
|DXGI_ERROR_INVALID_CALL|Este sistema operativo  no reconoce el tipo de propiedad especificado en la propiedad . Llame [a IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que el tipo de propiedad está disponible para este adaptador y sistema operativo (SO).|
|DXGI_ERROR_UNSUPPORTED|El adaptador no admite *el* tipo de propiedad especificado en la propiedad . Llame [a IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que el tipo de propiedad está disponible para este adaptador y sistema operativo (SO).|
|E_POINTER|`nullptr`se proporcionó para *bufferSize.*|

## <a name="remarks"></a>Observaciones

Puede llamar a **GetPropertySize en** un adaptador que ya no sea válido. La &mdash; función no producirá errores.

## <a name="see-also"></a>Consulte también

[IDXCoreAdapter,](./nn-dxcore_interface-idxcoreadapter.md) [referencia de DXCore,](../dxcore-reference.md) [uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)