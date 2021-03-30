---
description: El método ReadRecord crea un comando de unidad de datos de protocolo de aplicación (APDU) que lee el contenido de los registros especificados o la parte inicial de un registro de un archivo elemental.
ms.assetid: b00a3242-93bc-4779-8c62-89157fbcb5d1
title: 'ISCardISO7816:: ReadRecord (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0cb9697315a6f9dd2436cd7a64d54fa6b44e00f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082614"
---
# <a name="iscardiso7816readrecord-method"></a>ISCardISO7816:: ReadRecord (método)

\[El método **ReadRecord** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **ReadRecord** crea un comando de [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) que lee el contenido de los registros especificados o la parte inicial de un registro de un archivo elemental.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReadRecord(
  [in]      BYTE       byRecordId,
  [in]      BYTE       byRefCtrl,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*byRecordId* \[ de\]
</dt> <dd>

Número de registro o identificador del primer registro que se va a leer (00 indica el registro actual).

</dd> <dt>

*byRefCtrl* \[ de\]
</dt> <dd>

Codificación del control de referencia.



| Value                                                                                                                                                                                | Significado                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <dt>**EF actual**</dt> </dl>     | Posición de bit: 00000---<br/> EF actualmente seleccionado.<br/>                    |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <dt>**Short EF ID**</dt> </dl> | Posición de bit: xxxxx---<br/> Identificador de EF corto.<br/>                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                       | Posición de bit: 11111---<br/>                                                      |
| <span id="Record__"></span><span id="record__"></span><span id="RECORD__"></span><dl> <dt>**Record \#**</dt> </dl>            | Posición de bit:-----1xx<br/> Uso del número de registro en P1.<br/>             |
| <span id="Read_Record"></span><span id="read_record"></span><span id="READ_RECORD"></span><dl> <dt>**Leer registro**</dt> </dl> | Posición de bit:-----100<br/> Lea el registro P1.<br/>                           |
| <span id="Up_to_Last"></span><span id="up_to_last"></span><span id="UP_TO_LAST"></span><dl> <dt>**Hasta el último**</dt> </dl>     | Posición de bit:-----101<br/> Lea todos los registros de P1 hasta el último. <br/> |
| <span id="Up_to_P1"></span><span id="up_to_p1"></span><span id="UP_TO_P1"></span><dl> <dt>**Hasta P1**</dt> </dl>             | Posición de bit:-----110<br/> Lea todos los registros del último hasta el P1. <br/> |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                       | Posición de bit:-----111<br/>                                                      |
| <span id="Record_ID"></span><span id="record_id"></span><span id="RECORD_ID"></span><dl> <dt>**Record ID**</dt> </dl>         | Posición de bit:-----0xx<br/> Uso del número de registro en P1.<br/>             |
| <span id="First_Occur"></span><span id="first_occur"></span><span id="FIRST_OCCUR"></span><dl> <dt>**Primera vez**</dt> </dl> | Posición de bit:-----000<br/> Lea la primera aparición. <br/>                   |
| <span id="Last_Occur"></span><span id="last_occur"></span><span id="LAST_OCCUR"></span><dl> <dt>**Última vez**</dt> </dl>     | Posición de bit:-----001<br/> Leer la última aparición. <br/>                    |
| <span id="Next_Occur"></span><span id="next_occur"></span><span id="NEXT_OCCUR"></span><dl> <dt>**Siguiente sucede**</dt> </dl>     | Posición de bit:-----010<br/> Lea la siguiente repetición. <br/>                    |
| <span id="Previous"></span><span id="previous"></span><span id="PREVIOUS"></span><dl> <dt>**Anterior**</dt> </dl>             | Posición de bit:-----011<br/> Lee la repetición anterior. <br/>                |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**Secreto**</dt> </dl>                     | Posición de bit:---xxxxx<br/>                                                      |



 

</dd> <dt>

*lBytesToRead* \[ de\]
</dt> <dd>

Número de bytes que se van a leer del EF transparente.

Si el campo le contiene solo ceros, dependiendo de b3b2b1 de P2 y dentro del límite de 256 para la longitud corta o 65536 para la longitud extendida, el comando debe leer por completo el registro solicitado único o la secuencia de registros solicitada.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.

En la devolución, se rellena con el comando APDU construido por esta operación. Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                    |



 

## <a name="remarks"></a>Observaciones

El comando encapsulado solo puede realizarse si el estado de seguridad de la [*tarjeta inteligente*](../secgloss/s-gly.md) cumple los atributos de seguridad del archivo elemental que se está leyendo.

Si hay otro archivo elemental seleccionado actualmente en el momento de emitir este comando, se puede procesar sin identificación del archivo seleccionado actualmente.

Cuando el comando contiene un identificador elemental básico válido, establece el archivo como archivo elemental actual.

No se pueden leer los archivos elementales sin una estructura de registro. El comando encapsulado se anula si se aplica a un archivo elemental sin una estructura de registro.

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AppendRecord**](iscardiso7816-appendrecord.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**UpdateRecord**](iscardiso7816-updaterecord.md)
</dt> <dt>

[**WriteRecord**](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
