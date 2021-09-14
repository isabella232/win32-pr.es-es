---
description: El método AppendRecord crea un comando de unidad de datos de protocolo de aplicación (APDU) que anexa un registro al final de un archivo elemental estructurado linealmente (EF) o escribe el número de registro 1 en un archivo elemental estructurado cíclico.
ms.assetid: 4dd88661-41c4-4238-88c9-279b39afb206
title: Método ISCardISO7816::AppendRecord (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.AppendRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 28d1b6762e0a350bb87b673f21fa063ae2478e64
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244317"
---
# <a name="iscardiso7816appendrecord-method"></a>Método ISCardISO7816::AppendRecord

\[El **método AppendRecord** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método AppendRecord** crea un comando de unidad de datos de protocolo de aplicación (APDU) que anexa un registro al final de un archivo elemental estructurado linealmente (EF) o escribe el número de registro 1 en un archivo elemental estructurado cíclico. [](../secgloss/a-gly.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AppendRecord(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*byRefCtrl* \[ En\]
</dt> <dd>

Identifica el archivo elemental que se va a anexar.



| Value                                                                                                                                                                                | Significado                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <dt>**EF actual**</dt> </dl>     | Posición de bits: 00000000<br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <dt>**Id. de EF corto**</dt> </dl> | Posición de bits: xxxxx000<br/> |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <dt>**Reservada**</dt> </dl>             | Posición de bits: xxxxxxxx<br/> |



 

</dd> <dt>

*pData* \[ En\]
</dt> <dd>

Puntero a los datos que se anexarán al archivo.



| Value                                                                                                                                                | Significado                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="Tn"></span><span id="tn"></span><span id="TN"></span><dl> <dt>**Tn**</dt> </dl>     | 1 byte<br/>       |
| <span id="Ln_"></span><span id="ln_"></span><span id="LN_"></span><dl> <dt>**Ln**</dt> </dl> | 1 o 3 bytes<br/> |
| <span id="data"></span><span id="DATA"></span><dl> <dt>**Datos**</dt> </dl>                    | Bytes Ln<br/>     |



 

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En la entrada, puntero a un [**objeto de interfaz ISCardCmd**](iscardcmd.md) o **NULL.**

Al devolverse, se rellena con el comando APDU construido por esta operación. Si *ppCmd* se estableció en **NULL,** [*se*](../secgloss/s-gly.md) crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de tarjeta inteligente y se devuelve mediante el *puntero ppCmd.*

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

El comando encapsulado solo se puede realizar [](../secgloss/s-gly.md) si el estado de seguridad de la tarjeta inteligente satisface los atributos de seguridad del archivo elemental leído.

Si se selecciona otro archivo elemental en el momento de emitir este comando, se puede procesar sin identificar el archivo seleccionado actualmente.

Los archivos elementales sin una estructura de registros no se pueden leer. El comando encapsulado anula si se aplica a un archivo elemental sin una estructura de registros.

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**ReadRecord**](iscardiso7816-readrecord.md)
</dt> <dt>

[**UpdateRecord**](iscardiso7816-updaterecord.md)
</dt> <dt>

[**WriteRecord**](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
