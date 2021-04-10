---
title: IDXCoreAdapterList::Sort
description: Ordena un objeto de lista de adaptadores de DXCore basándose en una matriz de entrada proporcionada de criterios de ordenación.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 6260e700053a99b531a66a5c19e15d4a32f07e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149551"
---
# <a name="idxcoreadapterlistsort-method"></a>IDXCoreAdapterList:: sort (método)

## <a name="description"></a>Descripción

Ordena un objeto de lista de adaptadores de DXCore basándose en una matriz de entrada proporcionada de criterios de ordenación, donde los elementos de matriz situados antes en la matriz de criterios tienen un peso superior. La **ordenación** le ayuda a encontrar más fácilmente el adaptador ideal en una lista de adaptadores.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT Sort(
  uint32_t numPreferences,
  _In_reads_(numPreferences) const DXCoreAdapterPreference* preferences
);
```

## <a name="parameters"></a>Parámetros

### <a name="numpreferences"></a>numPreferences

Tipo: **uint32_t**

Número de elementos que se encuentran en la matriz a la que apunta el parámetro *Preferences* .

### <a name="preferences-in"></a>preferencias [in]

Tipo: **const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) \***

Puntero a una matriz constante de valores de [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) , que representa los criterios de ordenación.

## <a name="returns"></a>Devoluciones

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la función se ejecuta correctamente, devuelve **S_OK**. De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valor devuelto|Descripción|
|-|-|
|E_INVALIDARG|El argumento *numPreferences* es cero o el argumento *Preferences* es `nullptr` .|

## <a name="remarks"></a>Observaciones

En los casos en los que el sistema operativo (SO) no reconoce un valor de [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) proporcionado, se omite y no se produce un error en la API. Los valores de **DXCoreAdapterPreference** conocidos se seguirán considerando en este caso. Para determinar si la API comprende un tipo de ordenación, llame a [IDXCoreAdapterList:: IsAdapterPreferenceSupported](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).

Los valores de **DXCoreAdapterPreference** que se producen antes en la matriz de *preferencias* proporcionada se tratan con mayor prioridad. 

Consulte la documentación de la enumeración **DXCoreAdapterPreference** para obtener más información sobre la lógica que se aplica a cada tipo. La lógica interna de un tipo puede desarrollar a medida que el sistema operativo desarrolla.

Cuando se devuelva el **orden** , los elementos de la lista de adaptadores de DXCore se ordenarán de la más preferible a la menos preferible. Por lo tanto, al llamar a [IDXCoreAdapterList:: GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) con el índice 0 se recupera el adaptador que mejor coincida con los tipos de preferencia de ordenación solicitados. el índice 1 es la siguiente mejor coincidencia, y así sucesivamente.

## <a name="see-also"></a>Vea también

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)