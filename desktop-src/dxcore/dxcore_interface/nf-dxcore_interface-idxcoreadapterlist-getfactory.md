---
title: IDXCoreAdapterList::GetFactory
description: Recupera un puntero de [interfaz IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) al objeto de generador del adaptador DXCore. | IDXCoreAdapterList::GetFactory
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 08dc93f5c7e086e33d15f666a2c5b94fd7dd7e58
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966331"
---
# <a name="idxcoreadapterlistgetfactory-method"></a>IDXCoreAdapterList::GetFactory (método)

Recupera un puntero de [interfaz IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) al objeto de generador del adaptador DXCore. Para obtener instrucciones de programación y ejemplos de código, vea [Uso de DXCore para enumerar adaptadores.](../dxcore-enum-adapters.md)

## <a name="syntax"></a>Sintaxis

```cpp
virtual HRESULT STDMETHODCALLTYPE GetFactory(
  REFIID riid,
  _COM_Outptr_ void** ppvFactory) = 0;

template <class T>
HRESULT GetFactory(
  _COM_Outptr_ T** ppvFactory);
```

## <a name="parameters"></a>Parámetros

### <a name="riid"></a>riid

Tipo: **REFIID**

Referencia al identificador único global (GUID) de la interfaz que desea que se devuelva en *ppvFactory.* Se espera que sea el identificador de interfaz (IID) de [IDXCoreAdapterFactory.](./nn-dxcore_interface-idxcoreadapterfactory.md)

### <a name="ppvfactory-out"></a>ppvFactory [out]

Tipo: **\* \* void**

Dirección de un puntero a una interfaz con el IID especificado en el *parámetro riid.* Tras la devolución correcta, *\* ppvFactory* (la dirección desreferenciada) contiene un puntero al objeto de generador del adaptador DXCore existente. Antes de devolver, la función incrementa el recuento de referencias en la [interfaz IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) del objeto de generador.

## <a name="returns"></a>Devoluciones

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la función se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un [**código de**](../../com/structure-of-com-error-codes.md) error [HRESULT](../../com/com-error-codes-10.md).

|Valor devuelto|Descripción|
|-|-|
|E_NOINTERFACE|Se proporcionó un valor no válido para *riid*.|
|E_POINTER|`nullptr`se proporcionó para *ppvFactory.*|

## <a name="remarks"></a>Observaciones

Durante el tiempo que existe una referencia en una interfaz [IDXCoreAdapterFactory,](./nn-dxcore_interface-idxcoreadapterfactory.md) una interfaz [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) o una interfaz [IDXCoreAdapter,](./nn-dxcore_interface-idxcoreadapter.md) las llamadas adicionales a [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList::GetFactory]()o [IDXCoreAdapter::GetFactory](./nf-dxcore_interface-idxcoreadapter-getfactory.md) devolverán punteros al mismo objeto, lo que aumenta el recuento de referencias de la interfaz **IDXCoreAdapterFactory.**

## <a name="see-also"></a>Consulte también

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [Referencia de DXCore](../dxcore-reference.md), [Uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)
