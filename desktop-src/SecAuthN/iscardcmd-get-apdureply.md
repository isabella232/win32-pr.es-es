---
description: Recupera la APDU de respuesta y la coloca en un búfer de bytes específico.
ms.assetid: ab349e7a-350f-4e72-98b4-4c6431b6e380
title: Método ISCardCmd::get_ApduReply (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b5732d956e28c89ef3fba6d5beeea7077468c9e9154a48e4ffb327a36280d11f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015065"
---
# <a name="iscardcmdget_apdureply-method"></a>Método ISCardCmd::get \_ ApduReply

\[El **método \_ get ApduReply** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método \_ get ApduReply** recupera la [*APDU*](../secgloss/r-gly.md)de respuesta y la coloca en un búfer de bytes específico. La respuesta puede ser **NULL si** no [*se ha*](../secgloss/t-gly.md) realizado ninguna transacción en el comando APDU.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ApduReply(
  [out] LPBYTEBUFFER *ppReplyApdu
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppReplyApdu* \[ out\]
</dt> <dd>

Puntero al búfer de bytes (asignado a través de un **objeto IStream)** que contiene el mensaje de respuesta apdu en la devolución.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro ppReplyApdu* no es válido.<br/>  |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Se pasó un puntero no válido *en ppReplyApdu.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                             |



 

## <a name="remarks"></a>Comentarios

Para determinar la longitud de la respuesta de APDU, llame [**a get \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md).

Para establecer una nueva APDU de respuesta, llame a [**put \_ ApduReply**](iscardcmd-put-apdureply.md).

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de [*error*](../secgloss/s-gly.md) de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo recuperar datos de respuesta. En el ejemplo se supone que lLe es una variable de tipo **LONG** cuyo valor se estableció mediante una llamada anterior al método [**ISCardCmd::get \_ ApduReplyLength,**](iscardcmd-get-apdureplylength.md) que pIByteReply es un puntero válido a una instancia de la interfaz [**IByteBuffer**](ibytebuffer.md) y que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd.**](iscardcmd.md)


```C++
HRESULT      hr;

if (lLe > 0)
{
    // Get reply data if available.
    hr = pISCardCmd->get_ApduReply(&pIByteReply);
    if (FAILED(hr)) 
    {
        printf("Failed ISCardCmd::get_ApduReply.\n");
        // Take other error handling action as needed.
    }
    else
    {
        BYTE byReplyBytes[256];
        LONG lBytesRead;

        hr = pIByteReply->Read(byReplyBytes, lLe, &lBytesRead);
        if (FAILED(hr))
        {
            printf("Failed IByteBuffer::Read.\n");
            // Take other error handling action as needed.
        }
        // Use the bytes in byReplyBytes as needed.
    }
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardCmd se define como \_ D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**get \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ ApduReply**](iscardcmd-put-apdureply.md)
</dt> </dl>

 

 
