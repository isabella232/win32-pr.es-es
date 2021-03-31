---
description: El método PutData crea un comando APDU (unidad de datos de protocolo de aplicación) que almacena un solo objeto de datos primitivos o el conjunto de objetos de datos contenidos en un objeto de datos construido, dependiendo del archivo seleccionado.
ms.assetid: 6bad45fb-b202-4eb0-b2f4-fe0a6af64330
title: ISCardISO7816::P método utData (Scardssp. h)
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
ms.openlocfilehash: 3c15239943a92067011011b6cedca191fa78c3a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911614"
---
# <a name="iscardiso7816putdata-method"></a>ISCardISO7816::P método utData

\[El método **PutData** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **PutData** crea un comando APDU ( [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) ) que almacena un solo objeto de datos primitivos o el conjunto de objetos de datos contenidos en un objeto de datos construido, dependiendo del archivo seleccionado.

El modo en que se almacenan los objetos (al escribir una vez o actualizar o anexar) depende de la definición o de la naturaleza de los objetos de datos.

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

*byP1* \[ de\]
</dt> <dd>

Codificación de P1-P2.



| Value                                                                                  | Significado                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000-003F</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0040-00FF</dt> </dl> | Etiqueta BER-TLV (1 byte) en P2<br/>            |
| <dl> <dt>0100-01FF</dt> </dl> | Datos de aplicación (codificación propietaria)<br/> |
| <dl> <dt>0200-02FF</dt> </dl> | Etiqueta SIMPLE-TLV en P2<br/>                  |
| <dl> <dt>0300-03FF</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | Etiqueta BER-TLV (2 bytes) en P1-P2<br/>        |



 

</dd> <dt>

*byP2* \[ de\]
</dt> <dd>

Codificación de P1-P2.



| Value                                                                                  | Significado                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000-003F</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0040-00FF</dt> </dl> | Etiqueta BER-TLV (1 byte) en P2<br/>            |
| <dl> <dt>0100-01FF</dt> </dl> | Datos de aplicación (codificación propietaria)<br/> |
| <dl> <dt>0200-02FF</dt> </dl> | Etiqueta SIMPLE-TLV en P2<br/>                  |
| <dl> <dt>0300-03FF</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | Etiqueta BER-TLV (2 bytes) en P1-P2<br/>        |



 

</dd> <dt>

*pdata* \[ de\]
</dt> <dd>

Puntero a un búfer de bytes que contiene los parámetros y los datos que se van a escribir.

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

El comando solo se puede realizar si el estado de seguridad satisface las condiciones de seguridad definidas por la aplicación en el [*contexto*](../secgloss/c-gly.md) de la función.

<dl> <dt>

<span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>Almacenar datos de aplicaciones
</dt> <dd>

Cuando el valor de P1-P2 se encuentra en el intervalo de 0100 a 01FF, el valor de P1-P2 será un identificador reservado para las pruebas internas de tarjeta y para los servicios de propiedad significativos en un contexto de aplicación determinado.

</dd> <dt>

<span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>Almacenar objetos de datos
</dt> <dd>

Cuando el valor P1-P2 se encuentra en el intervalo de 0040 a 00FF, el valor de P2 será una etiqueta BER-TLV en un solo byte. El valor de 00FF se reserva para indicar que el campo de datos incluye objetos de datos BER-TLV.

Cuando el valor de P1-P2 se encuentra en el intervalo de 0200 a 02FF, el valor de P2 será una etiqueta SIMPLE-TLV. El valor 0200 es RFU. El valor 02FF se reserva para indicar que el campo de datos incluye objetos de datos simples-TLV.

Cuando el valor de P1-P2 se encuentra en el intervalo de 4000 a FFFF, el valor de P1-P2 será una etiqueta BER-TLV en dos bytes. Los valores 4000 a FFFF son RFU.

Cuando se proporciona un objeto de datos primitivo, el campo de datos del mensaje de comando contendrá el valor del objeto de datos primitivo correspondiente.

Cuando se proporciona un objeto de datos construido, el campo de datos del mensaje de comando contendrá el valor del objeto de datos construido (es decir, los objetos de datos, incluida su etiqueta, longitud y valor).

</dd> </dl>

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

[**GetData**](iscardiso7816-getdata.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
