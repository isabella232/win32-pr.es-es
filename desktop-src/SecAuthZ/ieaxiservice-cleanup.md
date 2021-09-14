---
description: Libera los recursos usados por la interfaz IeAxiService.
ms.assetid: 11f5cfdc-dcdd-4b41-b02c-b19b9452509e
title: IeAxiService::Cleanup (Método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Cleanup
api_type:
- COM
api_location: ''
ms.openlocfilehash: b29784ae360ec78b9f7e01d2045617615333a5c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073692"
---
# <a name="ieaxiservicecleanup-method"></a>IeAxiService::Cleanup (Método)

El **método Cleanup** libera los recursos usados por la interfaz [**IeAxiService.**](ieaxiservice.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Cleanup();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el método devuelve S \_ OK.

Si se produce un error en el método, devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Business, Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista \[ Ultimate\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                 |
| IID<br/>                      | IID IeAxiService se define como \_ E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IeAxiService**](ieaxiservice.md)
</dt> </dl>

 

