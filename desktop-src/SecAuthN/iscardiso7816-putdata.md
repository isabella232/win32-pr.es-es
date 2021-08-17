---
description: El método PutData construye un comando de unidad de datos de protocolo de aplicación (APDU) que almacena un único objeto de datos primitivo o el conjunto de objetos de datos contenidos en un objeto de datos construido, en función del archivo seleccionado.
ms.assetid: 6bad45fb-b202-4eb0-b2f4-fe0a6af64330
title: Método ISCardISO7816::P utData (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.PutData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 66698db3c15223071167441fc37437bfa299baa100c58943a41cb4d774a8e17c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141118"
---
# <a name="iscardiso7816putdata-method"></a>Método ISCardISO7816::P utData

\[El **método PutData** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método PutData** construye un comando de unidad de datos de protocolo de aplicación (APDU) que almacena un único objeto de datos primitivo o el conjunto de objetos de datos contenidos en un objeto de datos construido, en función del archivo seleccionado. [](../secgloss/a-gly.md)

La forma en que se almacenan los objetos (escribir una vez o actualizar o anexar) depende de la definición o la naturaleza de los objetos de datos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PutData(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*byP1* \[ En\]
</dt> <dd>

Codificación de P1-P2.



| Value                                                                                  | Significado                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000 - 003F</dt> </dl> | Rfu<br/>                                   |
| <dl> <dt>0040 - 00FF</dt> </dl> | Etiqueta BER-TLV (1 byte) en P2<br/>            |
| <dl> <dt>0100 - 01FF</dt> </dl> | Datos de la aplicación (codificación propietaria)<br/> |
| <dl> <dt>0200 - 02FF</dt> </dl> | Etiqueta SIMPLE-TLV en P2<br/>                  |
| <dl> <dt>0300 - 03FF</dt> </dl> | Rfu<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | Etiqueta BER-TLV (2 bytes) en P1-P2<br/>        |



 

</dd> <dt>

*byP2* \[ En\]
</dt> <dd>

Codificación de P1-P2.



| Value                                                                                  | Significado                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000 - 003F</dt> </dl> | Rfu<br/>                                   |
| <dl> <dt>0040 - 00FF</dt> </dl> | Etiqueta BER-TLV (1 byte) en P2<br/>            |
| <dl> <dt>0100 - 01FF</dt> </dl> | Datos de la aplicación (codificación propietaria)<br/> |
| <dl> <dt>0200 - 02FF</dt> </dl> | Etiqueta SIMPLE-TLV en P2<br/>                  |
| <dl> <dt>0300 - 03FF</dt> </dl> | Rfu<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | Etiqueta BER-TLV (2 bytes) en P1-P2<br/>        |



 

</dd> <dt>

*pData* \[ En\]
</dt> <dd>

Puntero a un búfer de bytes que contiene los parámetros y los datos que se escribirán.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En la entrada, puntero a un [**objeto de interfaz ISCardCmd**](iscardcmd.md) o **NULL.**

Al devolverse, se rellena con el comando APDU construido por esta operación. Si *ppCmd se* estableció en **NULL,** [*se*](../secgloss/s-gly.md) crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de tarjeta inteligente y se devuelve mediante el *puntero ppCmd.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Se pasó un puntero no válido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                    |



 

## <a name="remarks"></a>Comentarios

El comando solo se puede realizar si el estado de seguridad cumple las condiciones de seguridad definidas por la aplicación en el [*contexto*](../secgloss/c-gly.md) de la función.

<dl> <dt>

<span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>Almacenamiento de datos de aplicación
</dt> <dd>

Cuando el valor de P1-P2 se encuentra en el intervalo de 0100 a 01FF, el valor de P1-P2 debe ser un identificador reservado para las pruebas internas de tarjeta y para los servicios propietarios significativos dentro de un contexto de aplicación determinado.

</dd> <dt>

<span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>Almacenar objetos de datos
</dt> <dd>

Cuando el valor P1-P2 se encuentra en el intervalo de 0040 a 00FF, el valor de P2 debe ser una etiqueta BER-TLV en un solo byte. El valor de 00FF se reserva para indicar que el campo de datos lleva objetos de datos BER-TLV.

Cuando el valor de P1-P2 se encuentra en el intervalo de 0200 a 02FF, el valor de P2 debe ser una etiqueta SIMPLE-TLV. El valor 0200 es RFU. El valor 02FF está reservado para indicar que el campo de datos contiene objetos de datos SIMPLE-TLV.

Cuando el valor de P1-P2 se encuentra en el intervalo de 4000 a FFFF, el valor de P1-P2 debe ser una etiqueta BER-TLV en dos bytes. Los valores de 4000 a FFFF son RFU.

Cuando se proporciona un objeto de datos primitivo, el campo de datos del mensaje de comando debe contener el valor del objeto de datos primitivo correspondiente.

Cuando se proporciona un objeto de datos construido, el campo de datos del mensaje de comando debe contener el valor del objeto de datos construido (es decir, los objetos de datos incluidos su etiqueta, longitud y valor).

</dd> </dl>

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetData**](iscardiso7816-getdata.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
