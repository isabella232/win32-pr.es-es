---
description: Recupera la dirección de origen de un marco.
ms.assetid: 414f9e64-f1b2-46f1-822e-0fffacfad843
title: Función GetFrameSourceAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6939e5875c4d2f6f41ae33574c7a7240697042ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686570"
---
# <a name="getframesourceaddress-function"></a>GetFrameSourceAddress función)

La función **GetFrameSourceAddress** recupera la dirección de origen de un marco.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI GetFrameSourceAddress(
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

Identificador del marco para el que se va a obtener un puntero.

</dd> <dt>

*lpAddress* 
</dt> <dd>

Búfer de retorno que almacena la dirección de origen del marco.

</dd> <dt>

*AddressType* 
</dt> <dd>

El tipo de dirección que se busca, como el tipo de dirección \_ \_ Ethernet o el tipo de dirección \_ \_ IP.

</dd> <dt>

*Marcas* 
</dt> <dd>

Marcas usadas para modificar los datos de dirección de origen devueltos.



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
| <dl> <dt>**\_ \_ no \_ se encontró el protocolo BHERR**</dt> </dl> | El protocolo especificado por el parámetro *AddressType* no es válido para el marco.<br/> |
| <dl> <dt>**BHERR \_ no válido \_ HFRAME**</dt> </dl>      | El valor del parámetro *hFrame* no es válido.<br/>                                        |



 

## <a name="remarks"></a>Observaciones

Se permite un tipo de dirección de **tipo de dirección \_ \_ Buscar \_ superior** . Cuando se usa este tipo de dirección, la función busca la dirección IP de IPX, XNS, IP o VINEs antes de devolver la dirección ETHERNET, TOKENRING o FDDI. Este enfoque es útil para los protocolos y entornos en los que se pueden multiplexar dos NIC en una sola dirección de servidor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




