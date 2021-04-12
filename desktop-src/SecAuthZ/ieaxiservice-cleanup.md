---
description: Libera los recursos utilizados por la interfaz IeAxiService.
ms.assetid: 11f5cfdc-dcdd-4b41-b02c-b19b9452509e
title: 'IeAxiService:: Cleanup (método)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277970"
---
# <a name="ieaxiservicecleanup-method"></a>IeAxiService:: Cleanup (método)

El método **Cleanup** libera los recursos utilizados por la interfaz [**IeAxiService**](ieaxiservice.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Cleanup();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, el método devuelve S \_ correcto.

Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiService se define como E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IeAxiService**](ieaxiservice.md)
</dt> </dl>

 

