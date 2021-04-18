---
description: Ejecuta una operación de escritura y lectura en el objeto de comando de tarjeta inteligente (unidad de datos de protocolo de aplicación).
ms.assetid: 4dc8ed56-97e0-4c05-a70a-ea2ffd976d47
title: 'ISCard:: Transaction (método) (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Transaction
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2abe9d4acd4d59019fe0c8ce122baa12fde06f2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652517"
---
# <a name="iscardtransaction-method"></a>ISCard:: Transaction (método)

\[El método de **transacción** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método de **transacción** ejecuta una operación de lectura y escritura en el objeto de comando de [*tarjeta inteligente*](../secgloss/s-gly.md) ([*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md)). La cadena de respuesta de la tarjeta inteligente para la cadena de comando definida en la tarjeta que se envió a la tarjeta inteligente será accesible después de que se devuelva esta función.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Transaction(
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

Puntero al objeto de comando de tarjeta inteligente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | La operación se ha completado correctamente.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *ppCmd* no es válido.<br/>           |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido en *ppCmd*.<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | La memoria para satisfacer la solicitud no está disponible.<br/> |



 

## <a name="remarks"></a>Observaciones

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra la ejecución de una operación de escritura y lectura en el objeto de comando de tarjeta inteligente.


```C++
HRESULT    hr;

// pISCard is a pointer to an instance of ISCard.
// pISCardCmd is a pointer to an instance of ISCardCmd,
// and ISCardCmd::BuildCmd has already been called.
hr = pISCard->Transaction(&pISCardCmd);
if (FAILED(hr))
{
    printf("Failed ISCard::Transaction\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCard se define como 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AttachByHandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**AttachByReader**](iscard-attachbyreader.md)
</dt> <dt>

[**Conecta**](iscard-detach.md)
</dt> <dt>

[**obtener \_ ATR**](iscard-get-atr.md)
</dt> <dt>

[**obtener \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**obtener \_ contexto**](iscard-get-context.md)
</dt> <dt>

[**obtener \_ Protocolo**](iscard-get-protocol.md)
</dt> <dt>

[**obtener \_ Estado**](iscard-get-status.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**LockSCard**](iscard-lockscard.md)
</dt> <dt>

[**Volver a adjuntar**](iscard-reattach.md)
</dt> <dt>

[**UnlockSCard**](iscard-unlockscard.md)
</dt> </dl>

 

 
