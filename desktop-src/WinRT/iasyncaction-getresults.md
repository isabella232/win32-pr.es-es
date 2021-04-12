---
description: Obtiene el resultado de una acción asincrónica.
ms.assetid: E5AF357D-B1EE-4581-AEBC-6F1C89D7DBB0
title: 'IAsyncAction:: GetResults (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.GetResults
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 292c73846227f1bb8884b24b7e709bc6b2296e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275413"
---
# <a name="iasyncactiongetresults-method"></a>IAsyncAction:: GetResults (método)

Obtiene el resultado de una acción asincrónica.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetResults();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Este método siempre devuelve **S \_ correcto**.

## <a name="remarks"></a>Observaciones

La llamada al método **GetResults** no tiene ningún efecto si la implementación actual tiene un tipo dinámico de [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                    |
| Encabezado<br/>                   | <dl> <dt>Windows. Foundation. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
