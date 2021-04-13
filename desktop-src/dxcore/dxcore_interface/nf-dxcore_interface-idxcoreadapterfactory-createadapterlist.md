---
title: IDXCoreAdapterFactory::CreateAdapterList
description: Genera una lista de objetos de adaptador que representan el estado actual del adaptador del sistema y que cumplen los criterios especificados.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0a35d4dd9a481880d66988b6ade079534d1297c1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488035"
---
# <a name="idxcoreadapterfactorycreateadapterlist-method"></a>IDXCoreAdapterFactory:: CreateAdapterList (método)

Genera una lista de objetos de adaptador que representan el estado actual del adaptador del sistema y que cumplen los criterios especificados. Para obtener instrucciones de programación y ejemplos de código, vea [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintaxis

```cpp
virtual HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapterList) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  _COM_Outptr_ T **ppvAdapterList);
```

## <a name="parameters"></a>Parámetros

### <a name="numattributes"></a>numAttributes

Tipo: **uint32_t**

Número de elementos de la matriz a los que apunta el argumento *filterAttributes* .

### <a name="filterattributes-in"></a>filterAttributes [in]

Tipo: **GUID \* const**

Puntero a una matriz de GUID de atributo de adaptador. Para obtener una lista de los GUID de atributo, consulte [GUID del atributo del adaptador de DXCore](../dxcore-adapter-attribute-guids.md). Se debe proporcionar al menos un GUID. En el caso de que se proporcione más de un GUID en la matriz, solo se incluirán en la lista devuelta los adaptadores que cumplan *todos* los atributos solicitados.

### <a name="riid"></a>riid

Tipo: **REFIID**

Referencia al identificador único global (GUID) de la interfaz que desea que se devuelva en *ppvAdapterList*. Se espera que sea el identificador de interfaz (IID) de [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md).

### <a name="ppvadapterlist-out"></a>ppvAdapterList [out]

Tipo: **void \* \***

Dirección de un puntero a una interfaz con el IID especificado en el parámetro *riid* . Si la devolución es correcta, *\* ppvAdapterList* (la dirección desreferenciada) contiene un puntero a la lista de adaptadores creada.

## <a name="returns"></a>Devoluciones

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la función se ejecuta correctamente, devuelve **S_OK**. De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valor devuelto|Descripción|
|-|-|
|E_INVALIDARG|`nullptr` se proporcionó para *filterAttributes* o se proporcionó 0 para *numAttributes*.|
|E_NOINTERFACE|Se proporcionó un valor no válido para *riid*.|
|E_POINTER|`nullptr` se proporcionó para *ppvAdapterList*.|

## <a name="remarks"></a>Observaciones

Aunque no se encuentre ningún adaptador, siempre y cuando los argumentos sean válidos, **CreateAdapterList** crea un objeto [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) válido y devuelve **S_OK**. Una vez generados, los adaptadores de esta lista específica no cambiarán. Pero la lista se considerará obsoleta si uno de los adaptadores deja de ser válido, o si llega un nuevo adaptador que cumpla los criterios de filtro proporcionados. La lista devuelta por **CreateAdapterList** no se ordena de ninguna manera determinada, pero el orden de una lista es coherente entre varias llamadas e incluso entre reinicios del sistema operativo. El orden puede variar tras los cambios de configuración del sistema, incluida la adición o eliminación de un adaptador, o la actualización de un controlador en un adaptador existente. Puede registrarse para estos cambios con [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) mediante el tipo de notificación **DXCoreNotificationType. AdapterListStale**.

## <a name="see-also"></a>Vea también

[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [DXCore GUID Attribute GUID](../dxcore-adapter-attribute-guids.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)