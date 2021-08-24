---
description: El método LockSCard reclama acceso exclusivo a la tarjeta inteligente.
ms.assetid: 70af7c5a-ebe7-48ee-8a76-dfea7f73f45e
title: Método ISCard::LockSCard (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.LockSCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bdb9e531013836bb193719faa7bcd9d73581e83a3599bd51439be27c44ba1e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482175"
---
# <a name="iscardlockscard-method"></a>Método ISCard::LockSCard

\[El **método LockSCard** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método LockSCard reclama** acceso exclusivo a la tarjeta [*inteligente.*](../secgloss/s-gly.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LockSCard();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                          | Descripción                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Operación completada correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Además del código de error COM enumerado anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

Para desbloquear la tarjeta inteligente, llame al [**método ISCard::UnlockSCard.**](iscard-unlockscard.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo adquirir acceso exclusivo a la tarjeta inteligente.


```C++
HRESULT    hr;

// Lock the smart card.
hr = pISCard->LockSCard();
if (FAILED(hr))
{
    printf("Failed LockSCard\n");
    // Take error handling action as needed.
}
// Use smart card; unlock the smart card when done.
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCard se define como \_ 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**UnlockSCard**](iscard-unlockscard.md)
</dt> </dl>

 

 
