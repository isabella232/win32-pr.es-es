---
title: XTYP_WILDCONNECT transacción (ddeml. h)
description: Permite a un cliente establecer una conversación en cada uno de los pares nombre de servicio y nombre de tema del servidor que coinciden con el nombre de servicio y el nombre de tema especificados.
ms.assetid: 4651e14f-ca13-412e-853d-326a13db78e4
keywords:
- Intercambio de datos de transacciones XTYP_WILDCONNECT
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
ms.openlocfilehash: cc63d6c367aebc440418beaabb0a06f05b0df967
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705135"
---
# <a name="xtyp_wildconnect-transaction"></a>XTYP \_ WILDCONNECT

Permite a un cliente establecer una conversación en cada uno de los pares nombre de servicio y nombre de tema del servidor que coinciden con el nombre de servicio y el nombre de tema especificados. Una función de devolución de llamada de servidor Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe esta transacción cuando un cliente especifica un nombre de servicio **nulo** , un nombre de tema **nulo** o ambos en una llamada a la función [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) o [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) .


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

No se utiliza.

</dd> <dt>

*hconv* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*hsz1* 
</dt> <dd>

Identificador del nombre del tema. Si este parámetro es **null**, el cliente solicita una conversación en todos los nombres de tema admitidos por el servidor.

</dd> <dt>

*hsz2* 
</dt> <dd>

Identificador del nombre del servicio. Si este parámetro es **null**, el cliente solicita una conversación en todos los nombres de servicio admitidos por el servidor.

</dd> <dt>

*hdata* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*dwData1* 
</dt> <dd>

Puntero a una estructura [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) que contiene información de contexto para la conversación. Si el cliente no es una aplicación DDEML, este parámetro se establece en 0.

</dd> <dt>

*dwData2* 
</dt> <dd>

Especifica si el cliente es la misma instancia de aplicación que el servidor. Si el parámetro es 1, el cliente es la misma instancia. Si el parámetro es 0, el cliente es una instancia diferente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El servidor debe devolver un identificador de datos que identifique una matriz de estructuras [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) . La matriz debe contener una estructura para cada par de nombre de servicio y nombre de tema que coincida con el par de nombre de servicio y nombre de tema solicitado por el cliente. La matriz debe terminar con un identificador de cadena **null** . El sistema envía la transacción de [**\_ \_ confirmación de conexión de XTYP**](xtyp-connect-confirm.md) al servidor para confirmar cada conversación y pasar los identificadores de conversación al servidor. El servidor no recibirá estas confirmaciones si especificó la marca **CBF \_ SKIP \_ Connect \_ Confirmations** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

El servidor debe devolver **null** para rechazar la transacción **XTYP \_ WILDCONNECT** .

## <a name="remarks"></a>Observaciones

Esta transacción se filtra si la aplicación de servidor especificó la marca **CBF \_ FAIL \_ Connections** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Un servidor no puede bloquear este tipo de transacción; \_se omite el código de retorno del bloque CBR.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Ddeml. h (incluir Windows. h)</dt> </dl> |



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

**Vista**
</dt> <dt>

[Biblioteca de administración de Intercambio dinámico de datos](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

