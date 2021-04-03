---
description: Recupera el APDU de respuesta, colocándolo en un búfer de bytes específico.
ms.assetid: ab349e7a-350f-4e72-98b4-4c6431b6e380
title: 'Método ISCardCmd:: get_ApduReply (Scarddat. h)'
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
ms.openlocfilehash: 2ce11ec2d3d8202574ab23074531c393c9fecb98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083434"
---
# <a name="iscardcmdget_apdureply-method"></a>ISCardCmd:: get \_ ApduReply (método)

\[El método **Get \_ ApduReply** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **Get \_ ApduReply** recupera el [*APDU de respuesta*](../secgloss/r-gly.md)y lo coloca en un búfer de bytes específico. La respuesta puede ser **null** si no se ha realizado ninguna [*transacción*](../secgloss/t-gly.md) en el comando APDU.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ApduReply(
  [out] LPBYTEBUFFER *ppReplyApdu
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppReplyApdu* \[ enuncia\]
</dt> <dd>

Puntero al búfer de bytes (asignado a través de un objeto **IStream** ) que contiene el mensaje de respuesta APDU en la devolución.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *ppReplyApdu* no es válido.<br/>  |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido en *ppReplyApdu*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                             |



 

## <a name="remarks"></a>Observaciones

Para determinar la longitud de la respuesta APDU, llame a [**Get \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md).

Para establecer una nueva APDU de respuesta, llame a [**Put \_ ApduReply**](iscardcmd-put-apdureply.md).

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo recuperar los datos de la respuesta. En el ejemplo se da por supuesto que lLe es una variable de tipo **Long** cuyo valor fue establecido por una llamada anterior al método [**ISCardCmd:: get \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md) , que pIByteReply es un puntero válido a una instancia de la interfaz [**IByteBuffer**](ibytebuffer.md) y que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**obtener \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**Put \_ ApduReply**](iscardcmd-put-apdureply.md)
</dt> </dl>

 

 
