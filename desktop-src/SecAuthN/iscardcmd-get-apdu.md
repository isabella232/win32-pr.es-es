---
description: Recupera la unidad de datos de protocolo de aplicación (APDU) sin formato.
ms.assetid: d8b326db-de54-4ef8-becb-fd905414c45c
title: 'Método ISCardCmd:: get_Apdu (Scarddat. h)'
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
ms.openlocfilehash: fb943d7ade48f6684cdc10cb4b1ad7e48f87e65c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082140"
---
# <a name="iscardcmdget_apdu-method"></a>ISCardCmd:: get \_ APDU (método)

\[El método **Get \_ APDU** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **Get \_ APDU** recupera la unidad de [*datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) sin procesar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Apdu(
  [out] LPBYTEBUFFER *ppApdu
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppApdu* \[ enuncia\]
</dt> <dd>

Puntero al búfer de bytes asignado a través de un objeto **IStream** que contiene el mensaje APDU en la devolución.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *ppApdu* no es válido.<br/>  |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido en *ppApdu*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                        |



 

## <a name="remarks"></a>Observaciones

Para copiar las APDU de un objeto [**IByteBuffer**](ibytebuffer.md) (**IStream**) en las APDU ajustadas en este objeto de interfaz, llame a [**Put \_ APDU**](iscardcmd-put-apdu.md).

Para determinar la longitud de las APDU, llame a [**Get \_ ApduLength**](iscardcmd-get-apdulength.md).

Para obtener una lista de todos los métodos proporcionados por la interfaz [**ISCardCmd**](iscardcmd.md) , vea [**ISCardCmd**](iscardcmd.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener información sobre los códigos de error de las tarjetas inteligentes, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo recuperar la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) sin formato (APDU). En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a la interfaz [**ISCardCmd**](iscardcmd.md) y que pIByteApdu es un puntero válido a una instancia de la interfaz [**IByteBuffer**](ibytebuffer.md) .


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

[**obtener \_ ApduLength**](iscardcmd-get-apdulength.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**poner \_ APDU**](iscardcmd-put-apdu.md)
</dt> </dl>

 

 
