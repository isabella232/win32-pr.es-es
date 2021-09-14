---
description: El método GetData construye un comando de unidad de datos de protocolo de aplicación (APDU) que recupera un único objeto de datos primitivo o un conjunto de objetos de datos (contenidos en un objeto de datos construido), en función del tipo de archivo seleccionado.
ms.assetid: d764a765-f451-4bf7-9d06-f5901062dcac
title: Método ISCardISO7816::GetData (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 93dca04daa50e068a68dc62cf11a580eb8e3b1c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244299"
---
# <a name="iscardiso7816getdata-method"></a>Método ISCardISO7816::GetData

\[El **método GetData** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método GetData** construye un comando de unidad de datos de protocolo de aplicación (APDU) que recupera un único objeto de datos primitivo o un conjunto de objetos de datos (contenidos en un objeto de datos construido), en función del tipo de archivo seleccionado. [](../secgloss/a-gly.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetData(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToGet,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*byP1* \[ En\]
</dt> <dd>

Parámetros.



| Value                                                                                  | Significado                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000 - 003F</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0040 - 00FF</dt> </dl> | Etiqueta BER-TLV (1 byte) en P2<br/>            |
| <dl> <dt>0100 - 01FF</dt> </dl> | Datos de la aplicación (codificación propietaria)<br/> |
| <dl> <dt>0200 - 02FF</dt> </dl> | Etiqueta SIMPLE-TLV en P2<br/>                  |
| <dl> <dt>0300 - 03FF</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | Etiqueta BER-TLV (2 bytes) en P1-P2<br/>        |



 

</dd> <dt>

*byP2* \[ En\]
</dt> <dd>

Parámetros.



| Value                                                                                  | Significado                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000 - 003F</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0040 - 00FF</dt> </dl> | Etiqueta BER-TLV (1 byte) en P2<br/>            |
| <dl> <dt>0100 - 01FF</dt> </dl> | Datos de la aplicación (codificación propietaria)<br/> |
| <dl> <dt>0200 - 02FF</dt> </dl> | Etiqueta SIMPLE-TLV en P2<br/>                  |
| <dl> <dt>0300 - 03FF</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | Etiqueta BER-TLV (2 bytes) en P1-P2<br/>        |



 

</dd> <dt>

*lBytesToGet* \[ En\]
</dt> <dd>

Número de bytes esperados en la respuesta.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **NULL.**

En la devolución, se rellena con el comando APDU construido por esta operación. Si *ppCmd se* estableció en **NULL,** [*se*](../secgloss/s-gly.md) crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de tarjeta inteligente y se devuelve mediante el *puntero ppCmd.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Se pasó un puntero no válido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                    |



 

## <a name="remarks"></a>Observaciones

El comando encapsulado solo se puede realizar [](../secgloss/s-gly.md) si el estado de seguridad de la tarjeta inteligente satisface los atributos de seguridad del archivo básico que se está leyendo. Las condiciones de seguridad dependen de la directiva de la tarjeta y se pueden manipular a través de [**ExternalAuthenticate,**](iscardiso7816-externalauthenticate.md) [**InternalAuthenticate,**](iscardiso7816-internalauthenticate.md) [**ISCardAuth,**](iscardauth.md)y así sucesivamente.

Para seleccionar un archivo, llame a [**SelectFile**](iscardiso7816-selectfile.md).

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[**InternalAuthenticate**](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[**ISCardAuth**](iscardauth.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**PutData**](iscardiso7816-putdata.md)
</dt> <dt>

[**SelectFile**](iscardiso7816-selectfile.md)
</dt> </dl>

 

 
