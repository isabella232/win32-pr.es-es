---
title: XTYP_WILDCONNECT transacción (Ddeml.h)
description: Permite que un cliente establezca una conversación en cada uno de los pares de nombre de servicio y nombre de tema del servidor que coincidan con el nombre de servicio y el nombre del tema especificados.
ms.assetid: 4651e14f-ca13-412e-853d-326a13db78e4
keywords:
- XTYP_WILDCONNECT datos de transacción Exchange
topic_type:
- apiref
api_name:
- XTYP_WILDCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b2b170a8d2362dec6311f935a5bc0bb92fa16a9b04270afc59d8fe5ad5c19f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914735"
---
# <a name="xtyp_wildconnect-transaction"></a>Transacción WILDCONNECT de XTYP \_

Permite que un cliente establezca una conversación en cada uno de los pares de nombre de servicio y nombre de tema del servidor que coincidan con el nombre de servicio y el nombre del tema especificados. Una función de devolución de llamada de servidor datos dinámicos Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe esta transacción cuando un cliente especifica un nombre de servicio **NULL,** un nombre de tema **NULL** o ambos en una llamada a la función [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) [**o DdeConnectList.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_WILDCONNECT        (0x00E0 | XCLASS_DATA | XTYPF_NOBLOCK)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uType* 
</dt> <dd>

El tipo de transacción.

</dd> <dt>

*uFmt* 
</dt> <dd>

No se usa.

</dd> <dt>

*hconv* 
</dt> <dd>

No se usa.

</dd> <dt>

*hsz1* 
</dt> <dd>

Identificador del nombre del tema. Si este parámetro es **NULL,** el cliente solicita una conversación en todos los nombres de tema que admite el servidor.

</dd> <dt>

*hsz2* 
</dt> <dd>

Identificador del nombre del servicio. Si este parámetro es **NULL,** el cliente solicita una conversación en todos los nombres de servicio que admite el servidor.

</dd> <dt>

*hdata* 
</dt> <dd>

No se usa.

</dd> <dt>

*dwData1* 
</dt> <dd>

Puntero a una [**estructura CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) que contiene información de contexto para la conversación. Si el cliente no es una aplicación DDEML, este parámetro se establece en 0.

</dd> <dt>

*dwData2* 
</dt> <dd>

Especifica si el cliente es la misma instancia de aplicación que el servidor. Si el parámetro es 1, el cliente es la misma instancia. Si el parámetro es 0, el cliente es una instancia diferente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El servidor debe devolver un identificador de datos que identifique una matriz de [**estructuras HSZPAIR.**](/windows/win32/api/ddeml/ns-ddeml-hszpair) La matriz debe contener una estructura para cada par nombre-servicio y nombre-tema que coincida con el par nombre-servicio y nombre-tema solicitado por el cliente. Un identificador de cadena NULL debe terminar la **matriz.** El sistema envía la [**transacción XTYP \_ CONNECT \_ CONFIRM**](xtyp-connect-confirm.md) al servidor para confirmar cada conversación y pasar los identificadores de conversación al servidor. El servidor no recibirá estas confirmaciones si especificó la marca **CBF \_ SKIP CONNECT \_ \_ CONFIRMS** en la [**función DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

El servidor debe devolver **NULL para** rechazar la **transacción \_ XTYP WILDCONNECT.**

## <a name="remarks"></a>Comentarios

Esta transacción se filtra si la aplicación de servidor especificó la **marca CBF \_ FAIL \_ CONNECTIONS** en la [**función DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

Un servidor no puede bloquear este tipo de transacción; Se omite \_ el código de retorno CBR BLOCK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Ddeml.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair)
</dt> <dt>

**Conceptual**
</dt> <dt>

[datos dinámicos Exchange management library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

