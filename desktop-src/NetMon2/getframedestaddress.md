---
description: Recupera la dirección de destino de un marco.
ms.assetid: f19a6753-37d8-4ec7-a7d4-ced0292d453c
title: Función GetFrameDestAddress (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169309"
---
# <a name="getframedestaddress-function"></a>Función GetFrameDestAddress

La **función GetFrameDestAddress** recupera la dirección de destino de un marco.

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

Identificador del marco al que se debe obtener un puntero.

</dd> <dt>

*lpAddress* 
</dt> <dd>

Búfer de retorno que almacena la dirección de destino del marco.

</dd> <dt>

*AddressType* 
</dt> <dd>

Un tipo de dirección, como ADDRESS \_ TYPE ETHERNET o ADDRESS TYPE \_ \_ \_ IP.

</dd> <dt>

*Marcas* 
</dt> <dd>

Marcas usadas para modificar los datos de direcciones de destino devueltos.



| Value                                                                                                                                                                                                           | Significado                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <dt>**NORMALIZACIÓN DE \_ LAS MARCAS ADDRESSTYPE \_**</dt> </dl>        | Cancela el enrutamiento y los BIT de grupo.<br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <dt>**ADDRESSTYPE \_ MARCA BIT \_ \_ REVERSE**</dt> </dl> | Convierte las direcciones de red de anillo de token de vuelta a la normalidad.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el *valor lpAddress* es válido y el valor devuelto es BHERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es un código de error.



| Código devuelto                                                                                                | Descripción                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**NO SE ENCONTRÓ EL PROTOCOLO BHERR \_ \_ \_**</dt> </dl> | El protocolo especificado en el *parámetro AddressType* no es válido para el marco.<br/> |
| <dl> <dt>**HFRAME NO \_ VÁLIDO DE BHERR \_**</dt> </dl>      | El *valor hFrame* no es válido.<br/>                                                  |



 

## <a name="remarks"></a>Observaciones

Se permite el tipo de dirección **\_ ADDRESS TYPE FIND \_ \_ HIGHEST.** Cuando se usa este tipo de dirección, la función busca la dirección IPX, XNS, IP o HEXADECIMALS antes de devolver la dirección ETHERNET, TOKENRING o FDDI. Este enfoque es útil para los protocolos y en entornos en los que se pueden multiplexación dos NIC en una sola dirección de servidor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




