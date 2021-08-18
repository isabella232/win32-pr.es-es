---
description: Recupera la unidad de datos del protocolo de aplicación (APDU) sin procesar.
ms.assetid: d8b326db-de54-4ef8-becb-fd905414c45c
title: Método ISCardCmd::get_Apdu (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 773185563db798877d38d3fb877fe1b4459468e4eeb4d45aed922203bd813418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015095"
---
# <a name="iscardcmdget_apdu-method"></a>Método ISCardCmd::get \_ Apdu

\[El **método \_ get Apdu** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método get \_ Apdu** recupera la unidad de datos del protocolo de aplicación (APDU) sin [*procesar.*](../secgloss/a-gly.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Apdu(
  [out] LPBYTEBUFFER *ppApdu
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppApdu* \[ out\]
</dt> <dd>

Puntero al búfer de bytes asignado a través de **un objeto IStream** que contiene el mensaje APDU en la devolución.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro ppApdu* no es válido.<br/>  |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Se pasó un puntero no válido *en ppApdu*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                        |



 

## <a name="remarks"></a>Comentarios

Para copiar la APDU de un [**objeto IByteBuffer**](ibytebuffer.md) **(IStream)** en la APDU encapsulada en este objeto de interfaz, llame a [**put \_ Apdu**](iscardcmd-put-apdu.md).

Para determinar la longitud de la APDU, llame [**a get \_ ApduLength**](iscardcmd-get-apdulength.md).

Para obtener una lista de todos los métodos proporcionados por la [**interfaz ISCardCmd,**](iscardcmd.md) vea [**ISCardCmd**](iscardcmd.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de [*error*](../secgloss/s-gly.md) de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener información sobre los códigos de error de tarjeta inteligente, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo recuperar la unidad de datos del protocolo de aplicación (APDU) sin [*procesar.*](../secgloss/a-gly.md) En el ejemplo se supone que pISCardCmd es un puntero válido a la interfaz [**ISCardCmd**](iscardcmd.md) y que pIByteApdu es un puntero válido a una instancia de la interfaz [**IByteBuffer.**](ibytebuffer.md)


```C++
HRESULT    hr;

hr = pISCardCmd->get_Apdu(&pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed get_Apdu.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardCmd se define como \_ D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**get \_ ApduLength**](iscardcmd-get-apdulength.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ Apdu**](iscardcmd-put-apdu.md)
</dt> </dl>

 

 
