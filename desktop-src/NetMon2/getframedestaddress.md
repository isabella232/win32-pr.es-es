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
ms.openlocfilehash: d7719392794027567521ce3e9c1bd1caf8ecbf76110f76ad0e54e0dd6549aae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366630"
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

Identificador del marco al que se obtiene un puntero.

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

Marcas usadas para modificar los datos de dirección de destino devueltos.



| Value                                                                                                                                                                                                           | Significado                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <dt>**NORMALIZACIÓN DE \_ MARCAS DE TIPO DE \_ DIRECCIÓN**</dt> </dl>        | Cancela el enrutamiento y los BIT de grupo.<br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <dt>**MARCAS DE TIPO \_ DE DIRECCIÓN \_ BIT \_ INVERSO**</dt> </dl> | Convierte las direcciones de red del anillo de token de vuelta a la normalidad.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor *lpAddress* es válido y el valor devuelto es BHERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es un código de error.



| Código devuelto                                                                                                | Descripción                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**NO SE ENCONTRÓ EL PROTOCOLO BHERR \_ \_ \_**</dt> </dl> | El protocolo especificado en el *parámetro AddressType* no es válido para el marco.<br/> |
| <dl> <dt>**HFRAME NO \_ VÁLIDO DE BHERR \_**</dt> </dl>      | El *valor hFrame* no es válido.<br/>                                                  |



 

## <a name="remarks"></a>Comentarios

Se **permite el tipo de dirección ADDRESS TYPE FIND \_ \_ \_ HIGHEST.** Cuando se usa este tipo de dirección, la función busca la dirección IP DE IPX, XNS, IP o SARS antes de devolver la dirección ETHERNET, TOKENRING o FDDI. Este enfoque es útil para protocolos y entornos en los que se pueden multiplexadas dos NIC en una sola dirección de servidor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




