---
title: IDXCoreAdapterList::Sort
description: Ordena un objeto de lista de adaptadores DXCore en función de una matriz de entrada proporcionada de criterios de ordenación.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 59580fb8b76c80a264796f829d2b0a1d2e8eabb4375896fbd27fb34a7697cf90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278876"
---
# <a name="idxcoreadapterlistsort-method"></a>IDXCoreAdapterList::Sort (Método)

## <a name="description"></a>Descripción

Ordena un objeto de lista de adaptadores DXCore en función de una matriz de entrada proporcionada de criterios de ordenación, donde los elementos de matriz anteriores en la matriz de criterios reciben un mayor peso. **Ordenar** le ayuda a encontrar más fácilmente el adaptador ideal en una lista de adaptadores.

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

Número de elementos que están en la matriz a la que apunta el parámetro *preferences.*

### <a name="preferences-in"></a>preferencias [in]

Tipo: **const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) \***

Puntero a una matriz constante de [valores DXCoreAdapterPreference,](./ne-dxcore_interface-dxcoreadapterpreference.md) que representan criterios de ordenación.

## <a name="returns"></a>Devoluciones

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la función se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un [**código de**](../../com/structure-of-com-error-codes.md) error [HRESULT](../../com/com-error-codes-10.md).

|Valor devuelto|Descripción|
|-|-|
|E_INVALIDARG|El *argumento numPreferences* es cero o el *argumento preferences* es `nullptr` .|

## <a name="remarks"></a>Comentarios

En los casos en los que el sistema operativo (SO) no reconoce un valor [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) proporcionado, se omite y no se producirá un error en la API. En este caso, se seguirán teniendo en cuenta los valores conocidos de **DXCoreAdapterPreference.** Para determinar si la API entiende un tipo de ordenación, llame a [IDXCoreAdapterList::IsAdapterPreferenceSupported](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).

**Los valores DXCoreAdapterPreference** que se producen anteriormente en la matriz *de* preferencias proporcionada se tratan con mayor prioridad. 

Consulte la documentación **de enumeración DXCoreAdapterPreference** para obtener más información sobre qué lógica se aplica a cada tipo. La lógica interna de un tipo puede desarrollarse a medida que se desarrolla el sistema operativo.

Cuando se devuelve **Sort,** los elementos de la lista de adaptadores DXCore se habrán ordenado de la más preferible a la menos preferible. Por lo tanto, al llamar a [IDXCoreAdapterList::GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) con el índice 0, se recupera el adaptador que mejor se corresponde con los tipos de preferencia de ordenación solicitados; El índice 1 es la siguiente mejor coincidencia, y así sucesivamente.

## <a name="see-also"></a>Consulte también

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [Referencia de DXCore](../dxcore-reference.md), [Uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)