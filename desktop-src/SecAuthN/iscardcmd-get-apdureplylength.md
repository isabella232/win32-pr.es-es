---
description: Determina la longitud (en bytes) de la unidad de datos del Protocolo de aplicación (APDU).
ms.assetid: 25011db1-a037-4764-b700-8ad2200419da
title: 'Método ISCardCmd:: get_ApduReplyLength (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduReplyLength
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b62e67154ab48f8378c96a78c8bd54765962c3fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279317"
---
# <a name="iscardcmdget_apdureplylength-method"></a>ISCardCmd:: get \_ ApduReplyLength (método)

\[El método **Get \_ ApduReplyLength** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **Get \_ ApduReplyLength** determina la longitud (en bytes) de la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ApduReplyLength(
  [out] LONG *plSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*plSize* \[ enuncia\]
</dt> <dd>

Puntero al tamaño del mensaje APDU de respuesta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *plSize* no es válido.<br/>  |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido en *plSize*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                        |



 

## <a name="remarks"></a>Observaciones

Para obtener una APDU de respuesta existente, llame a [**Get \_ ApduReply**](iscardcmd-get-apdureply.md).

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo recuperar la longitud de las [*APDU de respuesta*](../secgloss/r-gly.md). En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .


```C++
LONG    lLen;
HRESULT hr;

// Retrieve the APDU reply length.
hr = pISCardCmd->get_ApduReplyLength(&lLen);
if (FAILED(hr))
{
    printf("Failed get_ApduReplyLength\n");
    // Take other error handling action.
}
else
    printf("Length returned is %d\n", lLen);
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

[**obtener \_ ApduReply**](iscardcmd-get-apdureply.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**Put \_ ApduReply**](iscardcmd-put-apdureply.md)
</dt> </dl>

 

 
