---
description: El método UpdateRecord construye un comando de unidad de datos de protocolo de aplicación (APDU) que actualiza un registro específico con los bits dados en el comando APDU.
ms.assetid: 66039afd-5d73-41b3-b87b-b5d598c6f3db
title: Método ISCardISO7816::UpdateRecord (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.UpdateRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bf810594e623d58944f58d3b7671664b3be175f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244263"
---
# <a name="iscardiso7816updaterecord-method"></a>Método ISCardISO7816::UpdateRecord

\[El **método UpdateRecord** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método UpdateRecord** construye un comando [*de*](../secgloss/a-gly.md) unidad de datos de protocolo de aplicación (APDU) que actualiza un registro específico con los bits dados en el comando APDU.

> [!Note]  
> Cuando se usa el direccionamiento de registros actual, el comando establece el puntero de registro en el registro actualizado correctamente.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UpdateRecord(
  [in]      BYTE         byRecordId,
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*byRecordId* \[ En\]
</dt> <dd>

Valor P1:

P1 = 00 designa el registro actual

P1 != '00' es el número del registro especificado

</dd> <dt>

*byRefCtrl* \[ En\]
</dt> <dd>

Codificación del control de referencia P2:



| Value                                                                                                                                                                                                | Significado                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <dt>**EF actual**</dt> </dl>                     | Posición de bits: 00000---<br/> Ef seleccionado actualmente.<br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <dt>**Identificador corto de EF**</dt> </dl>                 | Posición de bits: xxxxx---<br/> Identificador corto de EF.<br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <dt>**Primer registro**</dt> </dl>             | Posición de bits: -----000<br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <dt>**Último registro**</dt> </dl>                 | Posición de bits: -----001<br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <dt>**Siguiente registro**</dt> </dl>                 | Posición del bit: -----010<br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <dt>**Registro anterior**</dt> </dl> | Posición de bits: -----011<br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <dt>**Registro \# en P1**</dt> </dl>    | Posición del bit: -----100<br/>                                   |



 

</dd> <dt>

*pData* \[ En\]
</dt> <dd>

Puntero al registro que se va a actualizar.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **NULL.**

En la devolución, se rellena con el comando APDU construido por esta operación. Si *ppCmd* se estableció en **NULL,** [*se*](../secgloss/s-gly.md) crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de tarjeta inteligente y se devuelve a través del *puntero ppCmd.*

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

El comando encapsulado solo se puede realizar [](../secgloss/s-gly.md) si el estado de seguridad de la tarjeta inteligente satisface los atributos de seguridad del archivo básico que se está procesando.

Cuando el comando contiene un identificador básico corto válido, establece el archivo como archivo básico actual. Si actualmente se selecciona otro archivo básico en el momento de emitir este comando, este comando se puede procesar sin identificar el archivo seleccionado actualmente.

Si el comando construido se aplica a un archivo básico lineal fijo o estructurado cíclico, se anulará si la longitud del registro es diferente de la longitud del registro existente.

Si el comando se aplica a un archivo básico estructurado de variable lineal, se puede llevar a cabo cuando la longitud del registro es diferente de la longitud del registro existente.

La opción "anterior" del comando (P2=xxxxx011), aplicada a un archivo cíclico, tiene el mismo comportamiento que un comando construido por [**AppendRecord**](iscardiso7816-appendrecord.md).

Los archivos elementales sin una estructura de registros no se pueden leer. El comando construido anula si se aplica a un archivo básico sin estructura de registros.

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

[**AppendRecord**](iscardiso7816-appendrecord.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**ReadRecord**](iscardiso7816-readrecord.md)
</dt> <dt>

[**WriteRecord**](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
