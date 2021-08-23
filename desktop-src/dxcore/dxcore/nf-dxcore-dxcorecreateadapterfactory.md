---
title: DXCoreCreateAdapterFactory
description: Crea un generador de adaptadores DXCore, que puede usar para generar más objetos DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 90567d732f6febc5d95b460b2ff88929dd12b2f22275de9db0d6bc5f88ef99ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985185"
---
# <a name="dxcorecreateadapterfactory-function"></a>Función DXCoreCreateAdapterFactory

## <a name="description"></a>Descripción

Crea un generador de adaptadores DXCore, que puede usar para generar más objetos DXCore. Para obtener instrucciones de programación y ejemplos de código, [vea Uso de DXCore para enumerar adaptadores.](../dxcore-enum-adapters.md)

## <a name="parameters"></a>Parámetros

### <a name="riid"></a>riid

Tipo: **REFIID**

Referencia al identificador único global (GUID) de la interfaz que desea que se devuelva en *ppvFactory.* Se espera que sea el identificador de interfaz (IID) de [IDXCoreAdapterFactory.](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md)

### <a name="ppvfactory-out"></a>ppvFactory [out]

Tipo: **\* \* void**

Dirección de un puntero a una interfaz con el IID especificado en el *parámetro riid.* Tras la devolución correcta, *\* ppvFactory* (la dirección desreferenciada) contiene un puntero al generador de DXCore creado.

## <a name="returns"></a>Devoluciones

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la función se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un [**código de**](../../com/structure-of-com-error-codes.md) error [HRESULT](../../com/com-error-codes-10.md).

|Valor devuelto|Descripción|
|-|-|
|E_NOINTERFACE|Se proporcionó un valor no válido para *riid*.|
|E_POINTER|`nullptr`se proporcionó para *ppvFactory.*|

## <a name="remarks"></a>Comentarios

Durante el tiempo que existe una referencia en una interfaz [IDXCoreAdapterFactory,](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) una interfaz [IDXCoreAdapterList](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) o una [interfaz IDXCoreAdapter,](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) las llamadas adicionales a **DXCoreCreateAdapterFactory**, [IDXCoreAdapterList::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md)o [IDXCoreAdapter::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) devolverán punteros al mismo objeto, lo que aumenta el recuento de referencias de la interfaz **IDXCoreAdapterFactory.**

## <a name="see-also"></a>Vea también

[Referencia de DXCore,](../dxcore-reference.md) [uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)