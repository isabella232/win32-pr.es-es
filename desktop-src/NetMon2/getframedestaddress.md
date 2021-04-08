---
description: Recupera la dirección de destino de un marco.
ms.assetid: f19a6753-37d8-4ec7-a7d4-ced0292d453c
title: Función GetFrameDestAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: afec32f0e0fc66ccd5a1d78cc9769b0e742f1e6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000935"
---
# <a name="getframedestaddress-function"></a>GetFrameDestAddress función)

La función **GetFrameDestAddress** recupera la dirección de destino de un marco.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI GetFrameDestAddress(
   HFRAME    hFrame,
   LPADDRESS lpAddress,
   DWORD     AddressType,
   DWORD     Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* 
</dt> <dd>

Identificador del marco al que se va a obtener un puntero.

</dd> <dt>

*lpAddress* 
</dt> <dd>

Búfer de retorno que almacena la dirección de destino del marco.

</dd> <dt>

*AddressType* 
</dt> <dd>

Un tipo de dirección, como el tipo de dirección \_ \_ Ethernet o el tipo de dirección \_ \_ IP.

</dd> <dt>

*Marcas* 
</dt> <dd>

Marcas usadas para modificar los datos devueltos de la dirección de destino.



| Value                                                                                                                                                                                                           | Significado                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <dt>**marcas de ADDRESSTYPE ( \_ \_ normalizar)**</dt> </dl>        | Cancela los BITs de enrutamiento y grupo.<br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <dt>**BIT de las \_ marcas ADDRESSTYPE \_ \_ inverso**</dt> </dl> | Vuelve a convertir las direcciones de red de token ring en normal.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, el valor de *lpAddress* es válido y el valor devuelto es BHERR \_ Success.

Si la función no es correcta, el valor devuelto es un código de error.



| Código devuelto                                                                                                | Descripción                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ \_ no \_ se encontró el protocolo BHERR**</dt> </dl> | El protocolo especificado en el parámetro *AddressType* no es válido para el marco.<br/> |
| <dl> <dt>**BHERR \_ no válido \_ HFRAME**</dt> </dl>      | El valor de *hFrame* no es válido.<br/>                                                  |



 

## <a name="remarks"></a>Observaciones

Se permite el tipo de dirección buscar el tipo de dirección **\_ \_ \_ más alto** . Cuando se usa este tipo de dirección, la función busca la dirección IP de IPX, XNS, IP o VINEs antes de devolver la dirección ETHERNET, TOKENRING o FDDI. Este enfoque es útil para los protocolos y en entornos en los que se pueden multiplexar dos NIC en una sola dirección de servidor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




