---
title: IDXCoreAdapter::GetProperty
description: Recupera el valor de la propiedad de adaptador especificada.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8adb48994580125d153c36394c4db65cb38f4a08306814d1638e5c27eb3d4868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279405"
---
# <a name="idxcoreadaptergetproperty-method"></a>IDXCoreAdapter::GetProperty (método)

Recupera el valor de la propiedad de adaptador especificada. Antes de llamar a **GetProperty** para un tipo de propiedad, llame a [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que el tipo de propiedad está disponible para este adaptador y sistema operativo (SO). También antes de **llamar a GetProperty**, llame a [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para determinar el tamaño necesario del búfer en el que se va a recibir el valor de propiedad.

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

Tipo de la propiedad cuyo valor desea recuperar. Consulte la tabla de [DXCoreAdapterProperty para](./ne-dxcore_interface-dxcoreadapterproperty.md) obtener más información sobre cada propiedad del adaptador.

### <a name="buffersize"></a>bufferSize

Tipo: **size_t**

Tamaño, en bytes, del búfer de salida que asigna y proporciona en *propertyData.*

### <a name="propertydata-out"></a>propertyData [out]

Tipo: **\* void**

Puntero a un búfer de salida que se asigna en la aplicación y que la función rellena. Llame [a GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para determinar el tamaño que debe tener el búfer *propertyData* para una propiedad de adaptador determinada.

## <a name="returns"></a>Devoluciones

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la función se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un [**código de**](../../com/structure-of-com-error-codes.md) error [HRESULT](../../com/com-error-codes-10.md).

|Valor devuelto|Descripción|
|-|-|
|DXGI_ERROR_INVALID_CALL|Este sistema operativo  (SO) no reconoce el tipo de propiedad especificado en la propiedad . Llame [a IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que el tipo de propiedad está disponible para este adaptador y sistema operativo (SO).|
|DXGI_ERROR_UNSUPPORTED|El adaptador no admite *el* tipo de propiedad especificado en la propiedad . Llame [a IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que el tipo de propiedad está disponible para este adaptador y sistema operativo (SO).|
|E_INVALIDARG|Se proporciona un tamaño de búfer insuficiente en *propertyData.* Llame [a GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para determinar el tamaño que debe tener el búfer *propertyData* para una propiedad de adaptador determinada.|
|E_POINTER|`nullptr`se proporcionó para *propertyData.*|

## <a name="remarks"></a>Comentarios

Como resultado, puede llamar a **GetProperty** en un adaptador que ya no sea válido. &mdash; Esta función cero el búfer *propertyData* antes de rellenarlo.

## <a name="see-also"></a>Consulte también

[IDXCoreAdapter,](./nn-dxcore_interface-idxcoreadapter.md) [referencia de DXCore,](../dxcore-reference.md) [uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)