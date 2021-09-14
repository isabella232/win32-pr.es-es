---
title: IDXCoreAdapterList::GetAdapter
description: Recupera un adaptador específico por índice de un objeto de lista de adaptadores DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 5ba03c9e6f2711adc5264354a6abd70ee489965f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966328"
---
# <a name="idxcoreadapterlistgetadapter-method"></a>IDXCoreAdapterList::GetAdapter (método)

Recupera un adaptador específico por índice de un objeto de lista de adaptadores DXCore. Para obtener instrucciones de programación y ejemplos de código, [vea Uso de DXCore para enumerar adaptadores.](../dxcore-enum-adapters.md)

## <a name="syntax"></a>Sintaxis

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapter(
  uint32_t index,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapter( 
  uint32_t index,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a>Parámetros

### <a name="index"></a>índice

Tipo: **uint32_t**

Índice de base cero que identifica una instancia de adaptador dentro de la lista de adaptadores DXCore.

### <a name="riid"></a>riid

Tipo: **REFIID**

Referencia al identificador único global (GUID) de la interfaz que desea que se devuelva en *ppvAdapter.* Se espera que sea el identificador de interfaz (IID) [de IDXCoreAdapter.](./nn-dxcore_interface-idxcoreadapter.md)

### <a name="ppvadapter-out"></a>ppvAdapter [out]

Tipo: **\* \* void**

Dirección de un puntero a una interfaz con el IID especificado en el *parámetro riid.* Tras la devolución correcta, *\* ppvAdapter* (la dirección desreferenciada) contiene un puntero al adaptador DXCore creado.

## <a name="returns"></a>Devoluciones

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la función se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un [**código de**](../../com/structure-of-com-error-codes.md) error [HRESULT](../../com/com-error-codes-10.md).

|Valor devuelto|Descripción|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|El *índice* es válido, pero el adaptador ya no está en un estado válido.|
|E_INVALIDARG|El índice *proporcionado* no es válido.|
|E_NOINTERFACE|Se proporcionó un valor no válido para *riid*.|
|E_POINTER|`nullptr` se proporcionó para *ppvAdapter*.|

## <a name="remarks"></a>Observaciones

Varias llamadas que pasan un índice que representa el mismo adaptador devuelven punteros de interfaz idénticos, incluso en diferentes listas de adaptadores. Como resultado, es seguro comparar punteros de interfaz para determinar si varios punteros hacen referencia al mismo objeto de adaptador.

## <a name="see-also"></a>Consulte también

[IDXCoreAdapterList,](./nn-dxcore_interface-idxcoreadapterlist.md) [referencia de DXCore,](../dxcore-reference.md) [uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)