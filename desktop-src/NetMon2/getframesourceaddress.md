---
description: Recupera la dirección de origen de un marco.
ms.assetid: 414f9e64-f1b2-46f1-822e-0fffacfad843
title: Función GetFrameSourceAddress (Netmon.h)
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
ms.openlocfilehash: 4878e08b8d8fb475c0da23d2ed765819fa14a10cd93140c791ed8603b1677584
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366322"
---
# <a name="getframesourceaddress-function"></a>Función GetFrameSourceAddress

La **función GetFrameSourceAddress** recupera la dirección de origen de un marco.

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

Identificador del marco al que se va a obtener un puntero.

</dd> <dt>

*lpAddress* 
</dt> <dd>

Búfer devuelto que almacena la dirección de origen del marco.

</dd> <dt>

*AddressType* 
</dt> <dd>

Tipo de dirección que se busca, como ADDRESS \_ TYPE ETHERNET o ADDRESS TYPE \_ \_ \_ IP.

</dd> <dt>

*Marcas* 
</dt> <dd>

Marcas usadas para modificar los datos devueltos de la dirección de origen.



| Valor                                                                                                                                                                                                           | Significado                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <dt>**NORMALIZACIÓN DE \_ LAS MARCAS ADDRESSTYPE \_**</dt> </dl>        | Cancela el enrutamiento y los BIT de grupo.<br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <dt>**ADDRESSTYPE \_ MARCA BIT \_ \_ REVERSE**</dt> </dl> | Convierte las direcciones de red de anillo de token de vuelta a la normalidad.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el *valor lpAddress* es válido y el valor devuelto es BHERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es un código de error.



| Código devuelto                                                                                                | Descripción                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**NO SE ENCONTRÓ EL PROTOCOLO BHERR \_ \_ \_**</dt> </dl> | El protocolo especificado por el *parámetro AddressType* no es válido para el marco.<br/> |
| <dl> <dt>**HFRAME NO \_ VÁLIDO DE BHERR \_**</dt> </dl>      | El *valor del parámetro hFrame* no es válido.<br/>                                        |



 

## <a name="remarks"></a>Comentarios

Se permite un tipo **de dirección de TIPO DE DIRECCIÓN FIND \_ \_ \_ HIGHEST.** Cuando se usa este tipo de dirección, la función busca la dirección IPX, XNS, IP o HEXADECIMALS antes de devolver la dirección ETHERNET, TOKENRING o FDDI. Este enfoque es útil para los protocolos y entornos en los que se pueden multiplexación dos NIC en una sola dirección de servidor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




