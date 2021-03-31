---
title: DXCoreCreateAdapterFactory
description: Crea un generador de adaptadores de DXCore, que puede usar para generar más objetos DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3f5164578da87af8f4d92c3bedcecb6f3dbaa95e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995508"
---
# <a name="dxcorecreateadapterfactory-function"></a>DXCoreCreateAdapterFactory función)

## <a name="description"></a>Descripción

Crea un generador de adaptadores de DXCore, que puede usar para generar más objetos DXCore. Para obtener instrucciones de programación y ejemplos de código, vea [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md).

## <a name="parameters"></a>Parámetros

### <a name="riid"></a>riid

Tipo: **REFIID**

Referencia al identificador único global (GUID) de la interfaz que desea que se devuelva en *ppvFactory*. Se espera que sea el identificador de interfaz (IID) de [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md).

### <a name="ppvfactory-out"></a>ppvFactory [out]

Tipo: **void \* \***

Dirección de un puntero a una interfaz con el IID especificado en el parámetro *riid* . Cuando la devolución es correcta, *\* ppvFactory* (la dirección desreferenciada) contiene un puntero al generador de DXCore creado.

## <a name="returns"></a>Devoluciones

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la función se ejecuta correctamente, devuelve **S_OK**. De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valor devuelto|Descripción|
|-|-|
|E_NOINTERFACE|Se proporcionó un valor no válido para *riid*.|
|E_POINTER|`nullptr` se proporcionó para *ppvFactory*.|

## <a name="remarks"></a>Observaciones

Durante el tiempo que existe una referencia en una interfaz [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) , una interfaz [IDXCoreAdapterList](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) o una interfaz [IDXCoreAdapter](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) , las llamadas adicionales a **DXCoreCreateAdapterFactory**, [IDXCoreAdapterList:: GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md)o [IDXCoreAdapter:: GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) devolverán punteros al mismo objeto, lo que aumentará el recuento de referencias de la interfaz **IDXCoreAdapterFactory** .

## <a name="see-also"></a>Vea también

[Referencia de DXCore](../dxcore-reference.md), [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md)