---
description: Copia la unidad de datos de protocolo de aplicación (APDU) del objeto IByteBuffer (IStream) en las APDU ajustadas en este objeto de interfaz.
ms.assetid: 28dac222-ee7a-40aa-903b-e9c0b7757c9c
title: 'ISCardCmd: método de ut_Apdu de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ee615e7f2e8d7555cfed276658e8de1a97ddf73a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001161"
---
# <a name="iscardcmdput_apdu-method"></a>ISCardCmd: \_ método Apdu:p UT

\[El método **Put \_ APDU** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método put \_ APDU** copia la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) del objeto [**IBYTEBUFFER**](ibytebuffer.md) (**IStream**) en las APDU ajustadas en este objeto de interfaz.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Apdu(
  [in] LPBYTEBUFFER pApdu
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pApdu* \[ de\]
</dt> <dd>

Puntero a la APDU ISO 7816-4 en la que se va a copiar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *pApdu* no es válido.<br/>  |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido en *pApdu*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                       |



 

## <a name="remarks"></a>Observaciones

Para recuperar las APDU sin formato del búfer de bytes asignado a través de una **IStream** que contiene el mensaje APDU, llame a [**Get \_ APDU**](iscardcmd-get-apdu.md).

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo copiar un APDU de un objeto [**IByteBuffer**](ibytebuffer.md) (**IStream**) en las APDU contenidas en un objeto de interfaz. En el ejemplo se da por supuesto que pIByteApdu es un puntero válido a una instancia de **IByteBuffer** y que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .


```C++
HRESULT    hr;


// Set the APDU.
hr = pISCardCmd->put_Apdu(pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed put_Apdu.\n");
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

[**obtener \_ APDU**](iscardcmd-get-apdu.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
